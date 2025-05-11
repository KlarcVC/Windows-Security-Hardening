# Windows-Security-Hardening

Project Summary

This project documents the process of hardening a Windows 10 virtual machine using CIS Benchmarks and best practices. The goal was to enhance system security, reduce the attack surface, and simulate real-world endpoint protection for Blue Team operations.

Objectives

Reduce attack surface of Windows 10

Apply CIS Benchmark recommendations

Strengthen firewall and antivirus configurations

Test compliance using CIS-CAT Lite

Environment

Host OS: Windows/Linux/macOS

Virtualization: Oracle VirtualBox

Guest OS: Windows 10 Pro (x64)

Steps Taken

1. Create Standard User Account

Created a non-administrative user to use for daily tasks.

Disabled the built-in Administrator account.

2. Enable BitLocker Encryption

Enabled BitLocker to encrypt the system drive using TPM.

Backed up the recovery key to a secure location.

3. Harden Microsoft Defender Antivirus

Verified real-time protection is enabled.

Set Defender updates to automatic.

Configured scans and cloud-delivered protection.

4. Configure Windows Firewall

Enabled firewall for all profiles (Domain, Private, Public).

Created custom inbound/outbound rules to limit traffic.

Blocked legacy and unused ports/services (e.g., Telnet, SMBv1).

5. Disable Insecure Services

Disabled unnecessary services via services.msc, including:

Remote Registry

Telnet

SMBv1 (via Windows Features and registry)

6. Apply Group Policy Settings

Used gpedit.msc to set policies, such as:

Account lockout policies

Audit policies

User rights assignment

7. Install and Run CIS-CAT Lite

Downloaded CIS-CAT Lite from Center for Internet Security.

Ran an initial assessment and recorded the score.

Made remediations according to CIS Windows 10 Benchmark v1.12.

Re-ran the tool to verify improvements.

8. Final Security Checks

Verified all accounts and services.

Ran a full antivirus scan.

Confirmed no open risky ports using netstat.

Tools Used

Oracle VirtualBox

Microsoft Defender

Group Policy Editor

CIS-CAT Lite

PowerShell / Command Prompt

Outcome

The final CIS-CAT report showed improved compliance from an initial baseline. The VM now follows key endpoint protection practices, making it resilient against common threats.

Screenshots

(Add your screenshots here to show progress and settings)

Next Steps

Integrate Sysmon for event monitoring

Forward logs to Wazuh or Splunk for SIEM visibility

Explore automated hardening with PowerShell scripts

License

This project is for educational purposes. No warranties implied.

Author: Klarc ClarabalDate: May 2025Location: Montreal, QC
