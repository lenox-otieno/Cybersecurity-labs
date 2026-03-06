# Incident Investigation: Phishing Email Attempt

## Severity
High

## Description

A suspicious email claiming to be from Microsoft support was flagged for investigation.

The email attempted to impersonate Microsoft services and potentially trick the recipient into interacting with malicious content.

---

## Indicators

Sender Email:
support@microsoft.com

Recipient:
e.huffman@tryhackme.thm

Authentication Results:

SPF: Failed  
DKIM: Failed  

---

## Investigation

Email authentication checks revealed that the message failed both **SPF and DKIM validation**, which indicates the sender was likely spoofed.

The email attempted to appear as a legitimate Microsoft support message.

---

## Analysis

Email spoofing is a common technique used in phishing campaigns.

Attackers impersonate trusted organizations to:

- Steal credentials
- Deliver malware
- Trick users into clicking malicious links

Because both authentication mechanisms failed, the email was considered malicious.

---

## Verdict

True Positive – Phishing Attempt

---

## Response

The alert was escalated to a **Level 2 SOC Analyst** for further investigation.

---

## Lessons Learned

Email authentication checks such as **SPF and DKIM** are critical in identifying phishing attempts.
