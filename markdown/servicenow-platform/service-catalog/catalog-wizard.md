---
title: Creating a Service Catalog Wizard
description: Service Catalog wizards help you to create wizard like, multi-step experiences.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Creating a Service Catalog Wizard

Service Catalog wizards help you to create wizard like, multi-step experiences.

## Before you begin

Service Catalog wizards are especially useful when the input required is huge and complex since the wizard offers a step-by-step experience for the requester and also provides a side panel to provide contextual help. A visa application is a good example where Service Catalog wizards could be used as the data needs to be presented in steps such as Personal details, Education details, and so on.

Pre-requisites for creating Service Catalog wizards:

-   Ensure that you have either a composite record producer, or a record producer set up. For more information, see [Create a record producer](t_DefRecProdInSCat.md).
-   The **Save options** field must have the value **Save in destination** in the composite record producer or record producer to enable the wizard to create records.
-   The **Allow edit** option should be selected on the composite record producer or record producer form so that records are editable in the wizard.

Role required: wizard\_admin, or admin

## About this task

The Service Catalog Wizard is available as a component in UI Builder \(UIB\). You can use it to create guided experiences backed by composite record producers or record producers. You can create multi-step wizard experiences using Service Catalog Wizard.

Service Catalog Wizards are used in these modes:

-   **Normal** mode: To create records in the table configured in the record producer, or the composite record producer associated with the wizard.
-   **Template** mode: To create a template where admins can predefine some data and provide guardrails to fine-tune and personalize the creation of records.

## Procedure

1.  Navigate to **Service Catalog Wizards** &gt; **Maintain Wizards**, and click **New** to create a new wizard.

2.  On the form, fill in the fields.

<table id="table_cqf_bgj_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the wizard.

</td></tr><tr><td>

**Type**

</td><td>

The wizard uses a composite record producer, or record producer.

</td></tr><tr><td>

**Producer**

</td><td>

Reference of the composite record producer, or record producer.

</td></tr><tr><td>

**Has feedback panel**

</td><td>

Option to specify if the wizard has a feedback panel.

</td></tr><tr><td>

**Layout**\[Stacked/Tabbed\]

</td><td>

The rendering of wizard steps can be either stacked or tabbed layout mode.

</td></tr><tr><td>

**Title**

</td><td>

Title of the wizard. **Note:** The title can also dynamically refer to the composite record producer, or record producer variables using $\{variable\} syntax.

</td></tr><tr><td>

**Enable Save**

</td><td>

Auto-save the wizard on each step change.

</td></tr><tr><td>

**Show review step**

</td><td>

The Review and submit step is displayed to summarize the wizard steps, and field values.

</td></tr><tr><td>

**Show Submit on last step**

</td><td>

If **true**, the **Submit** button is displayed in the last step.

</td></tr><tr><td>

**Review step label**

</td><td>

Label of the Review and submit step.

</td></tr></tbody>
</table>    For more information on fields, steps, sections, or questions on Service Catalog wizard, see the following:

    -   [Add a step, section, or question to a catalog item wizard](configure-the-catalog-builder-experience.md)
    -   [Catalog Wizard form](../reference/service-catalog-wizard-forms-field.md)
    ![Catalog Wizard form.](../image/wiztemplate_callouts.png)

    After you set up the field values, the resulting wizard with the steps, layout, labels, and other elements appear as follows:



3.  Set up the Catalog Wizard component properties using the UI Builder \(UIB\) components, for more information see Customize UI Builder pages using components.

    ![Service Catalog Wizard component configuration in UI Builder](../image/uib-wizardconfig.png)

    1.  **Select Wizard**: Select the wizard that you're creating the experience for \(you can choose the wizard you created in the previous step\).
    2.  **Wizard mode**: Select the mode for this experience.
    3.  **Field space**: Specify the spacing that should appear between fields in the wizard. The possible values are **Small**, **Medium**, **Large**, and **Extra Large**.
    4.  **Sys\_id of the record**: In Normal mode, the sys\_id of the record being edited or created by the wizard. In Template mode, the sys\_id of the template that is being edited.
    5.  **Select template**: Select the template that must be applied to the wizard. The **Select Template** option is applicable only in Normal mode.
    6.  **Make template mandatory**: If **true**, providing a template is mandatory for creating records, and is applicable only in Normal mode.
    7.  **Home button icon**: Select an icon that appears in place of the Home button icon.
    8.  **Hide home button**: If **true**, the **Home** button is hidden in the wizard.
    9.  **Hide step navigator Back button**: If **true**, hides the **Back** button in the footer of the wizard.
    10. **Hide step navigator Forward button**: If **true**, hides the **Forward** or **Continue** button in the footer of the wizard.
    11. **Step navigator forward button type**: Specify the button type for the **Forward** button in the wizard footer. The possible values are **Primary** or **Secondary**.
    For more information, see [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades) in the developer documentation site.


-   **[Create declarative actions for Service Catalog Wizards](declar-action-cw.md)**  
Create and configure declarative actions to enable administrators to configure buttons \(wizard actions\) in Service Catalog Wizards.

**Parent Topic:**[Service Catalog](../concept/service-catalog.md)

