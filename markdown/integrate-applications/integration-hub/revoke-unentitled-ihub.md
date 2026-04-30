---
title: Revoke unentitled software
description: Revoke software using Microsoft System Center Configuration Manager \(SCCM\) that a user is not entitled to use even if the software was installed by some other process or user.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SCCM software revocation, Client software distribution from SCCM, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Revoke unentitled software

Revoke software using Microsoft System Center Configuration Manager \(SCCM\) that a user is not entitled to use even if the software was installed by some other process or user.

## Before you begin

To revoke software using SCCM, you must create an [Define an SCCM configuration](https://www.servicenow.com/docs/access?context=t_ConfigureSCCMCollections&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for the application, in which the appropriate software Discovery model is defined. See [Software discovery models](https://www.servicenow.com/docs/access?context=c_DiscoveryModels&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) [Discovery models and software installations](https://www.servicenow.com/docs/access?context=c_DiscoveryModels&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).

Role required: sn\_client\_sf\_dist.csd\_admin or admin

Client Software Distribution \(CSD\) uses [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SAMOverview&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) to identify unentitled software installations. Discovery detects the software on the user's machine, and SAM determines if the user or device is entitled to use that software. This might include software that was not installed through a catalog request or software that the user installed without approval. If the software installation's Discovery model is associated with an SCCM software configuration that has an uninstall collection defined, then an administrator can use CSD to revoke that software from the user's machine without involving the user.

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **Reports** &gt; **Installed Software Not Entitled**.

2.  Select the record for the installation that has unentitled users.

3.  Under **Related Links**, click **Revoke software**.

    This action runs the Revoke Client Software flow, which triggers the Revoke SCCM Application subflow that moves the user or device from the install collection to the uninstall collection. When SCCM performs an internal policy check and finds the user or device in the uninstall collection, SCCM removes the related software package from the client computer.

    ![Revoking a software installation](../images/SCCMSoftwareInstallation.png)


**Parent Topic:**[SCCM software revocation](../concept/sccm-revocation-ihub.md)

