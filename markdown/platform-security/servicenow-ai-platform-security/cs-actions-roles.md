---
title: Code Signing actions and required roles
description: Reference table of Code Signing actions, their descriptions, and the roles required to perform them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/cs-actions-roles.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: reference
last_updated: "2026-05-19"
reading_time_minutes: 3
keywords: [code signing, roles, permissions, actions, reference]
breadcrumb: [Administer and Troubleshoot, Code Signing, Platform Security]
---

# Code Signing actions and required roles

Reference table of Code Signing actions, their descriptions, and the roles required to perform them.

## Role-based access control

Code Signing uses role-based access control so that only authorized users can perform specific actions. The following table maps all Code Signing actions to their required roles.

Unless otherwise noted, all listed roles are required to perform the action.

## Role hierarchy

Code Signing includes three primary roles with different levels of access:

-   **codesigning\_admin**

    Highest level access. Can assign codesigning\_manager and codesigning\_auditor roles to other users and access all configuration features.

-   **codesigning\_manager**

    Operational access. Can create and update signature configurations and create and run Code Signing jobs.

-   **codesigning\_auditor**

    Read-only access. Can view signature configurations and signing jobs but can't create or modify them.


|Action|Description|Required roles|Instance type|
|------|-----------|--------------|-------------|
|Initial setup and configuration|
|Assign Code Signing administrator role|Grant the codesigning\_admin role to a user to access the Code Signing configuration experience|admin, security\_admin|Both|
|Configure Code Signing Enterprise on trusted instance|Activate and configure Code Signing on the trusted instance, including uploading customer signing and COT administration key pairs|admin, security\_admin, codesigning\_admin, sn\_kmf.cryptographic\_manager|Trusted|
|Upload Code Signing configuration file to protected instance|Import the configuration file generated on the trusted instance to the protected instance|admin, security\_admin, codesigning\_admin, sn\_kmf.cryptographic\_manager|Protected|
|Configure Code Signing Enterprise on protected instance|Activate and configure Code Signing on the protected instance, including uploading the runtime/notarization key pair|admin, security\_admin, codesigning\_admin, sn\_kmf.cryptographic\_manager|Protected|
|Turn on certificate validation|Protect the instance with certificate-based validation|codesigning\_admin, security\_admin, sn\_kmf.cryptographic\_manager|Both|
|Turn off Code Signing|Disable Code Signing on the protected instance|admin, codesigning\_admin|Both|
|Certificate management|
|Create Code Signing key pairs and certificates|Create two key pairs and signed certificates to establish trust between protected and trusted instances|sn\_kmf.cryptographic\_manager|Trusted|
|Export revocation request configuration|Start the certificate revocation process by selecting the certificate to revoke and exporting the configuration as an update set|sn\_cse.codesigning\_admin, sn\_cse.quorum\_requester, security\_admin|Trusted|
|Import revocation request configuration|Import the update set into the protected instance to initiate the certificate revocation approval workflow|sn\_cse.codesigning\_admin, sn\_cse.quorum\_requester, security\_admin|Protected|
|Approve certificate revocation|Review and approve certificate revocation requests from email approval notifications|sn\_cse.codesigning\_admin, approver\_user|Protected|
|Signing operations|
|Sign update sets|Sign records that match a signature configuration in an update set and add signature records and verification certificates|codesigning\_admin|Trusted|
|Mass sign records|Sign all records that match a signature configuration applied on a specific metadata table|codesigning\_admin|Trusted|
|Mass sign attachments|Sign all attachment records attached to a table that matches a specified signature configuration|codesigning\_admin|Trusted|
|Sign existing flows, subflows, and actions|Sign and validate existing flows, subflows, and actions by using update sets|codesigning\_admin,sn\_kmf.cryptographic\_manager|Trusted|
|Sign new flows, subflows, and actions|Sign and validate new flows, subflows, and actions by using update sets|codesigning\_admin,sn\_kmf.cryptographic\_manager|Trusted|
|Sign specific records or attachments|Create a security job to sign specific records or attachments rather than all records or attachments on a table|security\_admin or sn\_kmf.cryptographic\_manager|Trusted|
|Advanced configuration|
|Specify custom rules in ECC firewall|Configure the External Communication Channel \(ECC\) firewall in the MID Server by specifying custom rules to selectively allow or reject incoming messages|security\_admin|Protected|
|Migrate signatures to customer certificate|Run a signing job to migrate signatures to a customer Root of Trust \(ROT\)|admin, security\_admin, sn\_kmf.cryptographic\_manager|Both|
|Disable ServiceNow Root of Trust|Run a scheduled job on the trusted instance to disable the ServiceNow Root of Trust|admin, security\_admin, sn\_kmf.cryptographic\_manager|Both|
|Use standalone signing tool|Use the standalone Signing Tool to sign supported records in ServiceNow applications using a private key|admin|Trusted|
|Monitoring and administration|
|View Code Signing Health and Status Dashboard|Monitor overall Code Signing system health, configuration, and status|codesigning\_admin, codesigning\_manager, codesigning\_auditor|Both|
|View signature verification status|View the status of valid, invalid, and orphan signatures across applications|codesigning\_admin, codesigning\_manager, codesigning\_auditor|Both|
|View Key Pair and Certificates dashboard|Monitor certificate status, expiration dates, and validity for Code Signing certificates|codesigning\_admin, codesigning\_manager, codesigning\_auditor|Both|
|View Code Signing configuration dashboard|Monitor system properties and key settings that control Code Signing|codesigning\_admin, codesigning\_manager, codesigning\_auditor|Both|
|View MID Server configuration dashboard|Manage and configure trust relationships and certificate settings for MID Servers|codesigning\_admin, codesigning\_manager, codesigning\_auditor|Both|
|Access Code Signing logs|Access logs to troubleshoot and identify Code Signing failure reasons|codesigning\_admin, codesigning\_manager, codesigning\_auditor|Both|

**Parent Topic:**[Code Signing reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/code-signing-reference.md)

