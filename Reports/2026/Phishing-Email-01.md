# Report

# Threat Intelligence Report: 
**Date:** June 4, 2026  
**Analyst:** RD7  
**Severity:** Low  
**Status:** Active

## 1. Executive Summary

A phishing Email was sent to me to lure me into clicking a button link to a website where I would input my debit card details to renew my subscription to a cloud storage service I have never known.

---

## 2. Threat Actor & Campaign Details
* **Estimated Threat Actor:** Unknown
* **Target Industry/Region:** Individuals
* **Delivery Method:** Email (Phishing)
* **Objective:** Credential Harvesting/Financial Fraud

---

## 3. Technical Analysis

**Note**: receiver's email - if your email is someone234@gmail.com, then the receiver's email is someone234. Without the domain name.

### 3.1 Email Delivery Details
| Header Field | Value |
| :--- | :--- |
| **Subject Line** | `We've Blocked Your Account! Your photos and videos will be deleted on receiver's email` |
| **Display Name** | `one.ass0036` |
| **Sender Address** | `alert-0633@idojn[.]uha` |
| **Return-Path** | `receiver's email@one.ass0036.rallysynchub.biz.ua` |
| **Authentication Status** | SPF: Pass \| DKIM: Pass \| DMARC: Fail |

### 3.2 Infrastructure & Network Analysis

* **Sender IP Address:** `199.59.150[.]93` & `161.38.202[.]170`
* **ASN / ISP:** AS13414 / ( Twitter Inc. ) & AS396479 / ( Mailgun Technologies Inc. )
* **Geolocation:** United States
* **IP Reputation:** Flagged on VirusTotal with a abuse score of [0% & 1%]. Associated with historical phishing activities dating back to 2026-04-20.

---

## 4. Indicators of Compromise (IoCs)


### Network Indicators
| Type | Value | Description |
| :--- | :--- | :--- |
| IP | `199.59.150[.]93` & `161.38.202[.]170` | Sender IP / Phishing Source |
| Domain | `malicious-domain[.]com` | Domain found in email body / link |
| URL | `[hxxps://storage.googleapis[.]com/strow/strw_v2[.]html#?act=cl&pid=21554_md&uid=4&vid=1090248&ofid=336&lid=470&cid=118379]` | Identified as Phishing link |

### Email Indicators
| Type | Value | Description |
| :--- | :--- | :--- |
| Sender Email | `receiver's email@xkmj.one.ass0036.rallysynchub.biz.ua` / `alert-0633@idojn.uha` | Envelope sender address |


---

## 5. Defensive Recommendations & Mitigations
What should defenders do about this specific threat?
1. **Block Network Indicators:** Ingest the provided IP `199.59.150[.]93` & `161.38.202[.]170` and domain `633@idojn.uha` into firewall, proxy, and email gateway blocklists.
2. **Email Rules:** Create an inbox rule to flag or quarantine external incoming emails matching the subject line prefix `We've Blocked Your Account! Your photos and videos will be deleted on `.
3. **User Awareness:** Remind users to verify unexpected invoice notifications, specifically checking for inconsistencies between the display name and actual sender address.

---

## 6. References & External Tooling
* AbuseIPDB Report: [Link to 161.38.202.170 analysis](https://www.abuseipdb.com/check/161.38.202.170)  [Link to 199.59.150.93](https://www.abuseipdb.com/check/199.59.150.93)
* VirusTotal Analysis: [Link to 161.38.202.170 analysis](https://www.virustotal.com/gui/ip-address/161.38.202.170/detection)  [Link to 199.59.150.93](https://www.virustotal.com/gui/ip-address/199.59.150.93/relations)  [graph](https://www.virustotal.com/graph/embed/g3a79d97d1a374abd97ade35704b07145814051d8712f449b8494f42e729e1028?theme=dark)
* Hybrid Analysis: [Link](https://hybrid-analysis.com/sample/580639c5c4bb7e438160f9e6a9a04d3ec4c86d9b3c16feceec8e76c6b9f2ca09)
