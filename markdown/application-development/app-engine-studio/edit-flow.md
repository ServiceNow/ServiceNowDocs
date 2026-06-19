---
title: Modify a flow
description: To update or change an existing flow for an app you built in App Engine Studio \(AES\), edit it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/app-engine-studio/edit-flow.html
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Add a flow from scratch, Add logic and automation, Enhance your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Modify a flow

To update or change an existing flow for an app you built in App Engine Studio \(AES\), edit it.

## Before you begin

Role required: sn\_app\_eng\_studio.user or delegated\_developer. For more information, see [Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/aes-app-dev-workflow.md).

Add logic and automation to your application. If you created an application using a template, logic and automation may already be added to your application. For more information on adding custom logic and automation, see [Add logic and automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/add-automation.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to a flow, select the menu icon \(\[Omitted image "menu-icon-purple.png"\] Alt text: Menu icon\) and then select **Edit**.

    \[Omitted image "aes-edit-flow-purple.png"\] Alt text: Select to edit a flow

    **Note:** When a flow is triggered by a record being created or updated in a data table, it's referred to as a record-based flow. Record-based flows display in the list of logic and automation with a distinct icon \(\[Omitted image "record-flow-icon.png"\] Alt text: Record-based flow.\). These flows open up within the **Flows** tab in Table Builder if you are licensed for Table Builder for App Engine and have it installed. Contact your account team for details. For more information on flows functionality in Table Builder, see [Flows in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/flows-tb.md).

4.  Take the appropriate actions to edit the flow.

<table id="choicetable_opd_n4h_x1b"><tbody><tr><td id="d121331e187">

**Change the flow name, description, or roles**

</td><td>

In the main header, select **Properties**, enter the values you want into the appropriate fields, and then select **Update**.

</td></tr><tr><td id="d121331e202">

**To edit the trigger**

</td><td>

In your flow, select the trigger description, fill in the fields as desired, and then select **Done**.**Note:** Modifying triggers can result in the deletion of referenced action configurations.

</td></tr><tr><td id="d121331e217">

**To edit an existing action**

</td><td>

In your flow, select the action description, fill in the fields as desired, and then select **Done**.

</td></tr><tr><td id="d121331e229">

**To add a new action**

</td><td>

In your flow, select the plus icon in the ACTION section, then proceed as you would for adding an action to a new flow.

</td></tr></tbody>
</table>    For more information on editing flows, see Edit a flow.

5.  To save your changes, select **Save**.


## What to do next

Test a flow to make certain it works the way you expect. For more information on testing flows, see Test a flow.

**Parent Topic:**[Add a flow from scratch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/create-scratch-flow.md)

