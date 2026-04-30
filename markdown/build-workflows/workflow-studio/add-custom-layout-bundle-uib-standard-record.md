---
title: Add a custom layout bundle to a UI Builder standard record page
description: Add playbook custom layout bundles to a new or an existing UI Builder standard record page.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Customize the Playbook Experience, Designing playbooks, Use, Workflow Studio, Build workflows]
---

# Add a custom layout bundle to a UI Builder standard record page

Add playbook custom layout bundles to a new or an existing UI Builder standard record page.

## Before you begin

Role required: admin, ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the upper right, select **+Create** to create a new experience.

3.  Fill in the fields for your experience.

<table id="choicetable_jwq_jdh_x1c"><tbody><tr><td id="d73110e87">

**Name**

</td><td>

The name is used for tracking the experience internally. The experience name is also visible to users from the browser tab.

</td></tr><tr><td id="d73110e96">

**URL path**

</td><td>

The URL path is the prefix that people will use to reach your experience. It matches your experience name by default. You can edit this path now or later in UI Builder.

Supported characters include digits \(0-9\), letters \(A-Z, a-z\), and the following symbols: $-\_!\*\(\),The path can't end with a forward slash \(/\).

</td></tr><tr><td id="d73110e112">

**App shell UI**

</td><td>

Choose the **UXR Base Experience Shell**.

 The app shell is the wrapper of the page contents, which is similar to the functionality of a web page. The app shell can show things like the logo of your company, user preferences, and the search icon. To learn more about the app shell options, see [Define UI experiences using app shells](https://www.servicenow.com/docs/access?context=app-shells-uibuilder&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td id="d73110e137">

**Landing path**

</td><td>

The landing path is the prefix that people will use to reach your experience homepage. It matches your experience name by default. To designate a page as the homepage, you will need to create a page that has a matching path.

</td></tr><tr><td id="d73110e146">

**Roles**

</td><td>

Only users with these assigned roles can access the experience. If you leave this field empty, the experience is open to all logged-in users by default.

</td></tr></tbody>
</table>4.  Select **Create**.

5.  In your new UI Builder experience, select **Create new page**.

    The **Select a template** screen displays.

6.  Choose the **Standard record** template and select **Use template**.

7.  Set up the page details.

<table id="table_grl_ch1_x1c"><tbody><tr><td>

**Name**

</td><td>

The name of your page.

</td></tr><tr><td>

**URL Path**

</td><td>

The URL path that users navigate to, to access the page.

</td></tr></tbody>
</table>8.  Select **Continue**.

9.  Add the test URL parameters for your page.

    **Note:** All playbooks require at least a table and sysId to be hardcoded on the controller or provided through a URL.

<table id="table_gp1_s4h_x1c"><tbody><tr><td>

**table**

</td><td>

Name of the parent table for the playbook.

</td></tr><tr><td>

**sysID**

</td><td>

Sys\_id of the record. For a record that doesn't exist, the value is **-1**.

</td></tr></tbody>
</table><table id="table_lnh_x4h_x1c"><tbody><tr><td>

**query**

</td><td>

Encoded Query string to optionally override the query provided for a record generator.

</td></tr><tr><td>

**extraParams**

</td><td>

Pass additional parameters to a page.

</td></tr><tr><td>

**views**

</td><td>

View mode used to render Playbook activities in stacked or focused mode.

</td></tr><tr><td>

**selectedTabIndex**

</td><td>

The tab that your page opens to by default.

</td></tr></tbody>
</table>10. Setup your default [page variant](https://www.servicenow.com/docs/access?context=create-variant&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

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

11. In the success message, select **Open in editor** to open your new page in the UIB editor.

12. In the component tree, select the **Main Tab**.

    The **Main Tab** panel opens on the right.

13. Under the **Tabs** section in the **Config** tab, select **+ Add**.

    A modal asking "How do you want to build this tab?" displays.

14. Select **Start from an empty container** and click **Next**.

    A **Tab Settings** modal displays.

15. Give your tab a name and an icon, and click **Create**.

    The tab is added to the component tree and a blank canvas displays.

16. In the component tree, under your new tab, select **+ Add component**.

    The toolbox opens.

17. Enter "bundle" in the search bar of the toolbox.

    Available bundles are displayed.

18. Select the bundle you want to add to your page.


## Result

You've added a bundle and all its components, presets, and controller to your new UI Builder standard record page.

If the width of the bundle container is set to the min-width of the component, set the **min-width** of the container to **100%**.

![Sizing settings under the bundle container Styles tab](../images/troubleshooting-custom-layout-bundle-1.png)

## What to do next

Edit test values and controller inputs.

**Parent Topic:**[Customize the Playbook Experience](../../workspace/concept/playbook-customize-playbook.md)

