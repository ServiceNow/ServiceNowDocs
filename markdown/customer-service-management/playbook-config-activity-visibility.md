---
title: Configure playbook stage and activity visibility
description: Configure the visibility of playbook stages and activities that are pending or that a user cannot access.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Playbooks for Customer Service Management, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure playbook stage and activity visibility

Configure the visibility of playbook stages and activities that are pending or that a user cannot access.

## Before you begin

Role required: admin

## About this task

Use the following fields in the playbook experience configuration record to control the visibility of playbook stages and activities.

-   **Inaccessible Data Visibility**: Accessibility is determined by user permissions. When enabled, the user cannot see an activity if they do not have permissions to view the data associated with the activity. If all activities in a stage are inaccessible to the user, the stage is also hidden.
-   **Pending Item Visibility**: Pending activities are those activities that have not yet been triggered. Select one of the options in this field to show or hide pending activities.

## Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Playbook Experiences**.

2.  Select a Playbook experience.

3.  In the Configurations related list, click the desired configuration.

4.  Select **Hide Inaccessible Activity** from the **Inaccessible Data Visibility** field drop-down list to hide the activities in a stage that the logged-in user cannot access.

    The default value for this field is false.

5.  In the **Pending Item Visibility** field, select one of the following options.

<table id="choicetable_zlx_32h_vpb"><thead><tr><th align="left" id="d270104e121">

Option

</th><th align="left" id="d270104e124">

Description

</th></tr></thead><tbody><tr><td id="d270104e130">

**Show pending stages and activities**

</td><td>

-   Shows all activities in a stage.
-   Pending activities are grayed out.
-   Default setting.


</td></tr><tr><td id="d270104e151">

**Hide pending activity**

</td><td>

-   Hides the pending activities in a stage.
-   If all activities are pending and hidden, the stage is grayed out.


</td></tr><tr><td id="d270104e169">

**Hide pending activities and stages**

</td><td>

-   Hides the pending activities in a stage.
-   If all activities are pending and hidden, the stage is also hidden.


</td></tr></tbody>
</table>6.  Click **Update**.


**Related topics**  


[Configure an optional activity for a playbook](configure-optional-activity-for-a-case-type-playbook.md)

