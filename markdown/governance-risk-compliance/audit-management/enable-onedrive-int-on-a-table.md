---
title: Complete the prerequisites to manage your documents using Microsoft
description: Complete the prerequisites to manage your documents using Microsoft so that you can enable the cloud file integration.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manage your documents and work papers with Audit Management as cloud files, Using Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Complete the prerequisites to manage your documents using Microsoft

Complete the prerequisites to manage your documents using Microsoft so that you can enable the cloud file integration.

## Before you begin

Role required: sn\_grc\_workspace.admin

## About this task

Ensure that you have installed the following applications:

-   Document Management \(com.snc.platform\_document\_management\)
-   Microsoft OneDrive Spoke for Document Service Framework \(sn\_docs\_onedrive\)

    **Note:** Integration Hub entitlements included in the Audit Workspace are solely restricted to the use for Microsoft integration. All other use requires the applicable purchase of an additional Integration Hub entitlement.


## Procedure

1.  Set up the Microsoft OneDrive Integration Hub Spoke.

    -   For grant type as **Authorization Code**, use a service account to generate the **OAuth** token. All the file operations in Microsoft OneDrive from ServiceNow are executed using this service account. The end user must ensure that the service account is also the owner of the file that the user is trying to link with the file.

        The required API permissions in Azure application registration are **openid**, **email**, **Files.Read**, **Files.ReadWrite.All**, **offline\_access**, **User.Read**, **User.ReadBasic.All**.

    -   For grant type as **Client Credentials**, the required API permissions in Azure application registration are **Files.Read.All** and **Files.ReadWrite.All**.

    For more information, see [Document Services Framework for Microsoft OneDrive](https://www.servicenow.com/docs/access?context=onedrive-spoke-document-services-framework&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

2.  Navigate to the **Cloud file configurations** module and configure this feature for Engagement and Audit tasks.

    The Cloud file configuration record is displayed.

    For more information on the fields, see [Create a Cloud file configuration record](manage-access-permissions-to-the-cloud-file.md).


