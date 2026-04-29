---
title: SCCM software revocation
description: An administrator can revoke software without any user interaction using Microsoft System Center Configuration Manager \(SCCM\) if the software configuration specifies an SCCM uninstall collection, even if the software was installed by some other process or user.Software deployed by SCCM can be revoked, but only when the software's status is Installed and the application associated with the software configuration has an uninstall collection configured.An administrator can revoke software using Microsoft System Center Configuration Manager \(SCCM\) that a user is not entitled to use even if the software was installed by some other process or user.The Revoke SCCM Application workflow moves a user or device from an install collection to an uninstall collection to revoke software installed from Microsoft System Center Configuration Manager \(SCCM\).
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# SCCM software revocation

An administrator can revoke software without any user interaction using Microsoft System Center Configuration Manager \(SCCM\) if the software configuration specifies an SCCM uninstall collection, even if the software was installed by some other process or user.

**Parent Topic:**[Client software distribution from SCCM](c_CSDFromAnSCCMHost.md)

## Revoke software deployed through the service catalog

Software deployed by SCCM can be revoked, but only when the software's status is **Installed** and the application associated with the software configuration has an uninstall collection configured.

### Before you begin

-   Create an [SCCM configuration record](../task/t_ConfigureSCCMCollections.md) for the application that names an appropriate uninstall collection.
-   Associate the [CSD catalog item](../task/t_CreateCatItemSCCMApp.md) for the application with the SCCM configuration that specifies the uninstall collection.

Role required: sn\_client\_sf\_dist.csd\_admin or admin

A workflow called [Revoke SCCM Application](c_SCCMSoftwareRevocation.md#) moves either the user or the device from its respective collection and adds it to the appropriate uninstall collection. When SCCM performs an internal policy check and finds the user or device in the uninstall collection, SCCM removes the related software package from the client computer.

### Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **Reports** &gt; **Requested Software**.

2.  Open the record for the SCCM software package you want to revoke.

    The package must have a **Status** of **Installed** to be revocable.

3.  Under **Related Links**, click **Revoke software**.

    This action runs the Revoke Client Software workflow, which triggers the Revoke SCCM Application subflow that moves the user or device from the install collection to the uninstall collection. When SCCM performs an internal policy check and finds the user or device in the uninstall collection, SCCM removes the related software package from the client computer.


## Revoke unentitled software

An administrator can revoke software using Microsoft System Center Configuration Manager \(SCCM\) that a user is not entitled to use even if the software was installed by some other process or user.

### Before you begin

To revoke software using SCCM, you must create an [SCCM configuration record](../task/t_ConfigureSCCMCollections.md) for the application, in which the appropriate software Discovery model is defined. See [Software discovery models](https://www.servicenow.com/docs/access?context=c_DiscoveryModels&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

Role required: sn\_client\_sf\_dist.csd\_admin or admin

Client Software Distribution \(CSD\) uses [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SAMOverview&version=australia&pubname=australia-it-asset-management&ft:locale=en-US) to identify unentitled software installations. Discovery detects the software on the user's machine, and SAM determines if the user or device is entitled to use that software. This might include software that was not installed through a catalog request or software that the user installed without approval. If the software installation's Discovery model is associated with an SCCM software configuration that has an uninstall collection defined, then an administrator can use CSD to revoke that software from the user's machine without involving the user.

### Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **Reports** &gt; **Installed Software Not Entitled**.

2.  Select the record for the installation that has unentitled users.

3.  Under **Related Links**, click **Revoke software**.

    This action runs the Revoke Client Software workflow, which triggers the Revoke SCCM Application subflow that moves the user or device from the install collection to the uninstall collection. When SCCM performs an internal policy check and finds the user or device in the uninstall collection, SCCM removes the related software package from the client computer.

    ![Revoking a software installation](../../../administer/integrationhub/images/SCCMSoftwareInstallation.png "Revoking a software installation")


## SCCM software revocation workflow

The Revoke SCCM Application workflow moves a user or device from an install collection to an uninstall collection to revoke software installed from Microsoft System Center Configuration Manager \(SCCM\).

For the revocation workflow to run, the software package must have a status of [**Installed**](c_ClientSWDistValidProcess.md) and must be pre-configured for an appropriate uninstall collection. See [Revoke software deployed through the service catalog](https://www.servicenow.com/docs/access?context=c_SCCMSoftwareRevocation&version=australia&pubname=australia-servicenow-platform&section=t_RevokeSoftwareInstalledFromSCCM&ft:locale=en-US) for configuration instructions. When an administrator initiates the revocation process, the system launches the Revoke SCCM Application workflow to move the user or device collection associated with installation to the appropriate SCCM uninstall collection. When the SCCM server performs a policy check, it finds the additions to the user or device uninstall collection and revokes the software package associated with that collection.

The workflow employs two custom activities, [Remove from User Collection](../../../administer/orchestration-activities/reference/r_RemoveFromUserCollectionActivity.md) and [Remove from Device Collection](../../../administer/orchestration-activities/reference/r_RemoveFmDevicCollectionActivity.md), to remove either the user or the device from its original collection. The workflow then adds the user or device to the appropriate uninstall collection on the SCCM server with the [Add to User Collection](../../../administer/orchestration-activities/reference/r_AddToUserCollectionActivity.md) or [Add to Device Collection](../../../administer/orchestration-activities/reference/r_AddToDeviceCollectionActivity.md) activity.

**Note:** This workflow is triggered by the Revoke Client Software workflow as a subflow.

