# Microsoft Entra ID Security – Conditional Access & MFA

## Project Objective

Implement and validate Microsoft Entra ID Conditional Access policies to strengthen identity security, enforce multi-factor authentication (MFA), and restrict unauthorized access.

This lab demonstrates how Conditional Access can reduce identity-based security risks while maintaining emergency administrative access.

## Conditional Access Policies Configured

### Policy 1: Require Multi-Factor Authentication (MFA)
- Configured Conditional Access to require MFA for users.
- Excluded emergency access (break-glass) accounts to prevent administrative lockout.

### Policy 2: Restrict Access by Geographic Location
- Configured location-based Conditional Access restrictions.
- Blocked sign-ins originating outside the United States.
- Used named locations to define geographic access boundaries.

## Policy Validation

Conditional Access policies can be validated using Microsoft Entra ID sign-in logs and the Conditional Access What If tool.

Validation checks include:
- Confirming MFA requirements apply to targeted users.
- Verifying emergency access accounts are excluded.
- Reviewing location-based access restrictions.
- Checking sign-in logs for policy evaluation results.
