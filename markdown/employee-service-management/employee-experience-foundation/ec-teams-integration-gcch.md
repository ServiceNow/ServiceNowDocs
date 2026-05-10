---
title: Integrating Employee Center with Microsoft Teams for GCC-H or DoD
description: You can integrate Employee Center with Microsoft Teams to enable Government Community Cloud High \(GCC-H\) and US Department of Defense \(DoD\) customers to access attached files in Employee Center.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating ServiceNow with Microsoft Teams for GCC-H or DoD, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Integrating Employee Center with Microsoft Teams for GCC-H or DoD

You can integrate Employee Center with Microsoft Teams to enable Government Community Cloud High \(GCC-H\) and US Department of Defense \(DoD\) customers to access attached files in Employee Center.

## Prerequisites

Before integrating Employee Center with your Microsoft Teams tenant, ensure that the following prerequisites are met:

-   Your ServiceNow instances have been upgraded to the Vancouver release.
-   You have not previously attempted to install the Conversational Integration with Microsoft Teams app on your instances.
-   You have the admin permissions for the ServiceNow instance and Microsoft Azure instances.

## Integration process

The overall process to integrate Employee Center with your Microsoft Teams tenant involves the following tasks:

1.  Activate the IT Service Management integration with Microsoft Teams plugin \(sn\_now\_teams\_it\).

    **Note:** For more information on activating plugins, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

2.  [Create Microsoft Azure application and authenticate users to access Employee Center in Microsoft Teams](../task/authenticate-users-your-hub-ms-teams.md).
3.  [Update the OIDC entities table](../task/oidc-entity-table.md).
4.  [Update your Microsoft Teams tenant URL for GCC-H or DoD](../task/gcch-response-header.md).
5.  [Download and modify the manifest file for Employee Center for GCC-H or DoD](../task/upload-task-package.md).
6.  [Upload manifest file in Microsoft Teams](../task/upload-manifest-ms-teams.md).

-   **[Update the OIDC entities table](../task/oidc-entity-table.md)**  
Update the OIDC entities table to replace dummy values created by the registry file with your Microsoft Teams tenant values.
-   **[Download and modify the manifest file for Employee Center for GCC-H or DoD](../task/upload-task-package.md)**  
Download and modify the package file to provide the information that is required to make Employee Center available in your organization.
-   **[Update your Microsoft Teams tenant URL for GCC-H or DoD](../task/gcch-response-header.md)**  
Configure your Microsoft Teams tenant URL for Government Community Cloud High \(GCC-H\) or US Department of Defense \(DoD\).

**Parent Topic:**[Integrating ServiceNow with Microsoft Teams for GCC-H or DoD](setup-sn-ms-teams-gcch.md)

