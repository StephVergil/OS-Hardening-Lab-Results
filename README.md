# OS Hardening Lab Results

This project documents the outcomes of an OS hardening lab, including password policy modifications, security benchmarks, and the results of password attack simulations. The lab emphasizes the importance of adhering to security policies and auditing practices to strengthen system defenses.

### Objectives
- Modify and analyze password policies for enhanced security.
- Evaluate the impact of security benchmarks and recommendations.
- Perform password attacks to understand vulnerabilities and defenses.
- Analyze logging and auditing practices to detect potential threats.

### Key Results
1. **Password Policy Changes**:
   - Enforce password history: 24 passwords remembered.
   - Maximum password age: 42 days.
   - Minimum password age: 1 day.
   - Minimum password length: 0 characters (for testing purposes).
   - Password complexity requirements: Disabled (for comparison purposes).
   - Store passwords using reversible encryption: Disabled.
   - LAN Manager hash value: Enabled to prevent storage on the next password change.
   - LAN Manager authentication level: Configured to send NTLMv2 responses only and refuse LM.

2. **Password Testing**:
   - **password**: Rejected due to policy enforcement of non-reusable passwords.
   - **ITSY1400!**: Accepted as it adhered to the policy requirements, including non-reuse within the last 24 passwords.

3. **Benchmark Insights**:
   - **Maximum Password Age**: Reduces the opportunity for attackers to exploit known credentials.
   - **Minimum Password Age**: Prevents users from cycling through passwords to reuse familiar ones.
   - **Audit Policies**: Enables detection and evidence collection for security incidents.
   - **Password Complexity**: Requires passwords to have at least six characters, three distinct character classes, and avoid user-related identifiers.

4. **Password Attack Simulations**:
   - **Basic Password Attack**: No passwords retrieved due to enhanced policy settings.
   - **Hybrid Password Attack**: No passwords retrieved.
   - **Full Password Attack**: Limited success due to enforced security measures, including disabling LAN Manager hash storage.

5. **Security Recommendations**:
   - Implement tight controls on password policies, including complexity and aging requirements.
   - Regularly review and update security benchmarks, such as CIS guidelines, to align with organizational needs.
   - Enable logging and auditing of critical events to identify and respond to potential breaches effectively.

### Project Resources
- **Project Link**: [OS Hardening Lab Results](https://github.com/StephVergil/OS-Hardening-Lab-Results/blob/main/OSHardeningLabResult.docx.pdf)
- [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks/)
- [Microsoft Security Guidance](https://docs.microsoft.com/en-us/windows/security/)

### Conclusion
This lab demonstrates the importance of robust password policies and adherence to security benchmarks in hardening operating systems. By implementing these measures and testing for vulnerabilities, organizations can significantly enhance their resilience against attacks.

### Disclaimer
This project was conducted in a controlled environment. Unauthorized use of these techniques or tools outside such an environment may violate ethical guidelines and legal regulations.
