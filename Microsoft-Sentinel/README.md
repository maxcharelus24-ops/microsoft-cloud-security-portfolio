
# Microsoft Sentinel - Security Monitoring & Threat Detection

## Project Objective

Demonstrate security monitoring, threat detection, and incident investigation using Microsoft Sentinel in a controlled Azure lab environment.

## Technologies Used

- Microsoft Sentinel
- Azure Log Analytics
- Microsoft Entra ID
- Kusto Query Language (KQL)
- Sentinel Analytics Rules
- Security Incidents

## Project Scope

This project documents hands-on experience with:

1. Configuring a Microsoft Sentinel workspace
2. Connecting identity-related log sources
3. Investigating security events using KQL
4. Creating analytics rules for suspicious activity
5. Reviewing and managing security incidents
6. Configuring incident automation

## Validation

Configuration screenshots and available investigation results will be used to document the implementation and observed outcomes.


## Configuration and Investigation Evidence

The following screenshots document Microsoft Sentinel security monitoring and threat detection activities performed in the BlueCore Security lab environment.

### 1. Security Incidents

The incident dashboard shows security alerts generated from scheduled detection rules, including privileged role activity, multiple failed login attempts, and brute-force detection.

![Microsoft Sentinel Security Incidents](screenshots/sentinel-security-incidents.png)

### 2. Analytics Rules

Configured scheduled analytics rules for:
- Privileged role activity detection
- Impossible travel sign-ins
- Multiple failed login attempts

The screenshot shows three enabled analytics rules.

![Microsoft Sentinel Analytics Rules](screenshots/sentinel-analytics-rules.png)

### 3. Sign-in Event Investigation

Reviewed Microsoft Entra ID authentication events, including failed sign-ins, result codes, application details, and event timestamps.

![Microsoft Sentinel Sign-in Investigation](screenshots/sentinel-signin-investigation.png)

### 4. Log Analytics and Security Monitoring

Used Microsoft Sentinel Logs to examine authentication activity collected from Microsoft Entra ID.

The results show successful and failed sign-in events that can support identity threat investigations.

![Microsoft Sentinel Log Analytics](screenshots/sentinel-log-analytics.png)

## Evidence and Validation Notes

These screenshots capture historical lab configurations and observed results. They demonstrate analytics rule configuration, incident generation, and authentication log visibility.

They do not establish the current deployment status of the workspace or rules.

