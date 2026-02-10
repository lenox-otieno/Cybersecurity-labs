# Wireshark Basics: ICMP Traffic Analysis and SOC Use Cases

## Objective
The objective of this lab was to understand the core features of Wireshark and how they are applied in a SOC environment. The focus was on packet capture fundamentals, filtering techniques, traffic analysis, and practical SOC use cases such as incident response and threat hunting.

---

## Tools Used
- Wireshark
- Windows / Linux host
- Network interface (Ethernet / Wi-Fi)

---

## Concepts Covered
- Wireshark preferences
- Wireshark profiles
- Capture filters vs display filters
- Following a stream
- Colorizing traffic
- ICMP traffic analysis

---

## Methodology

### 1. Wireshark Preferences
- Reviewed Wireshark preferences to understand packet display, name resolution, and capture settings.
- Adjusted settings to improve packet visibility and analysis efficiency.

---

### 2. Wireshark Profiles
- Explored Wireshark profiles to separate workflows.
- Understood how profiles help SOC analysts switch between tasks such as:
  - Incident response
  - Malware analysis
  - Threat hunting

---

### 3. Capture Filter vs Display Filter
- Studied the difference between capture filters and display filters.

**Capture Filters**
- Applied before packet capture begins.
- Used to limit the traffic captured.
- 
**Display Filters**
- Applied after traffic has been captured.
- Used to analyze specific traffic.
- Example:

---

### 4. Capturing ICMP Traffic
- Started a packet capture using a capture filter for ICMP traffic.
- Generated ICMP packets using ping commands.
- Verified that only ICMP packets were captured.

---

### 5. Display Filtering ICMP Traffic
- Captured normal network traffic.
- Applied a display filter to isolate ICMP packets.
- Observed ICMP request and reply packets.

---

### 6. Following a Stream
- Used the “Follow Stream” feature to reconstruct communication flows.
- Understood how this helps in analyzing conversations between hosts.

---

### 7. Colorizing Traffic
- Used Wireshark’s color rules to highlight ICMP traffic.
- Improved visibility of specific protocols during analysis.
- Observed how colorization helps SOC analysts quickly identify suspicious traffic patterns.

---

## Screenshots
Relevant screenshots for this lab are available in the `/screenshots` directory and include:
- ICMP packets in capture view
- Display filter usage
- Colorized ICMP traffic
- Follow stream output

---

## Findings
- Capture filters reduce noise by limiting traffic at capture time.
- Display filters allow flexible post-capture analysis.
- ICMP traffic is easily identifiable and useful for detecting network reconnaissance.
- Color rules significantly improve analysis speed in busy packet captures.

---

## SOC Use Cases

### Incident Response
- Identify suspicious ICMP traffic used for network mapping or beaconing.

### Malware Analysis
- Detect abnormal ICMP communication patterns that may indicate C2 activity.

### Threat Hunting
- Hunt for unusual ICMP behavior across packet captures.

### Protocol Troubleshooting
- Diagnose connectivity issues using ICMP request and reply analysis.

---

## Lessons Learned
- Understanding filters is critical for efficient packet analysis.
- Wireshark profiles help organize SOC workflows.
- Visual enhancements like color rules improve speed and accuracy.
- ICMP traffic analysis is a foundational skill for network security monitoring.

---

## Next Steps
- Analyze TCP and UDP traffic
- Explore DNS traffic and tunneling techniques
- Practice detecting suspicious traffic patterns

---

