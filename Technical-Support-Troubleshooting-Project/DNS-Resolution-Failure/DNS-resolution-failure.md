# DNS Resolution Failure

## User Complaint
“The website won’t load.”

A customer reported that the website was completely inaccessible. The browser displayed a generic error page and no HTTP request reached the server. This usually indicates a DNS‑level failure rather than a server or application issue.

To understand the customer’s complaint, I reproduced the problem on my own machine using a domain that does not exist (`http://thisdomainshouldneverexist12345.com`). This allowed me to simulate the exact behaviour a customer experiences when DNS resolution fails. The goal was to confirm whether the browser could reach the server or whether the failure happened earlier in the process.

---

## Symptoms
When reproducing the issue, I observed the following:

- The browser showed **“This site can’t be reached.”**  
  [View screenshot](evidence/browser-error.png)

- The error code was **DNS_PROBE_FINISHED_NXDOMAIN.**  
  [View screenshot](evidence/browser-error.png)

- The Network tab showed a failed document request with no response from the server.  
  [View screenshot](evidence/browser-error.png)

- Other websites loaded normally.

- The issue persisted across multiple browsers.

These symptoms strongly suggested a DNS resolution problem.

---

## Tools Used
To investigate the issue, I used the following tools, with each tool helping confirm whether the problem was DNS, network, or server related:

- **nslookup** – to check whether the domain could be resolved by DNS  
- **ping** – to test whether the host could be reached at the network level  
- **Chrome DevTools** (Console and Network tabs) – to observe browser‑level errors and network behaviour  
- **tracert / traceroute** – to check whether any routing path existed to the domain  
- **DNS propagation checker** – to verify whether DNS records were available across global DNS servers  

---

## Diagnosis Steps

### Step 1 — DNS Lookup
Running `nslookup thisdomainshouldneverexist12345.com` returned no IP address and showed **“Non-existent domain.”** This confirmed that the domain doesn’t exist in DNS.  
[View screenshot](evidence/browser-error.png)

### Step 2 — Verify DNS Works for Other Domains
Running `nslookup google.com` resolved successfully, which ruled out a local DNS server failure.  
[View screenshot](evidence/browser-error.png)

### Step 3 — Check DNS Propagation
Using an online DNS propagation checker showed that **all global DNS servers returned NXDOMAIN**. This confirmed that the domain had no valid DNS records anywhere and that the failure was consistent across all regions.  
[View screenshot](evidence/browser-error.png)

### Step 4 — Inspect DNS Records
Using a DNS lookup tool, I checked whether the domain had any DNS records. The lookup returned an **NXDOMAIN** response and showed **no A record, no CNAME, and no NS entries**. This confirmed that the domain had no DNS configuration at all, which explains why the browser could not resolve it.  
[View screenshot](evidence/browser-error.png)

### Step 5 — Ping Test
Running `ping thisdomainshouldneverexist12345.com` returned **“unknown host,”** confirming DNS failure rather than a network connectivity issue.  
[View screenshot](evidence/browser-error.png)

### Step 6 — Traceroute
Running `tracert thisdomainshouldneverexist12345.com` failed immediately with **no hops recorded**. This confirmed the request never left the local machine because DNS resolution failed first.  
[View screenshot](evidence/browser-error.png)

---

## Root Cause
The domain had **no DNS records configured**. When DNS lookup tools returned NXDOMAIN, it confirmed that DNS could not map the domain name to an IP address. Because DNS resolution failed at the very first step, the browser never reached the server. This made the website appear offline even though the underlying hosting or application was not involved. This is a classic DNS misconfiguration scenario.

---

## Resolution
I verified the issue by reproducing the failure locally, confirmed the absence of DNS records using lookup tools, and validated that the problem was isolated to this domain.

In a real environment, the fix would involve:

- Adding or correcting the **A record** to point to the correct server  
- Ensuring **NS records** are valid and authoritative  
- Lowering **TTL values** to speed up propagation  
- Flushing local DNS caches to remove stale entries  
- Re‑checking global propagation to confirm the fix has spread  

Once DNS was corrected, the domain would resolve normally and the website would load.

---

## Customer‑Facing Explanation
“The website wasn’t loading because the domain name wasn’t pointing to any server. It’s similar to entering an address into GPS that doesn’t exist — the browser had nowhere to go. The DNS settings have now been corrected, and once the updated information reaches all networks, the site will load normally again.”

---

## Evidence
- [Browser error — “This site can’t be reached” with NXDOMAIN](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/loading-failure-browser.png)
- [DevTools Console — DNS resolution error](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/dns-console-error.png)
- [DevTools Network — No response from server](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/failed-document-request.png)
- [nslookup — Domain returns NXDOMAIN](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/nslookup-nxdomain.png.png)
- [nslookup — Other domain success](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/nslookup-success.png)
- [DNS propagation check — NXDOMAIN across all global DNS servers](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/dns-propagation-check.png)
- [DNS record lookup — No A, CNAME, or NS records](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/dns-records-missing.png)
- [ping — “unknown host,” confirming DNS failure](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/ping-nxdomain.png)
- [traceroute — Fails immediately, no hops recorded](/Technical-Support-Troubleshooting-Project/DNS-Resolution-Failure/Evidence/traceroute-nxdomain.png)
