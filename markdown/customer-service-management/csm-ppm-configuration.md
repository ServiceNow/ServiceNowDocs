---
title: Integrate with Customer Project Management using Guided Setup
description: Use the Customer Service Management Guided Setup to configure Customer Project Management.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating with Customer Project Management, Integrating Customer Service Management with other applications, Customer Service Management]
---

# Integrate with Customer Project Management using Guided Setup

Use the Customer Service Management Guided Setup to configure Customer Project Management.

## Before you begin

Role required: admin

## About this task

You can configure a number of different processes and components for the Customer Project Management feature using Guided Setup.

## Procedure

1.  Navigate to **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  Click **Get Started** on the Customer Service Management home page.

3.  Scroll through the list of categories, locate Customer Project Management, and click **Get Started**.

    The table below provides a description of the configuration steps included in this guided setup section.

<table id="table_csm_ppm_configuration"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate PPM Standard.

</td><td>

Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

</td></tr><tr><td>

Activate Customer Project Management.

</td><td>

Activate the Customer Project Management plugin \(com.snc.csm\_ppm\).

</td></tr><tr><td>

Configure form views.

</td><td>

Configure the Case form and add the following fields to the Case view, Workspace view, and Customer Self Service view: -   Project
-   Project Task
-   Issue
-   Project Change Request


</td></tr><tr><td>

Configure related lists.

</td><td>

Configure the Account form and add the **Projects** related list to the Case view and Workspace view. Configure the Contact form and add the **Projects** related list to the Case view and Workspace view.

 Configure the Customer Project Task form and add the following related lists to the **Default** view: **Work Order** &gt; **Initiated From**.

This step can only be completed if the following plugins are active:

-   Customer Service with Field Service Management \(com.snc.csm\_fsm\_integration\)
-   Field Service with Project Management \(com.snc.wm\_ppm\)


</td></tr><tr><td>

Configure notifications.

</td><td>

Configure the **Send Email to Contact when Customer Project Task is assigned** Flow Designer flow to send an email to the assigned contact when a customer project task is assigned.This notification includes the following details and can be configured as necessary:

-   Project number and name
-   Task number and short description
-   Task planned start and end dates and duration


</td></tr><tr><td>

Configure Flow Designer flows.

</td><td>

Use Flow Designer flows provided with Customer Project Management to:-   Configure the fields that are copied over, when a user creates a project issue or project change request from a case.
-   Update the work notes for a case record when the state of an associated project issue or project change request is updated.
-   Close a case record when an associated project issue or project change request is closed.
 **Create Project Issue from Case**: When a project issue is created from a case, this flow copies the **Priority** and **Short description** fields from the case to the project issue record. This flow is active by default.

 **Create Project Change Request from Case**: When a project change request is created from a case, this flow copies the **Priority** and **Short description** fields from the case to the project change request record. This flow is active by default.

 **Update and Close Case Record on Issue Closure**: This flow enables you to automatically:

-   Update the case work notes when the state of an associated issue is updated.
-   Close a case if the state of the associated issue is set to Closed.
Activate this flow as needed.

 **Update and Close Case Record on Project Change Closure**: This flow enables you to automatically:

-   Update the case work notes when the state of an associated project change request is updated.
-   Close a case if the state of the associated project change request is set to Closed.
Activate this flow as needed.

</td></tr><tr><td>

Assign Access Controls \(ACLs\)

</td><td>

Assign ACLs to the Customer Service Management user roles to provide access to the Project Portfolio Management tables, including the Project Change Request, Status Report, and Issues tables.

</td></tr></tbody>
</table>
