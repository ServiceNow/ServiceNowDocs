---
title: Revoke software deployed through the service catalog
description: Software deployed by SCCM can be revoked, but only when the software's status is Installed and the application associated with the software configuration has an uninstall collection configured.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Revoke software deployed through the service catalog

Software deployed by SCCM can be revoked, but only when the software's status is **Installed** and the application associated with the software configuration has an uninstall collection configured.

## Before you begin

-   Create an [SCCM configuration record](t_ConfigureSCCMCollections.md) for the application that names an appropriate uninstall collection.
-   Associate the [CSD catalog item](t_CreateCatItemSCCMApp.md) for the application with the SCCM configuration that specifies the uninstall collection.

Role required: sn\_client\_sf\_dist.csd\_admin or admin

A workflow called [Revoke SCCM Application](../concept/c_SCCMSoftwareRevocation.md#) moves either the user or the device from its respective collection and adds it to the appropriate uninstall collection. When SCCM performs an internal policy check and finds the user or device in the uninstall collection, SCCM removes the related software package from the client computer.

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **Reports** &gt; **Requested Software**.

2.  Open the record for the SCCM software package you want to revoke.

    The package must have a **Status** of **Installed** to be revocable.

3.  Under **Related Links**, click **Revoke software**.

    This action runs the Revoke Client Software workflow, which triggers the Revoke SCCM Application subflow that moves the user or device from the install collection to the uninstall collection. When SCCM performs an internal policy check and finds the user or device in the uninstall collection, SCCM removes the related software package from the client computer.


