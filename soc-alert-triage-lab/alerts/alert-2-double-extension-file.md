# Alert Investigation: Double-Extension File Creation

## Alert Severity
High

## Alert Name
Double-Extension File Creation

---

## Alert Description

The SOC dashboard generated an alert indicating that a file with a **double extension** had been created on a system.

Example format:

invoice.pdf.exe

Attackers often use double extensions to **trick users into thinking a file is safe** while hiding a malicious executable.

---

## Investigation Steps

1. Reviewed alert details from the SOC dashboard
2. Checked the filename and extension pattern
3. Investigated the user activity associated with the file
4. Analyzed whether the extension was attempting to disguise an executable

---

## Analysis

Double-extension files are a **common social engineering technique** used in phishing or malware delivery.

For example:

document.txt.exe  
invoice.pdf.exe

These files appear to be documents but are actually **executable malware**.

The presence of a double extension strongly indicates **malicious intent**, especially if the file was downloaded from an external source or email attachment.

---

## Verdict

True Positive

---

## Security Risk

If executed, the file could:

- Install malware
- Create backdoors
- Allow attacker persistence
- Lead to credential theft

---

## Recommended Response

- Isolate the affected system
- Remove the suspicious file
- Scan the system for malware
- Educate the user about suspicious attachments

---

## Lessons Learned

Attackers frequently manipulate file extensions to bypass user suspicion.  
SOC analysts must verify **actual file types rather than trusting filenames alone.**
