---
title: Customize a playbook in UI Builder
description: Use UI Builder pages and modular components for custom playbook layouts to customize the end user's Playbook Experience in a configurable workspace, Service Portal page, or mobile web page.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Customize the Playbook Experience, Designing playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Customize a playbook in UI Builder

Use UI Builder pages and modular components for custom playbook layouts to customize the end user's Playbook Experience in a configurable workspace, Service Portal page, or mobile web page.

## Before you begin

-   If you don't have a playbook to apply custom layouts to, build a playbook. To learn more, see [Building playbooks](../../process-automation-designer/concept/building-a-process.md).
-   Install the latest version of the Playbook Experience and Playbook Experience Component apps from the ServiceNow Store. See [Playbook Experience apps](https://store.servicenow.com/sn_appstore_store.do#!/store/product/e4cecaf0db2be81079279ee4db9619f2).

Role required: ui\_builder\_admin, admin

## About this task

After creating a UI Builder page, you can customize Playbook Experience pages to your needs. Page templates include controllers that can be used with component presets, including the playbook templates. See [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open the **UI Builder** experience that you want to work in, or create a new experience.

    The **Playbook Experience Builder** experience was built for you to customize Playbook Experience. For more information on how to create an experience, see [Configure how users interact with your applications in UI Builder](https://www.servicenow.com/docs/access?context=work-experiences&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

3.  In your **UI Builder** experience, you can:

    -   [Create a page from scratch](https://www.servicenow.com/docs/access?context=create-page&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US),
    -   [create a page from a **Standard record** template](https://www.servicenow.com/docs/access?context=reuse-page-definitions&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US),
    -   or create a page from a Playbook Experience template.
    Using a Playbook Experience template speeds up the development process, because the Playbook Custom Layout UI Controller and components are already added to every page, including record generators as of version 25.2. The controller automatically populates all the provided components with data.

    **Note:** You can still create and add custom components when you use a template.

    ![Select a playbook template.](../image/playbook-select-template.png)

4.  If you're using a Playbook Experience template, **Create** your page.

    1.  Set up the page details.

<table id="table_vlg_vc3_q1c"><tbody><tr><td>

**Name**

</td><td>

The name of your page.

</td></tr><tr><td>

**URL Path**

</td><td>

The URL path that users navigate to, to access the page.

</td></tr></tbody>
</table>    2.  Review the testing parameters for your page.

<table id="table_h3s_1d3_q1c"><tbody><tr><td>

**table**

</td><td>

Name of the parent table for the playbook.

</td></tr><tr><td>

**sysID**

</td><td>

Sys\_id of the record. For a record that doesn't exist, the value is **-1**.

</td></tr><tr><td>

**experience**

</td><td>

The experience you want to load.

</td></tr><tr><td>

**selectedPlaybook**

</td><td>

The playbook the agent or fulfiller is in.

</td></tr><tr><td>

**selectedStage**

</td><td>

The stage the agent or fulfiller is in.

</td></tr><tr><td>

**selectedActivity**

</td><td>

The activity the agent or fulfiller is in.

</td></tr></tbody>
</table>    3.  Set up your default page variant.

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
</table>    4.  Open the default page variant you just created.

    The new Playbook Experience layout already includes controllers and components populated with data, but there are a few more configurations to make. To make the remaining configurations, go to step 6.

5.  If you used the **Standard record** template or created your page from scratch, add the Playbook Custom Layout UI Controller to the page.

    1.  From the bottom corner of your new page, select the data icon \(![Data icon.](../image/playbook-data-resource-icon.png)\)

    2.  Select **+ Add**.

    3.  Search for "Playbook".

    4.  Under **Data resources**, select **Playbook Custom Layout UI Controller** and click **Add**.

    5.  Exit the **Data resources** panel.

6.  Configure the Playbook Custom Layout UI Controller you just added.

    1.  To allow users to create a new record in this customized Playbook Experience instead of the standard new record form, select a test value pill in the upper left.

        The test values popover opens.

    2.  Make sure the **sysID** test value is set to **-1**, and select **Apply**.

        ![Test values for your playbook experience, with the table and sysID.](../image/playbook-sysID-update.png)

        A record generator form is available when you open the preview. You should be able to test the record generator form and confirm that new records are created.

    3.  You can also update the **table** name or any of the optional parameters:

    4.  If you want to hard-code the test values instead, navigate back to **Data** &gt; **Data resources panel** &gt; **Local data resource instances**, and select **UI Controller Record Page**.

    5.  Under the **Config** tab of the controller, add the **Parent SysID** or **Parent Table**. In the test values popover, these are the **sysID** and **table** fields.

        You can enter **context.props.table** in the **Parent Table** field, and **context.props.sysId** for the **Parent SysID** field.

        **Note:** Make sure whatever table or record you enter has a playbook.

    6.  Add the **Playbook Experience** you want to use.

    7.  Enter values for the other fields, if needed.

<table id="table_xys_tlb_t1c"><tbody><tr><td>

**Activity View Mode**

</td><td>

View mode used to render Playbook activities in stacked or focused mode

</td></tr><tr><td>

**Record Generator Query**

</td><td>

Encoded Query string to optionally override the query provided for a record generator

</td></tr><tr><td>

**Selected Playbook Context ID**

</td><td>

Optional context ID of selected playbook for deep linking

</td></tr><tr><td>

**Selected Stage Context ID**

</td><td>

Optional context ID of selected stage for deep linking

</td></tr><tr><td>

**Selected Activity Context ID**

</td><td>

Optional context ID of selected activity for deep linking

</td></tr></tbody>
</table>    8.  In the Outputs column, you can select the values you want to hard-code.

    The controller is configured and you're ready to add playbook components.

7.  Add playbook components.

    1.  In the component tree, select the **Main Tab**.

        The **Main Tab** panel opens on the right.

    2.  In the **Main Tab** panel, select **+ Add**.

        A modal asking "How do you want to build this tab?" displays.

    3.  Select **Start from an empty container** and click **Next**.

        A **Tab Settings** modal displays.

    4.  Give your tab a name and an icon, and click **Create**.

        The tab is added to the component tree and a blank canvas displays.

    5.  In the component tree, under your new tab, select **+ Add component** and search for "resizable".

    6.  Select the **Resizable panes** component, give it a name, and click **Create**.

    7.  In the component tree, open the new **Resizable panes** component you just created.

        The panel for your new **Resizable panes** opens on the right.

    8.  Configure as needed, and click **Save** in the upper right corner.

    9.  To add the stage picker, find your new **Resizable panes**component in the component tree, and select **+ Add component** under **left**.

    10. In your component tree, select the new stage picker.

        The panel for your new stage picker opens on the right.

    11. Select the preset for this component from the Playbook Custom Layout UI Controller, and click **Save** in the upper right corner.

        ![Choose a preset for the component.](../image/playbook-stage-picker.png)

        A confirmation message is displayed, and the component inputs and events under the **Events** tab in the stage picker panel is auto-populated.

        ![Component configuration.](../image/playbook-stage-picker-confirm.png)

    12. To add the **Playbook Activity Viewer**, find your **Resizable panes**component in the component tree, and select **+ Add component** under **right**.

    13. Repeat steps 7j and 7k.

    14. To add the **Playbook Modals**, find the tab you created under the **Main Tab** in the component tree, and select **+ Add component**.

    15. Repeat steps 7j and 7k for the **Playbook Modals**.

    16. Navigate back to the **Playbook Stage Picker**, and determine the orientation of your stage picker.

    17. In the upper right corner, click **Open** to preview the playbook layout.

    18. Return to UI Builder.

    19. Navigate back to your stage picker in the component tree, and determine the orientation of your stage picker in the panel that opens on the right.


**Parent Topic:**[Customize the Playbook Experience](../concept/playbook-customize-playbook.md)

**Related topics**  


[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

