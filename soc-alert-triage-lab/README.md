# SOC Alert Triage Lab

This project demonstrates practical **Security Operations Center (SOC) alert triage skills** using a simulated SOC dashboard from TryHackMe.

The goal of this lab was to analyze alerts, investigate indicators, and determine whether alerts were **True Positives or False Positives**.

---

## Skills Demonstrated

- Security Alert Triage
- Incident Investigation
- False Positive Identification
- Threat Analysis
- Security Tool Usage
- Basic SOC Workflow

---

## SOC Triage Methodology

When triaging alerts, I followed this process:

1. Identify alert severity
2. Review alert details
3. Investigate user activity
4. Check domain/IP reputation
5. Analyze file indicators
6. Determine verdict
7. Document findings

---

## Alerts Investigated

| Alert Name | Severity | Verdict |
|------------|----------|--------|
| Potential Data Exfiltration | Critical | False Positive |
| Double-Extension File Creation | High | True Positive |
| Suspicious URL Activity | Medium | False Positive |

---

## Key Lessons Learned

- File extensions can be manipulated by attackers.
- Large data transfers are not always malicious.
- Reputation analysis (VirusTotal) is important during investigations.
- Context is critical in determining alert verdicts.

---

## Tools Used

- SOC Dashboard
- VirusTotal
- Threat Intelligence Sources

---

## Platform

Lab completed on **TryHackMe**

---

## Author

Lenox Otieno  
Cybersecurity Analyst | SOC Enthusiast
