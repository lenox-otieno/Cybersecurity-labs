# Alert Investigation: Potential Data Exfiltration

## Alert Severity
Critical

## Alert Description
The SOC dashboard generated an alert indicating a potential data transfer of **5GB of data**.

Large data transfers can indicate possible **data exfiltration attempts**.

---

## Investigation Steps

1. Reviewed alert details in SOC dashboard
2. Checked source domain involved in transfer
3. Investigated traffic source

Source Domain:
zoom.us

---

## Analysis

The domain **zoom.us** is a legitimate domain used for video conferencing.

The large data transfer was likely caused by **multiple Zoom meetings or file transfers during meetings**.

No evidence of malicious activity was observed.

---

## Verdict

False Positive

---

## Lessons Learned

Not all large data transfers are malicious.  
Context and domain verification are essential in SOC investigations.
