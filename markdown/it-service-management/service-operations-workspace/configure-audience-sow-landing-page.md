---
title: Configure the audience for the SOW landing page
description: Define who can access your SOW landing pages. You can targeted experiences for audiences such as agents and managers.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access controls in Service Operations Workspace for ITSM, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the audience for the SOW landing page

Define who can access your SOW landing pages. You can targeted experiences for audiences such as agents and managers.

## Before you begin

Role required: admin

## About this task

You can configure the audiences that define who can access the SOW landing pages. For information about audiences, see [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

By default, the SOW landing page is associated with the following audiences. To access SOW, a user must align with the following criteria.

-   The user has the admin role
-   The user has the sn\_incident\_write role and belongs to the Service Desk user group.
-   The user has the itil role and belongs to Service Desk user group.

## Procedure

1.  Create an audience if required.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Building Blocks** &gt; **Audiences**.

    2.  On the Audiences page, select **New**.

    3.  Specify the required data.

        For example, specify the following:

        -   Name: SOW Service Desk T1
        -   Roles: itil
        -   Any user criteria inclusions. For this, add a user criteria and then add user groups to it.
    4.  Select **Save**.

2.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

3.  From the **Experiences** section, select **Service Operations Workspace**.

4.  From the **Pages and Variants** section, select **Settings** for **Home Landing Page**.

5.  On the Variant: Service desk landing page SNC page, from the **Pages and variants** section, select **Service Desk landing page SNC**.

6.  Change the application scope to Incident management for Service Operations Workspace.

7.  From the **Audiences** section, select **Edit all audiences**.

8.  In the Edit Audiences window, select **Add**.

9.  Search for your audience and select **Save**.


