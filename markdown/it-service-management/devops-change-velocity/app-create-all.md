---
title: Create an application - Classic
description: Create applications using the Classic UI or the Service Catalog.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Applications, DevOps Change Velocity, IT Service Management]
---

# Create an application - Classic

Create applications using the Classic UI or the Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.app\_owner

## Procedure

1.  You can create applications using the Classic UI, or the Service Catalog.

    -   Classic UI: Navigate to **All** &gt; **DevOps** &gt; **Apps &amp; Pipelines** &gt; **Create App \(legacy\)**.
    -   Service Catalog: Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintatin Items** &gt; **Create DevOps Application** &gt; **Try It**.
2.  On the Create DevOps Application form, choose whether to create a new application and new application model or to base the application on an existing application model.

<table id="choicetable_ddn_pxv_2tb"><thead><tr><th align="left" id="d447177e105">

Choice

</th><th align="left" id="d447177e108">

Actions

</th></tr></thead><tbody><tr><td id="d447177e114">

**New application**

</td><td>

Enter a name for the new application.

 -   The system generates a new DevOps application, a new application model, and a new SDLC component \(SDLC-C\) in the CMDB.
-   The SDLC-C is assigned the same name as the new application.
-   If the DevOps Config application is installed, then DevOps associates the application to the CDM application.


</td></tr><tr><td id="d447177e150">

**Existing application model**

</td><td>

Select the application model from the list.

 The system generates a new DevOps application from that application model.

-   The application is given the same name as the application model.
-   If an SDLC component exists for the application model, then DevOps associates the SDLC-C to the new application.
-   If an SDLC component doesn’t exist for the application model, then DevOps generates a new SDLC-C with the same name as the application model.
-   If DevOps Config is installed, then DevOps creates a CDM application and associates the SDLC-C to the application.


</td></tr></tbody>
</table>3.  Select **Submit**.


## What to do next

You can view the list of all the applications from the Apps page in the Classic UI. Navigate to **All** &gt; **DevOps** &gt; **Apps &amp; Pipelines** &gt; **Apps** and select your application.

For each application, you can:

-   Update details such as  **Business app**, **State \(Active\)**, and  **Log Level**. Applications marked as **Active** are polled daily for updates to associated plans, repositories, and pipelines.
-   Control access to the application by adding user groups to the **Maintained by** field. You can select any group that has at least one user with DevOps roles.

    When user groups are added:

    -   Users with DevOps App Owner role or DevOps Administrator role can edit and associate objects with the application.
    -   Users having other DevOps roles can view the application.
    -   Users having DevOps roles, but aren’t part of the groups added can't view the application.
    **Note:** DevOps admins can always see and edit everything in DevOps.

-   View and associate plans, repositories, pipelines, and artifact repositories. Associate the appropriate tool objects to the application to ensure that all the DevOps data is grouped and tracked. For more information, see [Associate tool objects to applications – Classic](apps-associate-objects-classic.md).
-   Delete the application record.

