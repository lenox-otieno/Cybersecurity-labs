# SIEM Alert Investigation – Potential CryptoMiner Activity

## Overview

This investigation analyzes a SIEM alert triggered by suspicious process execution detected in Windows Event Logs. The alert rule was configured to identify potential cryptocurrency mining activity based on process name patterns.

The objective of this investigation was to identify the process responsible for the alert, determine the user involved, and verify whether the activity represented a true security threat.

---

## Alert Details

**Alert Name:** Potential CryptoMiner Activity  
**Event ID:** 4688 (Process Creation)  
**Log Source:** Windows Event Logs  

**Detection Rule:**

EventID = 4688  
ProcessName = (*miner* OR *crypt*)

This rule triggers whenever a newly created process contains the keywords **miner** or **crypt**, which are commonly associated with cryptocurrency mining malware.

---

## Investigation Steps

### 1. Trigger Suspicious Activity

After initiating the simulated suspicious activity in the SIEM dashboard, an alert was generated indicating a potentially malicious process execution.

---

### 2. Identify the Suspicious Process

The process responsible for triggering the alert was:

cudominer.exe 


This process name contains the keyword **miner**, which matched the detection rule configured in the SIEM.

---

### 3. Identify the User Responsible

Analysis of the event logs revealed that the process was executed by the user:

chris


---

### 4. Identify the Host Machine

The system where the suspicious process was executed was identified as:

HR_02


---

### 5. Rule Match Analysis

The SIEM rule searched for processes containing:


---

### 5. Rule Match Analysis

The SIEM rule searched for processes containing:

miner
crypt


The process **cudominer.exe** matched the keyword:

miner


which triggered the alert.

---

## Indicators Observed

| Indicator | Value |
|-----------|------|
Process Name | cudominer.exe |
User | chris |
Host | HR_02 |
Event ID | 4688 |
Log Source | Windows Event Logs |

---

## Event Classification

**True Positive**

The SIEM alert successfully detected a suspicious process associated with cryptocurrency mining activity.

Cryptomining malware can consume system resources and may indicate unauthorized software execution within the network.

---

## Key Takeaways

This investigation demonstrates how SIEM platforms can detect suspicious activity through rule-based monitoring of system logs.

Important SOC skills demonstrated in this exercise include:

- Alert triage
- Log analysis
- Process investigation
- Detection rule analysis
- Event classification

---

## Skills Practiced

- SIEM Monitoring
- Security Event Analysis
- Incident Investigation
- Windows Event Log Analysis
- Threat Detection

---
