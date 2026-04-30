---
title: Flow Template Builder
description: Enable citizen developers to create their own flow templates. Flow Templates guide flow authors to create flows for common use cases. Use the flow template builder to define flows, actions, and flow template variables.Create template from a flow in Workflow Studio to guide flow authors through the creation of a flow with the same configuration and customized template input values for the components.Create a flow from an existing App Engine Studio automation template. Follow the template guidance to provide values for template inputs that accept dynamic data.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Building flows, Use, Workflow Studio, Build workflows]
---

# Flow Template Builder

Enable citizen developers to create their own flow templates. Flow Templates guide flow authors to create flows for common use cases. Use the flow template builder to define flows, actions, and flow template variables.

Template authors can create templates from the flow with the required configurations, in Workflow Studio. Template authors can view or edit an existing flow template in Flow Template Builder.

![Flow Template Builder UI.](../images/flow-temp-ui.png "Flow Template Builder UI")

In App Engine Studio, administrator can add automations in the required app by creating flows using these active templates.![Create flow from template in App Engine Studio.](../images/template-add-automation.png)

**Parent Topic:**[Building flows](flows.md)

## Create a template using Flow Template Builder

Create template from a flow in Workflow Studio to guide flow authors through the creation of a flow with the same configuration and customized template input values for the components.

### Before you begin

-   Activate the App Engine Studio \(sn\_app\_eng\_studio\) and [Flow Template Builder \(sn\_flow\_template\)](https://store.servicenow.com/sn_appstore_store.do#!/store/application/dfe6fd01594b70605a943e33c8087226) plugins.
-   Create a flow in Workflow Studio as per your requirement.
-   Role required: App Template Author or admin

    **Note:** Users with the App Template Author cannot create flow templates in the **Global** scope. They can create flow template in only those scopes to which they have access.


### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  In Workflow Studio, open the required flow.

3.  Click the more actions icon \(![More actions icon.](../images/MoreActionsIcon.png)\) and select **Save flow as a template**.

    ![Save flow as a template.](../images/template-save.png)

4.  In the Save flow as template dialog, enter **Template name** and select **Application** in which you want the template.

    ![Details of template.](../images/template-save-as.png)

5.  Click **Save**.

    The template is created and is displayed in Flow Template Builder.

    ![Created template.](../images/template-designer.png)

6.  In **View**, select **Template setup**.

    ![Template setup view](../images/template-setup.png)

    Template is loaded in Flow Template Builder.

    When **View** is changed to **Flow**, the template is displayed in the Workflow Studio UI.

7.  Click the required action and select the required inputs.

    ![Template inputs.](../images/template-coll-vals.png)

<table id="table_e3r_krb_5rb"><thead><tr><th>

Choice

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use default value

</td><td>

Uses the default value provided in flow.

</td></tr><tr><td>

Collect new user input

</td><td>

Creates a template variable. Expand the template variable to configure the user input as per your requirement.![Collect new user input.](../images/templates-coll-usript.png)

 **Note:** Input variable once created, cannot be deleted.

</td></tr><tr><td>

Use template variable

</td><td>

Uses the template variable that has been collected in a previous action. Click the data picker to use the previously collected user input.![Data picker.](../images/template-data-picker.png)

In this example, **Price** is collected as a user input and this user input is used in the **Message** input of the **Log** action.![Use template variable.](../images/template-var.png)

</td></tr></tbody>
</table>    **Note:** Supported template variable data types:

    -   String
    -   List
    -   Choice
    -   Reference
    -   Table Name
    -   URL
    -   Multi Line Small Text Area
    -   Two Line Text Area
    -   Price
    -   Email
    -   Integer
8.  Click **Save**.

    The flow template is created.

    To verify if the template record is created, type `sys_app_template.list` in the left navigator pane and search for the template you had created.

9.  Click **Activate**.

    **Note:**

    -   While configuring the properties in Flow template properties dialog, ensure that you select the **Icon** first before you enter other fields and click **Update**.
    -   **Icon** in the Flow template properties supports only .SVG files.

## Create a flow from a template in App Engine Studio

Create a flow from an existing App Engine Studio automation template. Follow the template guidance to provide values for template inputs that accept dynamic data.

### Before you begin

-   [Create a template using Flow Template Builder](flow-template.md#) and activate it.

    **Note:** If the template is modified, the template must be activated again for the changes to be reflected in App Engine Studio.

-   Role required: Template Runner

### Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  In **My recent apps**, select the required app.

    If you haven't created an app, you can create it.

    The app is opened in App Engine Studio.

3.  Click **Logic and automation**.

4.  Click **Add**.

    ![Add automation to an app.](../images/template-app.png)

5.  Select the required flow template.

6.  In the template dialog, click **Begin**.

7.  In the templates wizard, provide the inputs to create flow using the template.

    ![Template wizard.](../images/template-wizard1.png)

    ![Template wizard.](../images/template-wizard2.png)

    After providing the required inputs, a confirmation message is displayed that the flow is created.

8.  To edit the flow in Workflow Studio, click **Edit this flow**.

    The flow is opened in Workflow Studio.

    **Note:**

    -   Avoid editing flows that are created from a template. If you intend to edit the flow, ensure that you test the flow before publishing it.
    -   In App Engine Studio, template inputs are not displayed in the same order as you had created in Workflow Studio. In this example, order in which fields appear in App Engine Studio is different from the order in which inputs are configured in Workflow Studio.

        ![Order of fields in Workflow Studio.](../images/ft-order.png "Input fields configured in Workflow Studio")

        ![Order of fields in App Engine Studio.](../images/ft-aes-order.png "Input fields displayed in App Engine Studio")

        **Note:** To configure the order in which fields are displayed in App Engine Studio and modify the displayed text such as title and heading, navigate to Template Wizards by typing `sys_app_template_wizard.list` in the left navigator pane and configure your template wizard as per your requirement.


