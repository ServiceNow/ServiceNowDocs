---
title: Exploring Code Signing
description: Code Signing provides cryptographic verification to ensure that only authorized scripts can execute on MID Servers. Code Signing prevents unauthorized or tampered ECC queue records from being processed by MID Servers, maintaining the integrity of integrations between ServiceNow and external systems.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Code Signing, Platform Security]
---

# Exploring Code Signing

Code Signing provides cryptographic verification to ensure that only authorized scripts can execute on MID Servers. Code Signing prevents unauthorized or tampered ECC queue records from being processed by MID Servers, maintaining the integrity of integrations between ServiceNow and external systems.

Code Signing creates digital signatures for your data, which are later checked to confirm the authenticity and integrity of the data. Code Signing is a module licensed as a component of ServiceNow Vault.

**Note:** The Customer Service and Support team must grant access to Code Signing.

<table id="table_f3d_s52_sxb"><tbody><tr><td>

Code Signing declares the intent behind the operation being performed and validates whether the resource or record may be used for the intended purpose. To facilitate Code Signing, the Key Management Framework \(KMF\) uses digital certificates and industry standard asymmetric encryption for digital signatures.

 Use Code Signing internally on the platform and infrastructure side. Code signing provides a way to sign the content of specific tables or of a subset of records in a given metadata table.

</td><td>

![Code signing process diagram](../image/codesign-diagram-1.png)

</td></tr></tbody>
</table>Code Signing uses a secure Circle of Trust \(COT\) between your trusted and protected instances to help ensure that only authorized, secure trusted instances can access the Code Signing feature.

**Note:** Code Signing is enabled on the protected instance and not on the trusted instance.

## How Code Signing protects your environment

Without Code Signing, an attacker who gains access to ServiceNow records can modify SQL statements in a protected instance. When the MID Server processes this data source request, it would execute the malicious SQL commands, potentially compromising system integrity and security.

When you implement a Circle of Trust architecture with Code Signing, transfer of data to the MID Server follows the following verification process. This process helps ensure that only authorized code originating from the trusted instance can execute on the MID Server. The processes reduces potential attack vectors that could otherwise compromise your systems.

1.  Digital signatures are applied to data sources created or updated within the trusted instance.
2.  Use the Code signing process to transfer the signed data from the trusted instance to the protected instance
3.  The MID Server verifies the digital signature on all incoming requests, automatically rejecting any requests lacking valid signatures.
4.  If the MID Server rejects a request, it logs this rejection and sends a notification to the protected instance.

## Benefits of implementing Code Signing

Code Signing provides several key advantages:

-   **Execution Control**

    Only cryptographically verified scripts can run on MID Servers

-   **Tamper Detection**

    Any modifications to signed records are immediately identified and blocked.

-   **Automated Protection**

    The system handles security enforcement without requiring manual intervention.

-   **Comprehensive Logging**

    All signature verification failures generate detailed audit records.


## Code Signing validation and jobs

All the metadata tables with valid configurations are signed at build time using the Code Signing metadata plugin​ \(com.glide.code\_signing\). Installing this plugin automatically installs the Code Signing OOB App Signatures plugin \(com.glide.code\_signing.oob\_apps\_signatures\) which contains build time signatures for all relevant records in the trued-up ServiceNow® Store application versions. If you choose to sign tables, admin users with the Security administrator role have access to Code Signing job​s:

-   Sign update sets.
-   Mass sign records.
-   Mass sign attachments.

-   **Sign update set**

    This job signs records that match a signature configuration in the update set. The job also adds all the new signature records and the verification certificates to the update set.

    ![Signature Configuration record for an update set.](../../key-management-framework/image/kmf-signature-config.png "KMF signature record for update set")

-   **Mass sign records**

    This job signs all the records that match the signature configuration applied on a specific metadata table​.

-   **Mass sign attachments**

    This job signs all the attachment records that are attached to a table that matches a specified signature configuration​.

    ![Encryption job to mass sign records.](../../key-management-framework/image/encryption-job.png "Encryption job to mass sign records")


**Parent Topic:**[Code Signing](code-signing-landing.md)

