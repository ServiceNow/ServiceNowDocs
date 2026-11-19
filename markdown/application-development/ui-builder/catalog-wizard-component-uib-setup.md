---
title: Catalog Wizard component setup
description: The Catalog Wizard simplifies the process of building a complex input form that is similar to the item authoring experience in Catalog Builder. Designers can also create and configure custom actions for Service Catalog Wizards using declarative actions.Define the Catalog Wizard component properties in these categories: Wizard, Template and record, and Button.Select event handlers to configure the events provided with the Catalog Wizard component. Event handlers work with data resources to link the Catalog Wizard actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/catalog-wizard-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Catalog Wizard component setup

The Catalog Wizard simplifies the process of building a complex input form that is similar to the item authoring experience in Catalog Builder. Designers can also create and configure custom actions for Service Catalog Wizards using declarative actions.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin, wizard\_admin, and ui\_builder\_admin

## Procedure

1.  Define a label for Catalog Wizard that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).\[Omitted image "catalog-wizard-content.png"\] Alt text: Shows the Catalog Wizard component by name in the UI Builder content tree

2.  Select the Catalog Wizard component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    When you select the component, the property fields and events appear in the Config tab in the setup panel on the right.\[Omitted image "catalog-wizard-properties.png"\] Alt text: Shows the Config panel and the Catalog Wizard properties


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Catalog wizard component properties

Define the Catalog Wizard component properties in these categories: Wizard, Template and record, and Button.

The Config tab in the Setup panel displays the available properties that can be configured.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### Wizard properties

Select the wizard and determine how it will be displayed.

<table id="table_sjc_clg_rvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select wizard\[sysId\]

</td><td>

Reference property that selects the wizard to be rendered.

</td></tr><tr><td>

Wizard mode\[mode\]

</td><td>

Catalog wizard can also be used to create/edit Catalog Templates. Use the following criteria for selecting a mode:-   When creating/editing templates, the mode should be **Template**.
-   When creating/editing records via wizard the mode should be **Normal**.

 Default value: **Normal**

</td></tr><tr><td>

Field Space\[fieldSpace\]

</td><td>

Spacing between questions inside wizard section.

</td></tr></tbody>
</table>### Template and record properties

Select the SysIDs of the template and the record to use.

<table id="table_gw1_wb5_tvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sys Id of the record\[recordId\]

</td><td>

Sys Id of the record being opened in wizard.

</td></tr><tr><td>

Select template\[templateId\]

</td><td>

Select the template record to apply. When a proper Catalog template record ID is given, the template data/behavior is loaded on to the wizard.This property is applicable only in **Normal** mode

</td></tr><tr><td>

Make template mandatory\[isTemplateMandatory\]

</td><td>

If set to **true**, a valid template has to be selected for entity creation.Default: **false**

</td></tr></tbody>
</table>### Button properties

Configure the appearance and behavior of the buttons in the wizard.

<table id="table_zfw_xc5_tvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Home Button icon\[homeButtonIcon\]

</td><td>

Icon that appears in place of the home button at the top of theCatalog Wizard.

</td></tr><tr><td>

Home Button Tooltip\[homeButtonTooltip\]

</td><td>

Content of a custom tooltip for the home button icon.

</td></tr><tr><td>

Hide Home button\[hideHomeButton\]

</td><td>

If **true**, hides the home button.Default: **false**

</td></tr><tr><td>

Hide step navigator Back button\[hideBackButton\]

</td><td>

If **true**, hides the backwards step navigator button in the Catalog Wizard footer.Default: **true**

</td></tr><tr><td>

Hide step navigator Forward button\[hideForwardButton\]

</td><td>

If true, hides the forward step navigator button in the Catalog Wizard footer.Default: **false**

</td></tr><tr><td>

Step navigator forward button type\[forwardButtonType\]

</td><td>

Selects either a primary or secondary button type for the step navigator forward button. The default type is **Primary**.

</td></tr></tbody>
</table>## Catalog wizard component events

Select event handlers to configure the events provided with the Catalog Wizard component. Event handlers work with data resources to link the Catalog Wizard actions to the data you want to display to your users.

The Events tab shows the events used by the Catalog Wizard component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Catalog Wizard actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Request Generated|Dispatched when the wizard submits a form.|
|Redirect to home page|Dispatched when the user confirms redirection to the home page by selecting the **Home** button.|
|Wizard title changed|Dispatched when the title of the wizard changes.|

### Declarative Actions

The Catalog Wizard component supports declarative actions. Only declarative actions of type **UXF Client Action** can be mapped to page level handled events in UI Builder.

