# HTTP Protocol Analysis: Methods and Response Codes

## Objective
The objective of this lab was to analyze HTTP traffic using Wireshark and understand how HTTP request methods and response status codes function in real-world network communication. The lab focused on identifying GET, POST, and PUT methods and interpreting common HTTP response codes.

---

## Tools Used
- Wireshark
- Web browser
- Local web server / Internet-based website
- Windows / Linux system

---

## Concepts Covered
- HTTP request methods (GET, POST, PUT)
- HTTP response structure
- HTTP status codes (200, 403, 404, 500)
- Filtering HTTP traffic in Wireshark
- SOC use cases for HTTP analysis

---

## HTTP Overview

Hypertext Transfer Protocol (HTTP) is an application-layer protocol used for communication between clients and servers.

It follows a request-response model:
- Client sends request
- Server returns response with status code

---

## HTTP Methods Analyzed

### 1. GET
- Used to request data from a server.
- Does not modify server resources.
- Commonly used when loading webpages.

### 2. POST
- Used to submit data to the server.
- Often used in login forms and file uploads.
- Can modify server-side resources.

### 3. PUT
- Used to update or replace a resource on the server.
- Common in APIs and web applications.

---

## HTTP Response Codes Observed

### 200 – OK
- Request was successful.
- Server returned the requested resource.

### 403 – Forbidden
- Server understood the request but refuses to authorize it.
- Often due to permission restrictions.

### 404 – Not Found
- Requested resource does not exist.
- Common during broken links or scanning attempts.

### 500 – Internal Server Error
- Server encountered an unexpected condition.
- Indicates possible backend failure or misconfiguration.

---

## Methodology

### 1. Started Packet Capture
- Opened Wireshark.
- Selected active network interface.
- Began capturing traffic.

### 2. Generated HTTP Traffic
- Accessed websites through a web browser.
- Submitted forms to generate POST requests.
- Observed normal browsing behavior.

### 3. Applied Display Filter
Used the following filter to isolate HTTP traffic:

http


### 4. Identified HTTP Requests
- Located GET, POST, and PUT methods in captured packets.
- Analyzed request headers and server responses.

### 5. Analyzed Response Codes
- Observed 200 responses for successful page loads.
- Triggered 404 errors by requesting non-existing pages.
- Observed 403 responses where access was restricted.
- Identified 500-level errors in server responses.

---

## Screenshots
Screenshots available in the `/screenshots` directory:
- HTTP GET request
- HTTP POST request
- HTTP response with 200 status
- HTTP 404 error response
- HTTP 500 response

---

## Findings
- HTTP methods clearly indicate client intent.
- Response codes provide immediate insight into request outcomes.
- Repeated 404 responses may indicate scanning activity.
- Multiple 403 responses may indicate unauthorized access attempts.
- 500-level errors may signal server misconfigurations or instability.

---

## SOC Use Cases

### 1. Incident Response
- Detect abnormal HTTP methods (unexpected PUT/DELETE).
- Identify repeated error codes during attack attempts.

### 2. Threat Hunting
- Hunt for repeated 404 errors (possible directory brute forcing).
- Identify unusual POST activity (possible data exfiltration).

### 3. Malware Analysis
- Detect suspicious HTTP requests to command-and-control servers.
- Analyze unusual outbound traffic patterns.

### 4. Web Application Monitoring
- Identify server misconfigurations via frequent 500 errors.
- Detect unauthorized access attempts (403 patterns).

---

## Lessons Learned
- HTTP analysis is critical for web-based threat detection.
- Response codes provide immediate context during investigations.
- Repeated client errors (404, 403) may indicate reconnaissance.
- Understanding HTTP behavior improves detection capability in a SOC environment.

---

## Next Steps
- Analyze HTTPS traffic and understand TLS handshake basics.
- Explore suspicious user-agent analysis.
- Study common web attack patterns (SQLi, XSS indicators in traffic).



