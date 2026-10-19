
# Microsoft Intune Endpoint Security & Device Management

## Project Objective

Configure and manage Windows endpoints using Microsoft Intune to strengthen endpoint security, enforce device compliance, and automate application deployments.

This project demonstrates hands-on experience with Microsoft Intune in a controlled lab environment.

## Technologies Used

- Microsoft Intune
- Microsoft Entra ID
- Windows 10/11
- Microsoft Defender Antivirus
- BitLocker Drive Encryption
- Microsoft 365 Apps

## Areas of Focus

### 1. Device Enrollment
- Entra ID device registration and enrollment
- Windows device management through Intune
- Device inventory and management status

### 2. Device Compliance
- Windows compliance policies
- Device compliance evaluation
- Identification and troubleshooting of non-compliant devices

### 3. Endpoint Security
- BitLocker encryption policies
- Microsoft Defender Antivirus configurations
- Endpoint security baselines and protection settings

### 4. Application Management
- Microsoft 365 Apps deployment
- Microsoft Edge deployment
- Application assignment and installation monitoring

## Validation

Configuration screenshots and observed results will document enrollment, compliance, endpoint protection, and application deployment status.

## Lab Environment

This project documents work performed in a controlled Microsoft Intune lab environment. Policy states and validation results will be described based on the available evidence.


## Configured Endpoint Security Policies

The following policies were created in Microsoft Intune and assigned to the SG-Test-Users pilot group.

### 1. Windows 11 Device Compliance

**Policy:** BCS-WIN11-Device-Compliance

Configured compliance requirements for:
- BitLocker encryption
- Minimum Windows version 10.0.22000.0
- Device encryption
- Firewall and antivirus protection
- Microsoft Defender Antimalware

![Windows 11 Device Compliance Policy](screenshots/intune-device-compliance-policy.png)

### 2. BitLocker Drive Encryption

**Policy:** BCS-WIN11-BitLocker-Encryption

Configured device encryption requirements, XTS-AES 128-bit encryption, and operating system drive recovery options.

The lab VM was independently verified as encrypted, with BitLocker protection enabled and its recovery key backed up to Microsoft Entra ID.

![BitLocker Encryption Policy](screenshots/intune-bitlocker-encryption-policy.png)

### 3. Microsoft Defender Antivirus

**Policy:** BCS-WIN11-Defender-Antivirus

Configured antivirus protection settings including:
- Real-time protection
- Cloud-delivered protection
- Behavior monitoring
- Script and archive scanning
- Potentially unwanted application protection
- Scheduled quick scans
- Network protection

![Microsoft Defender Antivirus Policy](screenshots/intune-defender-antivirus-policy.png)

## Deployment and Validation Status

All three Intune policies were created and assigned to the SG-Test-Users pilot group.

The existing lab VM retained its Microsoft Entra join and BitLocker encryption, but its previous Intune enrollment was no longer functioning correctly. Therefore, successful policy deployment and device compliance evaluation have not been verified.

The screenshots document policy configuration and assignment, not confirmed enforcement on managed endpoints.


