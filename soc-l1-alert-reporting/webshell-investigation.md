# Incident Investigation: Possible Web Shell Activity

## Severity
Critical

## Description

A suspicious alert was generated indicating unusual processes running on a server located in the DMZ.

---

## Affected Host

DMZ-MSEXCHANGE-2013

Operating System:
Windows Server 2012 R2

---

## Suspicious Processes Detected

revshell.exe  
powershell.exe  
w3wp.exe  

---

## Investigation

The presence of **revshell.exe** indicates a potential reverse shell connection.

The process **w3wp.exe** is associated with IIS web services and can sometimes be abused to execute malicious code.

PowerShell is often used by attackers for **post-exploitation activities**.

---

## Analysis

The combination of these processes suggests that the server may have been compromised through a **web shell attack**.

Exchange servers have historically been targeted by attackers due to known vulnerabilities.

---

## Verdict

True Positive – Potential Web Shell Activity

---

## Response

The alert was escalated to the SOC Level 2 team for deeper forensic investigation.

---

## Lessons Learned

Servers exposed in the DMZ should be continuously monitored for:

- Suspicious processes
- Reverse shells
- Unusual PowerShell activity
