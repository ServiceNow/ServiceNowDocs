---
title: Display ServiceNow cases on an Adobe Experience Manager page
description: Use case components available within Adobe Experience Manager \(AEM\) to access customer service cases from the ServiceNow instance and display them on an AEM-based website.
locale: en-US
release: zurich
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 6
breadcrumb: [Integrating with Adobe Experience Manager, Integrate, Customer Service Management]
---

# Display ServiceNow cases on an Adobe Experience Manager page

Use case components available within Adobe Experience Manager \(AEM\) to access customer service cases from the ServiceNow instance and display them on an AEM-based website.

## Before you begin

Define the cross-origin resource sharing \(CORS\) rule to access the Case API and CSM Attachment API from your AEM instance. For more information, see [Define a cross-origin resource sharing rule \(CORS\) to access ServiceNow API endpoints from AEM](../concept/aem-integration-setup.md#).

Role required: AEM author

## About this task

The Case REST API enables you to create, retrieve, and update customer service case records. For more information, see [Case API](https://www.servicenow.com/docs/access?context=case-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

The CSM Attachment API enables you to upload, download, and remove attachments associated with customer service cases and to retrieve attachment metadata. For more information, see [CSM Attachment API](https://www.servicenow.com/docs/access?context=attachment_csm-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Procedure

1.  Log in to your AEM instance.

2.  Open your AEM page in [Edit mode](https://helpx.adobe.com/in/experience-manager/6-5/sites/authoring/using/author-environment-tools.html#main-pars_title_20).

3.  Open the [components browser](https://helpx.adobe.com/in/experience-manager/6-5/sites/authoring/using/author-environment-tools.html#main-pars_title_17).

4.  From the **All** list, select **ServiceNow**.

5.  Drag a component to the required position on the page.

    **Note:** If components are not available, update your template configuration to include the case components. In addition, you must modify the properties of the site template and add each case component to the list of allowed components.

6.  Open the [component dialog for editing](https://helpx.adobe.com/in/experience-manager/6-5/sites/authoring/using/editing-content.html#ComponentEditDialog).

    **Note:** The case components in the Edit mode of a page in AEM are accessible to all users, including public users. Public users are anonymous AEM users who are not logged in.

7.  Set the Case Cards component properties to display all open customer service cases from your ServiceNow instance as column cards.

<table id="table_kx2_4q2_tkb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td id="component-title">

Title

</td><td id="component-title-desc">

Title of this component that appears on the AEM page.

</td></tr><tr><td id="component-column-label">

Label parameters

</td><td id="component-column-label-desc">

Comma-separated label parameters for Case \[sn\_customerservice\_case\] table columns. Each parameter is specified in the format `*label*:*column*`. Where *label* is displayed on the component and *column* is the name of a column from the Case \[sn\_customerservice\_case\] table.Example: `Number:number,Priority:priority,Product:product`

</td></tr><tr><td id="component-case-list">

Case list page URL

</td><td id="component-case-list-desc">

Relative URL of the case list page to redirect to. Example: `/content/servicenow/en/now_case_list.html`

</td></tr><tr><td id="component-view-case">

Case view page URL

</td><td id="component-view-case-desc">

Relative URL of the case view page to redirect to. Example: `/content/servicenow/en/now_case_view.html`

</td></tr><tr><td>

Hide component for no cases

</td><td>

Option to hide the component when there are no cases to display.

</td></tr><tr><td id="component-custom-css">

Custom CSS class

</td><td id="component-custom-css-desc">

Custom CSS class for applying custom styles to this component. For more information, see [Customizing the colors of ServiceNow components in AEM](../concept/aem-style-components.md#).

</td></tr></tbody>
</table>8.  Set the New Case component properties for users to create a customer service case in your ServiceNow instance from your AEM page.

<table id="table_abr_rbk_cmb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of this component that appears on the AEM page.

</td></tr><tr><td>

Short description label

</td><td>

Label for the field to enter a brief description of the case.

</td></tr><tr><td>

Description label

</td><td>

Label for the field to enter a description of the case.

</td></tr><tr><td>

Product label

</td><td>

Semicolon-separated parameters to define the label and the placeholder text for the product list.

</td></tr><tr><td>

Asset label

</td><td>

Semicolon-separated parameters to define the label and the placeholder text for the asset list

</td></tr><tr><td>

Number of list items

</td><td>

Maximum number of items to include in the product and asset lists.Use the increment or decrement icons to increase or decrease the values. You can also manually enter a value. The value must be greater than `1`.

</td></tr><tr><td>

Show assets

</td><td>

Option to display the asset list on the component.

</td></tr><tr><td>

Case list page URL

</td><td>

Relative URL of the case list page to redirect to. Example: `/content/servicenow/en/now_case_list.html`

</td></tr><tr><td>

Case view page URL

</td><td>

Relative URL of the case view page to redirect to. Example: `/content/servicenow/en/now_case_view.html`

 **Note:** You need to enter a value for this property to navigate to the case view page from the Case created window.

</td></tr><tr><td>

Attachment file size limit in MB

</td><td>

Maximum size limit for an attachment file that can be added to a case.

</td></tr><tr><td>

Custom CSS class

</td><td>

Custom CSS class for applying custom styles to this component. For more information, see [Customizing the colors of ServiceNow components in AEM](../concept/aem-style-components.md#).

</td></tr></tbody>
</table>9.  Set the Case View component properties to display customer service cases and any comments and attachments, if available, from a ServiceNow instance.

<table id="table_tfp_h4q_tkb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case parameter

</td><td>

Name of the URL query parameter for the case number. Example: `case_no`

</td></tr><tr><td>

Label parameters

</td><td>

Comma-separated label parameters for Case \[sn\_customerservice\_case\] table columns. Each parameter is specified in the format `*label*:*column*`. Where *label* is displayed on the component and *column* is the name of a column from the Case \[sn\_customerservice\_case\] table.Example: `Number:number,Priority:priority,Product:product`

</td></tr><tr><td>

Activities count

</td><td>

Maximum number of activities such as comments and attachments to be displayed on the Activity tab.Use the increment or decrement icons to increase or decrease the values. You can also manually enter a value. The value must be greater than `1`.

</td></tr><tr><td>

Attachment file size limit in MB

</td><td>

Maximum size limit for an attachment file that can be added to a case.Use the increment or decrement icons to increase or decrease the values. You can also manually enter a value. The value must be greater than `1`.

</td></tr><tr><td>

Article page URL

</td><td>

Relative URL of the article page to redirect to.Example: `/content/servicenow/en/now_article_view.html`

**Note:** If an article link is included in a case, you need to enter a value for this property to navigate to the knowledge article view page from the case.

</td></tr><tr><td>

Custom CSS class

</td><td>

Custom CSS class for applying custom styles to this component. For more information, see [Customizing the colors of ServiceNow components in AEM](../concept/aem-style-components.md#).

</td></tr></tbody>
</table>10. Set the Case List component properties to display a list of customer service cases.

<table id="table_ywq_wbr_tkb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of this component that appears on the AEM page.

</td></tr><tr><td>

Label parameters

</td><td>

Comma-separated label parameters for Case \[sn\_customerservice\_case\] table columns. Each parameter is specified in the format `*label*:*column*`. Where *label* is displayed on the component and *column* is the name of a column from the Case \[sn\_customerservice\_case\] table.Example: `Number:number,Priority:priority,Product:product`

</td></tr><tr><td>

Case count

</td><td>

Maximum number of cases to display on the component.Use the increment or decrement icons to increase or decrease the values. You can also manually enter a value. The value must be greater than `1`.

 The maximum value you can enter for this field is 50.

</td></tr><tr><td>

Show create case

</td><td>

Option to display the button to create a case on the component.

</td></tr><tr><td>

Create case button label

</td><td>

Label for the button to create a case.

</td></tr><tr><td>

Case create page URL

</td><td>

Relative URL of the case create page to redirect to.Example: `/content/servicenow/en/now_case_create.html`

</td></tr><tr><td>

Case view page URL

</td><td>

Relative URL of the case view page to redirect to.Example: `/content/servicenow/en/now_case_view.html`

</td></tr><tr><td>

Custom CSS class

</td><td>

Custom CSS class for applying custom styles to this component. For more information, see [Customizing the colors of ServiceNow components in AEM](../concept/aem-style-components.md#).

</td></tr></tbody>
</table>
