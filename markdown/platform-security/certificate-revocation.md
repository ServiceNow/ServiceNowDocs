---
title: Quorum Controlled Certificate Revocation
description: The quorum-controlled certificate revocation for Code Signing certificates provides a secure mechanism for a Code Signing admin to revoke Code Signing certificates. The revocation process involves submitting a request that requires approval from multiple stakeholders. This workflow helps to prevent accidental or unauthorized revocations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Quorum Controlled Certificate Revocation

The quorum-controlled certificate revocation for Code Signing certificates provides a secure mechanism for a Code Signing admin to revoke Code Signing certificates. The revocation process involves submitting a request that requires approval from multiple stakeholders. This workflow helps to prevent accidental or unauthorized revocations.

This topic provides the high-level process overview for securely revoking certificates between a trusted instance and a protected instance using a quorum-based approval workflow.

-   Request creation and export \(Trusted instance\): Initiate a quorum certificate revocation by creating a request with the required configuration properties. Export the update set, which includes the revocation request and related data. See [Export Revocation Request Configuration](../task/export_certificate.md)
-   Import and approval \(Protected instance\): Import the update set into the protected instance. Approvers receive notifications and must complete the approval workflow before the certificate is deleted. See [Import the revocation request configuration](../task/import-certificate.md)
-   Optional MID Server restart: If enabled in the configuration, MID Servers on the protected instance are restarted after the certificate revocation. This forces immediate certificate resynchronization but can result in data loss for unprocessed or cached events. See [Approve certificate revocation](../task/cerificate-revocation-approval.md)

**Note:**

Your **update set**expires after the time window defined by the **`com.snc.kmf.signature.validity_window`** property. If it expires, you can export a new signed update set from the trusted instance. This validity window applies to all update set operations, including export, import, and enabling Code Signing. This validity window is not related to the request time window that you specify when creating the request.

-   **[Export Revocation Request Configuration](../task/export_certificate.md)**  
Start the certificate revocation process by selecting the certificate that you want to revoke. Provide the required configuration properties. Export this transaction as part of an update set, which is imported into the protected instance for approval and execution.
-   **[Import the revocation request configuration](../task/import-certificate.md)**  
Import the update set into the protected instance to initiate the certificate revocation process. Approvers receive email notifications and they should complete the approval workflow before the certificate is revoked. The approval means that the revocations are confirmed, authorized, and traceable for security and compliance purposes.
-   **[Approve certificate revocation](../task/cerificate-revocation-approval.md)**  
Review and approve certificate revocation requests from the email approval notifications that are sent to your registered email address. Review the approval notification and select the **Click here to approve** or **Click here to reject** link to access the protected instance and act. You can also access the approval request and the code-signing quorum request directly from the email.

**Parent Topic:**[Configuring Code Signing](config-code-signing.md)

