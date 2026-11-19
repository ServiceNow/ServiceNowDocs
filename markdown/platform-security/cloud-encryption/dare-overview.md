---
title: Cloud Encryption with Key Management
description: ServiceNow Cloud Encryption offers encrypted storage for the database using block encryption, along with enhanced key management. Cloud Encryption is available with the ServiceNow Platform Encryption subscription bundle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/cloud-encryption/dare-overview.html
release: zurich
product: Cloud Encryption
classification: cloud-encryption
topic_type: concept
last_updated: "2026-05-21"
reading_time_minutes: 3
breadcrumb: [Encryption]
---

# Cloud Encryption with Key Management

ServiceNow® Cloud Encryption offers encrypted storage for the database using block encryption, along with enhanced key management. Cloud Encryption is available with the ServiceNow® Platform Encryption subscription bundle.

Cloud Encryption offers:

-   Segregation of duties.
-   Rotation of ServiceNow Managed keys.
-   Customer-Managed keys option.

    **Note:** With customer-managed keys, ServiceNow holds the encryption key on its infrastructure, but you perform key operations on it. Managing your key means you can bring your own key material \(BYOK\), rotate ServiceNow-managed or customer-managed keys, and withdraw your key. Keys aren't hosted on your own infrastructure. See [Key management operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/key-mgmt-operations-ce.md) for details.


The following diagram shows how Cloud Encryption works.

\[Omitted image "ce-cloud-encryption-overview.svg"\] Alt text: Cloud Encryption overview diagram

The Cloud Encryption Key Management module consists of the following submodules:

-   [Key management operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/key-mgmt-operations-ce.md):
    -   Access the list of keys.
    -   Perform key rotation operations.
    -   Withdraw customer-managed key.
-   [Key management transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/key-mgmt-transactions-ce.md):

    Reference all transactions that have occurred for the keys that have been used. Bring your own encryption key \(BYOK\) for use with Cloud Encryption.

    Use your own customer-managed key for encryption.


In certain circumstances, you may opt for a key withdrawal request when using a customer-managed key. To do so, you must license the Cloud Encryption Withdraw and Resupply optional add-on SKU and then request the key withdrawal functionality be activated by a Customer Service and Support team member.

The Quorum Control Policy Settings option becomes available when the withdrawal feature is activated, otherwise the module isn’t visible on the menu. This feature can be activated only when using customer-managed keys. This policy enables settings to be configured regarding quorum when the withdrawal feature is activated. For more details on this feature, see [Quorum Control Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/quorum-ctrl-policy.md).

Cloud Encryption supports production and non-production instances for MariaDB and RaptorDB databases. Cloud Encryption is supported in the ServiceNow Commercial Cloud, Government Customer Cloud \(GCC\) pod 101, and ServiceNow Protected Platform – Australia \(SPP-AU\).

## Licensing and enabling Cloud Encryption

For information about licensing Cloud Encryption, see [Encryption and Key Management subscription bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/encryption-sku.md).

For licensed customers with new instances, the new instance provisioning will include Cloud Encryption.

For licensed customers with existing instances, to request an instance be moved to Cloud Encryption, follow the instructions in [KB1117369](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117369). You must have the customer admin or partner admin role to request the Service Catalog item to Enable Cloud Encryption on your instance. Enabling this feature requires a one-hour maintenance window.

## Cloud Encryption UI

When Cloud Encryption is enabled, the Cloud Encryption user interface \(UI\) is visible to the security\_admin user when this user has the sn\_kmf.admin role.

To access the Cloud Encryption UI by searching for **Cloud Encryption Key Management** in the navigation bar. Navigate to the **Key Management Operations** section to see information about encryption keys, such as details of the active key, and whether Cloud Encryption is enabled for the instance.

-   **[Key management operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/key-mgmt-operations-ce.md)**  
The Key Management Operations submodule provides access to view and manage all encryption keys used with ServiceNow Cloud Encryption.
-   **[Quorum Control Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/quorum-ctrl-policy.md)**  
The Quorum Control Policy specifies the minimum number of approvals required among the total number of selected approvers to reach quorum for customer managed key withdrawal.
-   **[Key management transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/key-mgmt-transactions-ce.md)**  
The Key Management Transactions submodule displays all transactions that have occurred for the keys in your ServiceNow instance.
-   **[Cloud Encryption logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/dare-logging.md)**  
Learn about logging options for Cloud Encryption.
-   **[Tamper Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/tamper-detect.md)**  
Use tamper detection to improve security by detecting unauthorized changes to your quorum control settings.

**Parent Topic:**[Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/encryption-landing.md)

