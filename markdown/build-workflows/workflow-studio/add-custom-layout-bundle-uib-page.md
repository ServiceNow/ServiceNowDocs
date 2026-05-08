---
title: Add a custom layout bundle to a UI Builder page
description: Add playbook custom layout bundles to a new or existing UI Builder page that you've created from scratch.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize Playbook Experience, Design Playbook Experience, Playbooks, Workflow Studio, Build workflows]
---

# Add a custom layout bundle to a UI Builder page

Add playbook custom layout bundles to a new or existing UI Builder page that you've created from scratch.

## Before you begin

Role required: admin, ui\_builder\_admin

## About this task

Templates are page level, they are meant to be used when you create a completely new page. Bundles are like templates that you can add to a new or an existing page.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder** and select **Playbook Experience Builder**.

    The **Playbook Experience Builder** experience was built for you to customize Playbook Experience. For more information on how to create an experience, see Configure how users interact with your applications in UI Builder.

2.  Select **+** next to **Pages and variants** to create a new page.

3.  Select **Create a new page**.

    The **Select a template** screen displays.

4.  Select **Create from scratch instead** button at the top right.

5.  Set up the page details.

<table id="table_grl_ch1_x1c"><tbody><tr><td>

**Name**

</td><td>

The name of your page.

</td></tr><tr><td>

**URL Path**

</td><td>

The URL path that users navigate to, to access the page.

</td></tr></tbody>
</table>6.  Select **Continue**.

7.  Add the test URL parameters for your page.

    **Note:** All playbooks require at least a table and sysId to be hardcoded on the controller or provided through a URL.

<table><tbody><tr><td>

**table**

</td><td>

Name of the parent table for the playbook.

</td></tr><tr><td>

**sysID**

</td><td>

Sys\_id of the record. For a record that doesn't exist, the value is **-1**.

</td></tr></tbody>
</table>8.  Setup your default page variant.

<table id="table_frz_wd3_q1c"><tbody><tr><td>

**Name**

</td><td>

The name of your page variant.

</td></tr><tr><td>

**Audiences**

</td><td>

The users that can see your page variant. They can be defined by:-   Role
-   Group
-   User
-   Company
-   Department
-   Location
-   Script


</td></tr><tr><td>

**Conditions**

</td><td>

Conditions that determine when the page variant is shown.

</td></tr></tbody>
</table>    The page and default variant are created.

9.  Open your new page variant.

10. In the component tree, select **+ Add component** under **Body**.

    The toolbox opens.

11. Enter "bundle" in the search bar of the toolbox.

    Available bundles are displayed.

12. Select the bundle you want to add to your page.


## Result

You've added a bundle and all its components, presets, and controller to your new UI Builder page.

## What to do next

Edit test values and controller inputs.

