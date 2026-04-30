---
title: Azure policies
description: The Cloud Configuration Governance AWS policies are listed for your reference.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Azure policies

The Cloud Configuration Governance AWS policies are listed for your reference.

<table id="table_ify_b3v_t2c"><thead><tr><th>

Policy Set

</th><th>

Policy Name

</th><th>

Resource Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

Azure VM HardwareType

</td><td>

Condition builder

</td><td>

Policy to check if the deployed Azure VMs are using only the approved hardware types.

</td></tr><tr><td>

 

</td><td>

Azure VM IP Address

</td><td>

Script

</td><td>

Policy to check if the IP address of the Azure VM is matching with the CMDB record.

</td></tr><tr><td>

 

</td><td>

Azure VM Monitoring State

</td><td>

Condition builder

</td><td>

Policy to check if detailed monitoring is enabled for the Azure VM.

</td></tr><tr><td>

Azure: Security Center Configuration

</td><td>

Ensure That Auto provisioning of 'Log Analytics agent for Azure VMs' is Set to 'On' \(Automated\)

</td><td>

Azure Subscription

</td><td>

Enable automatic provisioning of the monitoring agent to collect security data.

 When 'Log Analytics agent for Azure VMs' is turned on, Microsoft Defender for Cloud provisions the Microsoft Monitoring Agent on all existing supported Azure virtual machines and any new ones that are created. The Microsoft Monitoring Agent scans for various security-related configurations and events such as system updates, OS vulnerabilities, endpoint protection, and provides alerts.

</td></tr><tr><td>

Azure: Security Center Configuration

</td><td>

Ensure 'Additional email addresses' is Configured with a Security Contact Email \(Automated\)

</td><td>

Azure Subscription

</td><td>

Microsoft Defender for Cloud emails the subscription owners whenever a high-severity alert is triggered for their subscription. You should provide a security contact email address as an additional email address.

 Microsoft Defender for Cloud emails the Subscription Owner to notify them about security alerts. Adding your Security Contact's email address to the 'Additional email addresses' field ensures that your organization's Security Team is included in these alerts. This ensures that the proper people are aware of any potential compromise in order to mitigate the risk in a timely fashion.

</td></tr><tr><td>

Azure: Security Center Configuration

</td><td>

Ensure That 'Notify about alerts with the following severity' is Set to 'High' \(Automated\)

</td><td>

Azure Subscription

</td><td>

Enables emailing security alerts to the subscription owner or other designated security contact.

 Enabling security alert emails ensures that security alert emails are received from Microsoft. This ensures that the right people are aware of any potential security issues and are able to mitigate the risk.

</td></tr><tr><td>

Azure: Security Center Configuration

</td><td>

Ensure That 'All users with the following roles' is set to 'Owner' \(Automated\)

</td><td>

Azure Subscription

</td><td>

Enable security alert emails to subscription owners.

 Enabling security alert emails to subscription owners ensures that they receive security alert emails from Microsoft. This ensures that they are aware of any potential security issues and can mitigate the risk in a timely fashion.

</td></tr><tr><td>

Azure: Storage Security

</td><td>

Ensure Storage logging is Enabled for Blob Service for 'Read', 'Write', and 'Delete' requests \(Automated\)

</td><td>

Microsoft.Storage/StorageAccounts

</td><td>

The Storage Blob service provides scalable, cost-efficient objective storage in the cloud.

 Storage Logging happens server-side and allows details for both successful and failed requests to be recorded in the storage account. These logs allow users to see the details of read, write, and delete operations against the blobs. Storage Logging log entries contain the following information about individual requests: Timing information such as start time, end-to-end latency, and server latency, authentication details, concurrency information and the sizes of the request and response messages.

 Storage Analytics logs contain detailed information about successful and failed requests to a storage service. This information can be used to monitor each individual request to a storage service for increased security or diagnostics. Requests are logged on a best-effort basis. Storage Analytics logging is not enabled by default for your storage account.

</td></tr><tr><td>

Azure: Storage Security

</td><td>

Ensure Storage Logging is Enabled for Table Service for 'Read', 'Write', and 'Delete' Requests \(Automated\)

</td><td>

Microsoft.Storage/StorageAccounts

</td><td>

The Storage Table storage is a service that stores structure NoSQL data in the cloud, providing a key/attribute store with a schema less design. Storage Logging happens server-side and allows details for both successful and failed requests to be recorded in the storage account. These logs allow users to see the details of read, write, and delete operations against the tables. Storage Logging log entries contain the following information about individual requests: Timing information such as start time, end-to-end latency, and server latency, authentication details, concurrency information and the sizes of the request and response messages.

 Storage Analytics logs contain detailed information about successful and failed requests to a storage service. This information can be used to monitor each individual request to a storage service for increased security or diagnostics. Requests are logged on a best-effort basis. Storage Analytics logging is not enabled by default for your storage account.

</td></tr><tr><td>

Azure: Storage Security

</td><td>

Ensure Storage Logging is Enabled for Queue Service for 'Read', 'Write', and 'Delete' requests \(Automated\)

</td><td>

Microsoft.Storage/StorageAccounts

</td><td>

The Storage Queue service stores messages that may be read by any client who has access to the storage account. A queue can contain an unlimited number of messages, each of which can be up to 64KB in size using version 2011-08-18 or newer. Storage Logging happens server-side and allows details for both successful and failed requests to be recorded in the storage account. These logs allow users to see the details of read, write, and delete operations against the queues. Storage Logging log entries contain the following information about individual requests: Timing information such as start time, end-to-end latency, and server latency, authentication details, concurrency information and the sizes of the request and response messages.

 Storage Analytics logs contain detailed information about successful and failed requests to a storage service. This information can be used to monitor individual request and to diagnose issues with a storage service. Requests are logged on a best-effort basis.Storage Analytics logging is not enabled by default for your storage account.

</td></tr><tr><td>

Azure: SQL Security

</td><td>

Ensure that Vulnerability Assessment \(VA\) is enabled on a SQL server by setting a Storage Account \(Automated\)

</td><td>

Microsoft.Sql/servers

</td><td>

Enable Vulnerability Assessment \(VA\) service scans for critical SQL servers and corresponding SQL databases.

</td></tr><tr><td>

Azure: SQL Security

</td><td>

Ensure that VA setting 'Periodic recurring scans' to 'on' for each SQL server \(Automated\)

</td><td>

Microsoft.Sql/servers

</td><td>

Enable Vulnerability Assessment \(VA\) Periodic recurring scans for critical SQL servers and corresponding SQL databases.

</td></tr><tr><td>

Azure: SQL Security

</td><td>

Ensure that VA setting 'Send scan reports to' is configured for a SQL server \(Automated\)

</td><td>

Microsoft.Sql/servers

</td><td>

Configure 'Send scan reports to' with email IDs of concerned data owners/stakeholders for a critical SQL servers.

</td></tr><tr><td>

Azure: SQL Security

</td><td>

Ensure that Vulnerability Assessment Setting 'Also send email notifications to admins and subscription owners' is Set for

</td><td>

Microsoft.Sql/servers

</td><td>

Enable Vulnerability Assessment \(VA\) setting 'Also send email notifications to admins and subscription owners'.

</td></tr><tr><td>

Azure: SQL Security

</td><td>

Ensure that Azure Active Directory Admin is configured \(Automated\)

</td><td>

Microsoft.Sql/servers

</td><td>

Use Azure Active Directory Authentication for authentication with SQL Database to manage credentials in a single place.

</td></tr><tr><td>

Azure: SQL Security

</td><td>

Ensure SQL server's TDE protector is encrypted with Customermanaged key \(Automated\)

</td><td>

Microsoft.Sql/servers

</td><td>

TDE with Customer-managed key support provides increased transparency and control over the TDE Protector, increased security with an HSM-backed external service, and promotion of separation of duties. With TDE, data is encrypted at rest with a symmetric key \(called the database encryption key\) stored in the database or data warehouse distribution. To protect this data encryption key \(DEK\) in the past, only a certificate that the Azure SQL Service managed could be used.

 Now, with Customer-managed key support for TDE, the DEK can be protected with an asymmetric key that is stored in the Key Vault. Key Vault is a highly available and scalable cloud-based key store which offers central key management, leverages FIPS 140-2 Level 2 validated hardware security modules \(HSMs\), and allows separation of management of keys and data, for additional security. Based on business needs or criticality of data/databases hosted a SQL server, it is recommended that the TDE protector is encrypted by a key that is managed by the data owner \(Customer-managed key\).

</td></tr><tr><td>

Azure: Logging and Monitoring

</td><td>

Ensure Diagnostic Setting captures appropriate categories \(Automated\)

</td><td>

Azure Subscription

</td><td>

The diagnostic setting should be configured to log the appropriate activities from the control/management plane. A diagnostic setting controls how the diagnostic log is exported. Capturing the diagnostic setting categories for appropriate control/management plane activities allows proper alerting

 A diagnostic setting controls how the diagnostic log is exported. Capturing the diagnostic setting categories for appropriate control/management plane activities allows proper alerting.

</td></tr><tr><td>

Azure: Logging and Monitoring

</td><td>

Ensure that logging for Azure KeyVault is 'Enabled' \(Automated\)

</td><td>

Microsoft.KeyVault

</td><td>

Enable AuditEvent logging for key vault instances to ensure interactions with key vaults are logged and available.

 Monitoring how and when key vaults are accessed, and by whom enables an audit trail of interactions with confidential information, keys and certificates managed by Azure Keyvault. Enabling logging for Key Vault saves information in an Azure storage account that the user provides. This creates a new container named insights-logs-auditevent automatically for the specified storage account, and this same storage account can be used for collecting logs for multiple key vaults.

</td></tr><tr><td>

Azure: Data Security

</td><td>

Ensure that 'Unattached disks' are encrypted with CMK \(Automated\)

</td><td>

Microsoft.Compute/disks

</td><td>

Ensure that unattached disks in a subscription are encrypted with a Customer Managed Key \(CMK\).

 Managed disks are encrypted by default with Platform-managed keys.

 Using Customermanaged keys may provide an additional level of security or meet an organization's regulatory requirements.

 Encrypting managed disks ensures that its entire content is fully unrecoverable without a key and thus protects the volume from unwarranted reads.

 Even if the disk is not attached to any of the VMs, there is always a risk where a compromised user account with administrative access to VM service can mount/attach these data disks which may lead to sensitive information disclosure and tampering.

</td></tr><tr><td>

Azure: Access Control

</td><td>

Ensure the key vault is recoverable \(Automated\)

</td><td>

Microsoft.KeyVault

</td><td>

The key vault contains object keys, secrets and certificates. Accidental unavailability of a key vault can cause immediate data loss or loss of security functions \(authentication, validation, verification, non-repudiation, etc.\) supported by the key vault objects.

 It is recommended the key vault be made recoverable by enabling the "Do Not Purge" and "Soft Delete" functions. This is in order to prevent loss of encrypted data including storage accounts, SQL databases, and/or dependent services provided by key vault objects \(Keys, Secrets, Certificates\) etc., as may happen in the case of accidental deletion by a user or from disruptive activity by a malicious user.

 There could be scenarios where users accidently run delete/purge commandson key vault or attacker/malicious user does it deliberately to cause disruption. Deleting or purging a key vault leads to immediate data loss as keys encrypting data and secrets/certificates allowing access/services will become non-accessible. There are 2 key vault properties that plays role in permanent unavailability of a key vault.1.enableSoftDelete:Setting this parameter to true for a key vault ensures that even if key vault is deleted, Key vault itself or its objects remain recoverable for next 90days. In this span of 90 days either key vault/objects can be recovered or purged \(permanent deletion\). If no action is taken, after 90 days key vault and its objects will be purged.2.enablePurgeProtection:enableSoftDelete only ensures that key vault is not deleted permanently and will be recoverable for 90 days from date of deletion. However, there are chances that the key vault and/or its objects are accidentally purged and hence will not be recoverable. Setting enablePurgeProtection to "true" ensures that the key vault and its objects cannot be purged.Enabling both the parameters on key vaults ensures that key vaults and their objects cannot be deleted/purged permanently.

</td></tr><tr><td>

Azure: App Service Security

</td><td>

Ensure Web App Redirects All HTTP traffic to HTTPS in Azure App Service \(Automated\)

</td><td>

Microsoft.Web/sites

</td><td>

Azure Web Apps allows sites to run under both HTTP and HTTPS by default. Web apps can be accessed by anyone using non-secure HTTP links by default. Non-secure HTTP requests can be restricted and all HTTP requests redirected to the secure HTTPS port. It is recommended to enforce HTTPS-only traffic.

 Enabling HTTPS-only traffic will redirect all non-secure HTTP request toHTTPS ports. HTTPS uses the TLS/SSL protocol to provide a secure connection, which is both encrypted and authenticated. So it is important to support HTTPS for the security benefits.

</td></tr><tr><td>

Azure: App Service Security

</td><td>

Ensure Web App is using the latest version of TLS encryption \(Automated\)

</td><td>

Microsoft.Web/sites

</td><td>

The TLS\(Transport Layer Security\) protocol secures transmission of data over the internet using standard encryption technology. Encryption should be set with the latest version of TLS. App service allows TLS 1.2 by default, which is the recommended TLS level by industry standards, such as PCI DSS.

 App service currently allows the web app to set TLS versions 1.0, 1.1 and 1.2. It is highly recommended to use the latest TLS 1.2 version for web app secure connections.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

