---
title: Software revocation
description: Revoke software without any user interaction if the software can be revoked and has a lease end date using the provider-specific revocation flow.Software deployed by the software provider can be revoked when the application associated with the software configuration has an uninstall collection configured. CSD 2.0 can revoke software requested using the CSD 2.0 catalog. CSD 2.0 can also uninstall software using Microsoft Endpoint Configuration Manager, Microsoft Intune, and Jamf when revocation is triggered from the reclamation candidates.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Software revocation

Revoke software without any user interaction if the software can be revoked and has a lease end date using the provider-specific revocation flow.

**Parent Topic:**[Client Software Distribution 2.0 application](csd-app-2.md)

## Revoke software deployed through the service catalog

Software deployed by the software provider can be revoked when the application associated with the software configuration has an uninstall collection configured. CSD 2.0 can revoke software requested using the CSD 2.0 catalog. CSD 2.0 can also uninstall software using Microsoft Endpoint Configuration Manager, Microsoft Intune, and Jamf when revocation is triggered from the reclamation candidates.

### Before you begin

-   Create a provider-specific configuration record for the application that names an appropriate uninstall collection.
-   Associate the CSD 2.0 catalog item for the application with the provider configuration that specifies the uninstall collection.

Role required: itil, sn\_csd.CSD Admin, or sn\_csd.CSD User

### Procedure

1.  Navigate to **Client Software Distribution 2.0** &gt; **Requested Software**.

2.  Open the record for the software package you want to revoke.

    The package must have a **Status** of **Installed** or **Not Synced** to be revocable.

3.  Under **Related Links**, click **Revoke software**.

    **Note:** This action runs the Revoke Client Software flow, which triggers the provider-specific Revoke Application subflow.


