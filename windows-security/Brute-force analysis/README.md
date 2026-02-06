# Investigating Failed Login Attempts Using Windows Event Logs

## Objective
To identify and analyze failed login attempts in a Windows environment in order to detect potential brute-force attacks.

## Tools Used
- Windows Event Viewer
- Local Security Policy
- VirtualBox

## Methodology
1. Configured auditing for logon events.
2. Generated multiple failed login attempts.
3. Filtered Event ID 4625 in Event Viewer.
4. Correlated timestamps and source details.

## Screenshots
Screenshots are available in the `/screenshots` folder.

## Findings
- Multiple failed login attempts from a single source.
- No account lockout policy configured.

## Lessons Learned
- Event logs are critical for detecting authentication attacks.
- Proper security policies reduce brute-force risk.

