# Security Testing

## 1. **Scope Setup / Defination**

   - [ ] Set up proxy, target scope, and other configurations,if required.

## 2. **Authentication and Authorization**

   - [ ] Identify API authentication mechanisms.
     - [ ] Test for weak authentication (e.g., default credentials, weak password policies).
     - [ ] Verify token-based authentication (JWT, OAuth) for vulnerabilities.
   - [ ] Test authorization controls.
     - [ ] Perform role-based access testing.
     - [ ] Check for missing or ineffective access controls.
     - [ ] Test for horizontal and vertical privilege escalation.

## 3. **Input Validation and Injection**

   - [ ] Test for injection vulnerabilities.
     - [ ] SQL injection, NoSQL injection, OS command injection, etc.
   - [ ] Validate input handling.
     - [ ] Special characters, encoding, and unexpected input.
   - [ ] Check for parameter tampering and manipulation.

## 4. **SSL/TLS Testing**

   - [ ] Ensure API communications are encrypted using HTTPS.
   - [ ] Verify secure SSL/TLS configurations.
     - [ ] Strong ciphers, secure protocols, and proper certificate validation.

## 5. **Data Exposure**

   - [ ] Test for sensitive information exposure in API responses.
     - [ ] Personally Identifiable Information (PII), API keys, sensitive data.
   - [ ] Review error handling for information leakage.
   - [ ] Ensure proper data redaction in logs and responses.

## 6. **Rate Limiting and Throttling**

   - [ ] Test for rate limiting and throttling mechanisms.
   - [ ] Verify if rate limits are enforced correctly.

## 7. **Cross-Site Scripting (XSS) and Cross-Site Request Forgery (CSRF)**

   - [ ] Test for XSS vulnerabilities in API responses.
   - [ ] Verify proper input validation to prevent XSS.
   - [ ] Check for CSRF vulnerabilities.
   - [ ] Verify the effectiveness of anti-CSRF tokens.

## 8. **Security Headers**

   - [ ] Check for the presence of security headers.
         Examples: `Strict-Transport-Security`, `Content-Security-Policy`.
   - [ ] Ensure proper configuration and strict security policies.

## 9. **Logging and Monitoring**

   - [ ] Verify API logs for security-relevant events.
   - [ ] Monitor logs for abnormal activities or potential security incidents.
   - [ ] Ensure logs do not expose sensitive information.

## 10. **File Uploads and Downloads**

   - [ ] Test security of file uploads.
   - [ ] File type validation 
   - [ ] size limits and proper handling (renaming etx).
   - [ ] Check for security issues related to file downloads.

## 11. **Error Handling**

   - [ ] Test how the API handles unexpected input and errors.
   - [ ] Verify that error messages do not leak sensitive information.
   - [ ] Ensure proper HTTP status codes are returned.

## 12. **Business Logic Testing**

   - [ ] Test for logical flaws or vulnerabilities in the API business logic.

## 13. **Client-Side Security**

   - [ ] Assess client-side security controls.
     - [ ] Verify if sensitive information is stored securely.
     - [ ] Test for insecure client-side storage (localStorage, sessionStorage).

## 14. **Error Handling**

   - [ ] Test how the appication handles unexpected input and errors.
   - [ ] Verify that error messages do not leak sensitive information.
   - [ ] Ensure proper HTTP status codes are returned.

## 15. **UI Redirection and Clickjacking**

   - [ ] Test for open redirects.
   - [ ] Verify clickjacking protection.
     - [ ] X-Frame-Options header.

## 16. **Mobile Responsiveness**

   - [ ] Test UI on various devices and screen sizes.
   - [ ] Ensure mobile UIs adhere to security best practices.



# FTP Security Testing Checklist

## 1. **Initial Setup and Configuration**

   - [ ] Identify FTP server details (hostname, port).
   - [ ] Verify the FTP server software and version.
   - [ ] Determine if anonymous FTP access is allowed.
   - [ ] Check for secure FTP configurations (FTPS or SFTP).

## 2. **Authentication and Authorization**

   - [ ] Test for weak authentication mechanisms.
     - [ ] Ensure strong passwords and authentication policies.
   - [ ] Verify user access controls and permissions.
     - [ ] Test for unauthorized access to sensitive directories.

## 3. **Secure Data Transmission**

   - [ ] Check if FTP connections use encryption.
     - [ ] Verify FTPS (FTP Secure) or SFTP (SSH File Transfer Protocol) is enforced.
     - [ ] Ensure secure ciphers and protocols are used.

## 4. **Anonymous FTP Access**

   - [ ] Test for anonymous FTP access.
     - [ ] Ensure that anonymous access is restricted.
     - [ ] Check for read-only permissions for anonymous users.

## 5. **FTP Banner Grabbing**

   - [ ] Identify the FTP server banner.
     - [ ] Verify that sensitive information is not disclosed in the banner.
     - [ ] Check if banner grabbing can reveal version information.

## 6. **FTP Commands Testing**

   - [ ] Test for FTP command injection vulnerabilities.
     - [ ] Verify proper input validation and handling of FTP commands.
   - [ ] Check for FTP-specific vulnerabilities (e.g., CVE-2010-4221).

## 7. **Directory Traversal and Path Manipulation**

   - [ ] Test for directory traversal vulnerabilities.
     - [ ] Attempt to navigate to unauthorized directories.
     - [ ] Check if path manipulation is properly validated.

## 8. **Brute Force Attacks**

   - [ ] Test for weak or easily guessable credentials.
     - [ ] Perform brute force attacks on FTP credentials.
     - [ ] Implement account lockout mechanisms to prevent brute force.

## 9. **FTP User Enumeration**

   - [ ] Test for FTP user enumeration vulnerabilities.
     - [ ] Verify that the server does not reveal valid user information.
     - [ ] Check if failed login attempts do not disclose valid usernames.

## 10. **Logging and Monitoring**

   - [ ] Verify that FTP server logs capture security-relevant events.
   - [ ] Monitor logs for unusual or suspicious activities.
   - [ ] Ensure logs do not expose sensitive information.

## 11. **FTP Firewall and Network Security**

   - [ ] Test for FTP firewall configurations.
     - [ ] Ensure that only necessary ports are open.
     - [ ] Verify proper network segmentation for FTP traffic.

## 12. **FTP Client Security**

   - [ ] Test security configurations of FTP clients.
     - [ ] Ensure FTP clients use secure connections (FTPS or SFTP).
     - [ ] Verify client configurations for secure data transmission.

## 13. **Secure File Transfers**

   - [ ] Verify secure file transfer configurations.
     - [ ] Check for secure file permissions and ownership.
     - [ ] Test for secure file uploads and downloads.

## 14. **Active vs. Passive FTP Testing**

   - [ ] Test for both active and passive FTP modes.
     - [ ] Ensure that firewall configurations support both modes securely.
     - [ ] Verify that the FTP server does not have unnecessary open ports.

