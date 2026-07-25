# Threat Intelligence Report: Gainrep Spam Mail
**Date:** June 24, 2026  
**Analyst:** RD7  
**Severity:** [Low]  
**Status:** [Active]

---

## 1. Executive Summary
I received an email a couple of times from an organization I've not heard of, Gainrep. Now, I don't have any of my gmails connected to their mail service which was suspicious. From my little investigation, below are all I found.

---

## 2. Threat Actor & Campaign Details
* **Estimated Threat Actor:** Unknown
* **Target Industry/Region:** General
* **Delivery Method:** Email (Phishing)
* **Objective:** Credential Harvesting / Malware Drop

---

## 3. Technical Analysis

### 3.1 Email Delivery Details
Document the metadata pulled from the email headers here.

| Header Field | Value |
| :--- | :--- |
| **Subject Line** | `Endorse someone's name - Today's date` |
| **Display Name** | `Gainrep` |
| **Sender Address** | `noreply@gainrepmail[.]com` |
| **Return-Path** | `0100019f6e98c9a3-2606c4e2-ebb7-4d3c-be6f-7509ca92099a-000000@amazonses[.]com` |
| **Authentication Status** | SPF: [Pass] \| DKIM: [Pass] \| DMARC: [Pass] |

### 3.2 Infrastructure & Network Analysis
Detail the sender's IP address and what you found when you cross-referenced it.
* **Sender IP Address:** `54.240.14[.]56` *(Always defanged)*
* **ASN / ISP:** AS16509 / Amazon.com, Inc
* **Geolocation:** [e.g., United States]
* **IP Reputation:** Flagged on [AbuseIPDB / VirusTotal / Cisco Talos] with a abuse score of [X%]. Associated with historical phishing activities dating back to [Date].

---

## 4. Indicators of Compromise (IoCs)
*Note: All IoCs are defanged to prevent accidental execution.*

### Network Indicators
| Type | Value | Description |
| :--- | :--- | :--- |
| IP | `54.240.14[.]56` | Sender IP / Phishing Source |
| Domain | `em.gainrep[.]com` | Domain found in email body / link |
| URL | `hxxps://em.gainrepmail.com/CL0/hxxps:/www.gainrep.com/Signin%3Fa=55d87064-f04d-4c63-b6df-414235783839&i=c4a62d12-7a2f-404e-9d97-d1bb9029a2a9/1/0100019f92c13cc1-79d0ac42-926d-4c07-ba04-ab8d1a054561-000000/szkFc5JBR24-40jTbu7IbgNYNxd1EoX_VjU6XBzi8ZA=452` | Exact credential harvesting link |

### Email Indicators
| Type | Value | Description |
| :--- | :--- | :--- |
| Sender Email | `noreply@gainrepmail.com` | Envelope sender address |

---

## 5. Defensive Recommendations & Mitigations
What should defenders do about this specific threat?
1. **Block Network Indicators:** Ingest the provided IP `192.0.2[.]1` and domain `malicious-domain[.]com` into firewall, proxy, and email gateway blocklists.
2. **Email Rules:** Create an inbox rule to flag or quarantine external incoming emails matching the subject line prefix `[Subject Line]`.
3. **User Awareness:** Remind users to verify unexpected invoice notifications, specifically checking for inconsistencies between the display name and actual sender address.

---

## 6. References & External Tooling
* AbuseIPDB Report: `[Link to the IP's AbuseIPDB page]`
* [VirusTotal Analysis](https://www.virustotal.com/gui/url-analysis/u-94fa907dfbfed5228ec84ef2877fdb514d771df51fb85d397e8f85248be92c9c-10770121)
* [ThreatFeed Reference](https://hybrid-analysis.com/sample/3e971bdea6c98c09421ff86b695133e0a26ae1731ac285c5c8fd4ed4d9d88f25)
