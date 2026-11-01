# Microsoft Purview DLP – Confidential Data Protection Lab

## Project Overview

This hands-on lab demonstrates the implementation and validation of Microsoft Purview Data Loss Prevention (DLP) controls in a Microsoft 365 test environment.

The objective was to identify confidential business records, prevent unauthorized external sharing through Exchange Online, and investigate policy violations using Microsoft Purview.

## Technologies Used

- Microsoft Purview Data Loss Prevention
- Microsoft 365 and Exchange Online
- Custom Sensitive Information Types (SITs)
- DLP Policy Simulation and Enforcement
- DLP Alerts and Investigation

## Lab Objectives

1. Create a custom sensitive information type to identify confidential business records.
2. Configure a DLP policy with advanced conditions and protective actions.
3. Test the policy in simulation mode before enforcement.
4. Prevent confidential records from being emailed to external recipients.
5. Validate DLP detection, blocking, and administrative alerting.

## Implementation

### 1. Custom Sensitive Information Type

Created a custom sensitive information type named **BlueCore Confidential Record Identifier** to detect synthetic confidential record identifiers used in the lab.

### 2. DLP Policy Configuration

Created a policy named **BlueCore Confidential Data Protection** with an advanced rule called **Block External Sharing of BlueCore Confidential Records**.

The rule was configured to:

- Detect the custom sensitive information type at high confidence.
- Evaluate email messages and attachments.
- Identify content shared with people outside the organization.
- Restrict external access when the conditions are met.
- Generate administrative alerts for policy matches.

The policy was scoped to Exchange Online for the tested scenario.

### 3. Simulation and Validation

Initially deployed the DLP policy in simulation mode to evaluate matches without enforcing restrictions.

Sent a test email containing a synthetic confidential record identifier to an external recipient.

Microsoft Purview successfully identified the test email and reported **one policy match** in the simulation results.

### 4. Policy Enforcement

After confirming successful detection, enabled the DLP policy and verified that policy synchronization completed.

Repeated the external-sharing test using a synthetic confidential record identifier.

Exchange Online blocked delivery and returned a nondelivery notification indicating that an organizational policy prevented the message from being sent.

### 5. Alert Investigation

Reviewed the generated DLP alert in Microsoft Purview.

Confirmed that the alert was associated with the **BlueCore Confidential Data Protection** policy and the external-sharing enforcement test.

The alert appeared with an active status and low severity.

## Results

| Validation Test | Result |
|---|---|
| Custom sensitive information type configured | Successful |
| Advanced DLP rule created | Successful |
| Simulation detected confidential content | 1 confirmed match |
| Policy enabled and synchronized | Successful |
| External email containing test identifier | Blocked |
| DLP administrative alert generated | Successful |
| Microsoft Defender incident correlation | Not verified |

## Security Concepts Demonstrated

- Data classification and sensitive information detection
- Data Loss Prevention policy design
- External data exfiltration prevention
- Simulation-first security control deployment
- Microsoft 365 email security enforcement
- Security alert monitoring and investigation

## Conclusion

This lab demonstrates a practical approach to protecting confidential information in Microsoft 365 using Microsoft Purview DLP.

By combining custom data classification, advanced policy conditions, simulation testing, enforcement, and alert investigation, the project validates the ability to configure and test controls designed to reduce unauthorized disclosure of sensitive business information.

**Environment:** Personal Microsoft 365 security lab using synthetic test data. No production or client information was used.


## Lab Evidence & Screenshots

The following screenshots document the implementation, testing, and enforcement of the BlueCore Confidential Data Protection policy in a Microsoft 365 test environment.

### 1. Custom Sensitive Information Type Detection
Created and validated a custom sensitive information type (SIT) to identify confidential BlueCore record identifiers.

![Custom SIT Detection](images/01-Custom-SIT-Detection.png)

### 2. DLP Policy Configuration
Configured the BlueCore Confidential Data Protection policy for Exchange Online, initially using simulation mode to evaluate policy matches.

![DLP Policy Configuration](images/02-DLP-Policy-Configuration.png)

### 3. DLP Policy Creation
Successfully created the custom DLP policy in Microsoft Purview.

![DLP Policy Created](images/03-DLP-Policy-Created.png)

### 4. DLP Simulation Results
Validated that the policy detected a matching Exchange Online email during simulation.

![DLP Simulation First Match](images/04-DLP-Simulation-First-Match.png)

### 5. Sensitive Information Match Details
Reviewed the matching email, triggered DLP rule, and custom sensitive information type detection results.

![DLP Simulation Match Details](images/05-DLP-Simulation-Match-Details.png)

### 6. DLP Alert Investigation
Reviewed the DLP alert generated for an email containing the confidential record identifier.

![DLP Security Alert](images/06-DLP-Security-Alert.png)

### 7. External Email Blocking Validation
Validated DLP enforcement by attempting to send a confidential record identifier externally. Exchange Online rejected the message due to the organization's DLP policy.

![External Email Blocked](images/07-DLP-External-Email-Blocked.png)

## Lab Outcome

Successfully demonstrated the Microsoft Purview DLP lifecycle: custom sensitive information identification, policy configuration, simulation testing, match investigation, alert generation, and enforcement of external email restrictions.
