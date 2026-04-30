---
title: Key Management Framework Health
description: Access on-demand health status information for the Key Management Framework. Warning and malfunction errors contain a detailed message.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Key Management Framework, Encryption]
---

# Key Management Framework Health

Access on-demand health status information for the Key Management Framework. Warning and malfunction errors contain a detailed message.

## Before you begin

Role required: sn\_kmf\_admin and either sn\_kmf.cryptographic\_auditor or sn\_kmf.cryptographic\_manager

## About this task

Each component of the Key Management Framework is outlined and reports the following statuses and colors:

-   Green/Operational: The component is operational, no errors to report.
-   Gray/Disabled: The component is inactive, therefore no health check is performed.
-   Yellow/Degraded: Warning, the component is working, but delays/transient issues are susceptible to occur.
-   Red/Malfunction: A fatal error is preventing the component from operating, which is likely to cause partial outages.

Components can include subcomponents with individual reports and their own health status impacts the parent as follows:

-   If all subcomponents are inactive, the parent shows as inactive. Inactive subcomponents don’t impact the health of their parents.
-   If one or more subcomponents is degraded or malfunctioned, the parent health shows as degraded.
-   If all subcomponents report as malfunctioned, then the parent also reports as malfunctioned.

For additional information on subcomponents, see [Instance level keys in the Key Management Framework](../reference/instance-level-keys.md).

**Note:** Health checks run every 15 seconds. Refresh the health page to rerun the report.

## Procedure

1.  Navigate to **All** &gt; **Key Management** &gt; **** &gt; **Diagnostics**.

2.  Review the following health status information:

<table id="table_q45_5b5_xrb"><thead><tr><th>

Category

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Key Secure

</td><td>

Checks if encryption is being attempted.

</td></tr><tr><td>

File Key Store

</td><td>

Checks if an Instance Root Key \(IRK\) fetch attempt is occurring.**Note:** The File Key Store is an offline alternative to Key Secure used for on-premise instances and developer instances.

</td></tr><tr><td>

GlideEncrypter

</td><td>

Checks if a GlideEncrypter instance-level cryptographic module, specification, and key are present.**Note:** GlideEncrypter is a scriptable component that enables transparent encryption of Password2 fields and other legacy encryption usages through the Key Management Framework.

</td></tr><tr><td>

Instance Key Encryption Key \(IKEK\)

</td><td>

Checks if the key can be fetched from the File Key Store or KeySecure.

</td></tr><tr><td>

Instance HMAC Key

</td><td>

Checks if the key can be fetched from the File Key Store or KeySecure.

</td></tr><tr><td>

Vault PKI

</td><td>

Checks Vault connectivity to verify if the Instance Asymmetric Encryption Key \(IAEK\) and Instance Signature Key \(ISK\) are usable and can be fetched from Vault.

</td></tr><tr><td>

EJBCA PKI

</td><td>

Checks LDAP connectivity to verify if IAEK and ISK are usable and can be fetched from cache and LDAP.

</td></tr><tr><td>

Instance PKI

</td><td>

Checks the File Key Store and KeySecure for a key and whether the certificate is present and matches the symmetric key.**Note:** Instance PKI is only available on instances within a ServiceNow datacenter.

</td></tr></tbody>
</table>    For assistance in troubleshooting, contact Customer Service and Support.


**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

