# OS Hardening Lab Results

## Overview

This project presents the outcomes of an Operating System (OS) hardening lab aimed at fortifying system defenses by implementing robust password policies, analyzing security benchmarks, and simulating password attack scenarios. The lab emphasizes the importance of applying best practices for security configuration, auditing, and proactive defense mechanisms to mitigate potential vulnerabilities.

---

## Objectives

- **Policy Implementation**: Configure and evaluate secure password policies to enhance system protection.
- **Benchmark Evaluation**: Align configurations with recognized security benchmarks like CIS guidelines.
- **Attack Simulation**: Conduct password attack simulations to understand weaknesses and validate defenses.
- **Logging and Auditing**: Review logging mechanisms to identify threats and enable effective incident response.

---

## Key Results

### 1. **Password Policy Implementation**
- **Password History Enforcement**: Prevent reuse of the last 24 passwords.
- **Maximum Password Age**: Set to 42 days, requiring regular password updates to limit exploitation time.
- **Minimum Password Age**: Set to 1 day to prevent users from cycling through passwords quickly.
- **Password Length**: Configured as 0 characters for testing purposes but should align with an organizational minimum (e.g., 8 characters or more in production).
- **Password Complexity**: Temporarily disabled for comparison but is typically required to enforce a mix of character types (uppercase, lowercase, digits, special characters).
- **Reversible Encryption**: Disabled to avoid plaintext password storage.
- **LAN Manager (LM) Hash Storage**: Disabled to prevent storage of weak, outdated hash formats.
- **LAN Manager Authentication**: Configured to enforce NTLMv2 responses and refuse LM authentication, enhancing protocol security.

---

### 2. **Password Testing Results**
- **Weak Password Example**: `password` was rejected due to policies preventing password reuse and failing complexity standards.
- **Strong Password Example**: `ITSY1400!` met policy requirements for length and previous password restrictions, demonstrating adherence to secure standards.

---

### 3. **Insights from Security Benchmarks**
- **Password Expiry Policies**:
  - Regular password changes (maximum age: 42 days) reduce risks of long-term credential exposure.
- **Password Complexity**:
  - When enabled, this policy ensures robust password composition, including three or more character categories.
- **Audit Policy**:
  - Configuring auditing ensures detailed logging of successful and failed logins, privilege escalations, and configuration changes for proactive threat detection and investigation.
- **LAN Manager and NTLMv2**:
  - Disabling LM hash storage and requiring NTLMv2 strengthens protection against brute-force and downgrade attacks.

---

### 4. **Password Attack Simulations**
- **Basic Dictionary Attack**:
  - No passwords were retrieved due to policy configurations and the lack of weak passwords in the system.
- **Hybrid Attack**:
  - Combined dictionary and rule-based attacks yielded no results, highlighting the effectiveness of secure configurations.
- **Full Brute-Force Attack**:
  - The system successfully resisted brute-force attempts, with critical defenses provided by NTLMv2 enforcement and disabled LM hashes.

---

## Security Recommendations

1. **Password Policy Enhancements**:
   - Ensure minimum length requirements of at least 12 characters with complexity enforcement enabled.
   - Configure password expiration and history policies to prevent reuse and long-term exposure.
   
2. **Audit and Logging Configuration**:
   - Enable logging for account logon events, privilege escalations, and access attempts.
   - Regularly review audit logs to detect suspicious activity and identify potential breaches.

3. **User Training and Awareness**:
   - Educate users on the importance of creating strong, unique passwords and avoiding credential reuse.
   - Provide guidance on recognizing phishing attempts that target credentials.

4. **Benchmark Alignment**:
   - Conduct regular audits against the CIS Benchmarks and other industry standards to ensure continued compliance and security improvements.

5. **Advanced Threat Mitigation**:
   - Consider multi-factor authentication (MFA) for critical systems to add an additional layer of defense.
   - Regularly test systems with simulated attacks to ensure security controls remain effective.

---

## Practical Applications

- **Enterprise Security Policies**:
  - Implement password and audit policies across organizational systems to achieve compliance with regulatory requirements.
- **Proactive Threat Management**:
  - Regularly evaluate the effectiveness of defenses by simulating attacks and aligning practices with evolving threats.
- **Forensic Readiness**:
  - Maintain robust logging mechanisms to collect evidence, enabling efficient incident response and post-attack analysis.

---

## Project Resources

1. [OS Hardening Lab Results](https://github.com/StephVergil/OS-Hardening-Lab-Results/blob/main/OSHardeningLabResult.docx.pdf)
2. **CIS Benchmarks**:
   - [CIS Security Benchmarks](https://www.cisecurity.org/cis-benchmarks/)
3. **Microsoft Security Documentation**:
   - [Windows Security Guidance](https://learn.microsoft.com/en-us/windows/security/)
4. **Password Security Best Practices**:
   - [NIST SP 800-63B](https://pages.nist.gov/800-63-3/sp800-63b.html)

---

## Conclusion

The OS hardening lab demonstrates how implementing robust password policies and aligning with security benchmarks can effectively reduce vulnerabilities. By conducting controlled attack simulations, the lab validates the importance of proactive defense measures and highlights areas for further improvement, such as adopting multi-factor authentication and conducting regular security audits.

---

## Disclaimer

This project was conducted in a controlled lab environment for educational purposes. Unauthorized use of the described tools or techniques outside such an environment may violate ethical guidelines and legal regulations. Always adhere to applicable laws and organizational security policies.

---
