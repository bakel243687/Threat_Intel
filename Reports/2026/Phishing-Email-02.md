# Threat Intelligence Report: [Campaign Name or Theme]
**Date:** June 4, 2026  
**Analyst:** [Your Name/Handle]  
**Severity:** [Low / Medium / High]  
**Status:** [Active / Contained / Mitigated]

---

## 1. Executive Summary
Provide a 2-3 sentence overview of what happened. Who was targeted, what was the lure, and what is the ultimate goal of the attack if known (e.g., credential theft, malware delivery).
*Example: A targeted phishing campaign utilizing a fake invoice lure was observed targeting corporate inboxes. The campaign attempts to direct victims to a credential harvesting page hosted on compromised infrastructure.*

---

## 2. Threat Actor & Campaign Details
* **Estimated Threat Actor:** [Unknown / Known Group Name]
* **Target Industry/Region:** [e.g., General, Financial, Tech / Global]
* **Delivery Method:** Email (Phishing)
* **Objective:** [Credential Harvesting / Malware Drop / Financial Fraud]

---

## 3. Technical Analysis

### 3.1 Email Delivery Details
Document the metadata pulled from the email headers here.

| Header Field | Value |
| :--- | :--- |
| **Subject Line** | `[Insert Subject Line Here]` |
| **Display Name** | `[Insert Spoofed Name]` |
| **Sender Address** | `badguy@example[.]com` |
| **Return-Path** | `bounce-handler@example[.]com` |
| **Authentication Status** | SPF: [Pass/Fail] \| DKIM: [Pass/Fail] \| DMARC: [Pass/Fail] |

### 3.2 Infrastructure & Network Analysis
Detail the sender's IP address and what you found when you cross-referenced it.
* **Sender IP Address:** `192.0.2[.]1` *(Always defanged)*
* **ASN / ISP:** [e.g., AS16509 / Amazon.com, Inc.]
* **Geolocation:** [e.g., United States]
* **IP Reputation:** Flagged on [AbuseIPDB / VirusTotal / Cisco Talos] with a abuse score of [X%]. Associated with historical phishing activities dating back to [Date].

---

## 4. Indicators of Compromise (IoCs)
*Note: All IoCs are defanged to prevent accidental execution.*

### Network Indicators
| Type | Value | Description |
| :--- | :--- | :--- |
| IP | `192.0.2[.]1` | Sender IP / Phishing Source |
| Domain | `malicious-domain[.]com` | Domain found in email body / link |
| URL | `hxxps://malicious-domain[.]com/login` | Exact credential harvesting link |

### Email Indicators
| Type | Value | Description |
| :--- | :--- | :--- |
| Sender Email | `attacker@spoofed-domain[.]com` | Envelope sender address |
| SHA256 (Attachment) | `e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855` | Hash of malicious attachment (if applicable) |

---

## 5. Defensive Recommendations & Mitigations
What should defenders do about this specific threat?
1. **Block Network Indicators:** Ingest the provided IP `192.0.2[.]1` and domain `malicious-domain[.]com` into firewall, proxy, and email gateway blocklists.
2. **Email Rules:** Create an inbox rule to flag or quarantine external incoming emails matching the subject line prefix `[Subject Line]`.
3. **User Awareness:** Remind users to verify unexpected invoice notifications, specifically checking for inconsistencies between the display name and actual sender address.

---

## 6. References & External Tooling
* AbuseIPDB Report: `[Link to the IP's AbuseIPDB page]`
* VirusTotal Analysis: `[Link to URL/IP analysis if scanned]`
* ThreatFeed Reference: `[Link if matching a known community feed]`
