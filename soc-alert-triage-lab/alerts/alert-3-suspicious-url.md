# Alert Investigation: Suspicious URL Activity

## Alert Severity
Medium

## Alert Description

The SOC dashboard generated an alert related to a **suspicious URL accessed by a user**.

Suspicious URLs can indicate:

- Phishing attempts
- Malware downloads
- Command and Control communication

---

## Investigation Steps

1. Reviewed alert information from the SOC dashboard
2. Identified the URL involved in the alert
3. Checked the reputation of the URL using **VirusTotal**
4. Investigated whether any files were downloaded

---

## Analysis

The URL was checked using **VirusTotal** to determine its reputation.

Results indicated:

- No malware detections
- No malicious reports
- No suspicious file downloads associated with the activity

The activity appeared to be **benign user browsing behavior**.

---

## Verdict

False Positive

---

## Reasoning

Although the system flagged the URL as suspicious, threat intelligence sources did not report any malicious activity associated with the domain.

There was no evidence of:

- Malware downloads
- Phishing activity
- Command and control communication

---

## Lessons Learned

Not all alerts indicate real threats.  

SOC analysts must always verify alerts using **threat intelligence platforms** before making a final determination.

False positives are common in SOC environments and proper investigation is necessary before escalation.
