# SOC Case Study: Phishing Email Alert

## Case Overview
**Alert Type:** Suspicious Email with External Link  
**Date/Time:** 03/10/2026 08:30 – 03/10/2026 08:32  
**Source:** Email Gateway / Firewall  

---

## 1. Affected Entities
- User: `h.harris@thetrydaily.thm`  
- Endpoint IP: `10.20.2.17`  

---

## 2. Email Details
**Sender:** urgents@amazon.biz  
**Subject:** Your Amazon Package Couldn’t Be Delivered – Action Required  
**Attachment:** None  
**URL:** [http://bit.ly/3sHkX3da12340](http://bit.ly/3sHkX3da12340)  

**Observations:**  
- Domain impersonates Amazon (`amazon.biz`)  
- URL uses Bit.ly shortening service  
- Generic greeting and urgent action requested  

---

## 3. Timeline of Activity
| Timestamp | Event | Source IP | URL | Action |
|-----------|-------|-----------|-----|--------|
| 03/10/2026 08:30:51 | Email received | – | http://bit.ly/3sHkX3da12340 | Alert triggered |
| 03/10/2026 08:32:05 | User clicked link | 10.20.2.17 | http://bit.ly/3sHkX3da12340 | Firewall blocked |

---

## 4. Reason for True Positive
- Sender domain is not legitimate Amazon domain  
- URL uses shortener to hide destination  
- Social engineering language (“Action Required”, 48-hour deadline)  
- User interaction recorded in firewall logs  

---

## 5. Reason for Escalation
- User attempted to click phishing URL  
- Potential malware download or credential theft if blocked measures fail  
- Ensures SOC team confirms no other users clicked the URL  

---

## 6. Recommended Remediation Actions
1. Block sender domain (`amazon.biz`) in email gateway  
2. Block phishing URL (`http://bit.ly/3sHkX3da12340`) in firewall/proxy  
3. Notify affected user about the phishing attempt  
4. Verify firewall logs for other endpoints accessing this URL  
5. Document case in SOC logs  

---

## 7. Attack Indicators (IOCs)
- Sender: `urgents@amazon.biz`  
- Subject: Your Amazon Package Couldn’t Be Delivered – Action Required  
- URL: `http://bit.ly/3sHkX3da12340`  
- Destination IP: 67.199.248.11  
- Source IP: 10.20.2.17  
- Firewall Action: Blocked  

---

## 8. Conclusion
The alert was a **confirmed phishing attempt**.  
The user attempted to click the malicious link, but the **firewall successfully blocked it**, preventing compromise.  
SOC measures contained the threat, and recommended actions have been applied.
