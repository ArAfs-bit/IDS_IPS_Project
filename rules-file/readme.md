# Rules Directory

This directory contains various rule files used by Suricata to detect and respond to different types of network traffic.

## Contents

### 1. `custom.rules`
- **Description**: User-defined custom rules tailored to detect specific threats or anomalies in network traffic.

### 2. `files.rules`
- **Description**: Defines rules for detecting specific file types transmitted over the network (e.g., .jpg, .pdf). Alerts on certain file extensions.

### 3. `ftp-events.rules`
- **Description**: Rules for monitoring and alerting on FTP traffic to detect unauthorized file transfers or commands that may indicate an attack.

### 4. `http-events.rules`
- **Description**: Holds rules for detecting anomalies or suspicious behavior in HTTP traffic, including potential SQL injection attempts and malformed requests.

### 5. `http2-events.rules`
- **Description**: Tailored for detecting issues in HTTP/2 traffic, addressing specific characteristics of that protocol.

### 6. `smtp-events.rules`
- **Description**: Monitors SMTP traffic for suspicious email activities, such as potential phishing attempts or unauthorized access.

### 7. `ssh-events.rules`
- **Description**: Detects suspicious activities or unauthorized access attempts over SSH, providing alerts for potential brute-force attacks or other malicious behaviors.

### 8. `dns-events.rules`
- **Description**: Includes rules that monitor DNS traffic for unusual queries or requests that may indicate malicious activity, such as lookups for known bad domains.

## Example Rules

### Custom Rules
```plaintext
# Custom rules for detecting specific file types
alert http any any -> any any (msg:"Detected JPG file"; fileext:"jpg"; sid:1000001; rev:1;)
alert http any any -> any any (msg:"Detected PDF file"; fileext:"pdf"; sid:1000002; rev:1;)

