---
title: Create a Guided Setup
description: Create a Guided Setup to assist users with planning the roll-out of a product and performing the basic configurations to go live.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Guided Setup, Adoption services, Configure user experiences]
---

# Create a Guided Setup

Create a Guided Setup to assist users with planning the roll-out of a product and performing the basic configurations to go live.

## Before you begin

Role required: sn\_help\_setup\_admin or sn\_help\_setup\_player

The Guided Setup builder is supported by the Process Automation Designer.

## Procedure

1.  Navigate to **All** &gt; **Adoption Services** &gt; **Guided Setup**.

2.  Select the **Build your guided setups** tab.

3.  Select **Create new**.

4.  Select **Get started**.

5.  Fill in the form.

    |Field|Definition|
    |-----|----------|
    |Name|The name of your guided setup.|
    |Description|Describe the purpose of this guided setup.|
    |User roles|Roles required to access the guided setup.|

6.  Select **Continue**.

7.  To add a stage to your Guided Setup, select **Board view** do the following:

    1.  Select **Add stage**.

    2.  Fill in the form.

        -   Label
        -   Description
        -   Start rule
            -   When the process starts
            -   After specific stages
    3.  Select **Save and close**.

    4.  After creating your stages, select **Add activity**.

    5.  Select **Guided Setup** and one of the following activities:

        -   External links - Shows a list of external links such as docs and videos in the playbook UI.
        -   Iframe - Embed any page inside an iframe using a page url.
        -   Plugin Install - Installs a list of plugins from the provided plugin query.
        ![Add activity pop up.](../image/guided-setup-add-activity-1.png)

    6.  Fill in the form.

    7.  In the Details tab, fill in

        -   Label
        -   Description
        -   Start Rule
        -   Select **Show additional options**
            -   Playbook display order
            -   Start with delay
            -   Run condition
            -   Restart rules
    8.  In the Automation tab, fill in

        -   For Iframe activity: Add URL
        -   For External Links activity: Add External links
        -   For Plugin Install activity: Add Plugin query
        -   select **Show additional options**
            -   Assigned to
            -   Assignment group
            -   Wait for user input
    9.  In the UI Layout tab, fill in

        -   Select **Show additional options**
        -   associated\_table
        -   associated\_record
        -   experience\_status\_table
        -   experience\_status\_record
        -   title
        -   description
        -   icon
        -   footer
        -   tagline
    10. Select **Save and close**.

    11. Select **Activate** and then **Finalize** when you're complete with configuring your stages.

    12. Select the check box and **Continue**.

    13. Create an optional pre-setup checklist and select **Finalize**.

        For example:

        -   Image for header
        -   Content for company description
        -   Company logo
8.  To delete a stage or activity, do the following:

    1.  To delete a stage, select the more actions menu ![More actions icon](../image/guided-setup-more-actions.png) on your stage.

        -   Configure stage
        -   Add stage before
        -   Add stage after
        -   Delete stage
    2.  To delete an activity, select the more actions menu ![More actions icon](../image/guided-setup-more-actions.png) on an activity.

        -   Configure activity
        -   Configure subflow in Flow Designer
        -   Move activity
        -   Delete activity

