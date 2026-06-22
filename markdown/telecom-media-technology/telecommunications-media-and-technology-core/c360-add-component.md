---
title: Add the Telecom Customer 360 component to a record page
description: Add the Telecom Customer 360 component to a record page in UI Builder so that customer service representatives can see the 360-degree consumer or account view in the context of the record they are working on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/c360-add-component.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Telecommunications Customer 360 component, Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Add the Telecom Customer 360 component to a record page

Add the Telecom Customer 360 component to a record page in UI Builder so that customer service representatives can see the 360-degree consumer or account view in the context of the record they are working on.

## Before you begin

Role required: sn\_telecom\_c360.admin

## About this task

Add the Telecom Customer 360 component as a dedicated tab on a record page in the CSM/FSM Configurable Workspace. The component displays configurable cards scoped to a single customer record. Cards cover customer contact details, products and services, billing, tasks, interaction history, data visualizations, and Now Assist AI insights.

**Note:**

-   After adding the component, you must also add the **Setup Customer360 Context** data resource to the page. This data resource resolves the record to the associated account or consumer. Without it, the component context cannot be determined. See [Add the Setup Customer360 Context data resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-add-data-resource.md).
-   The component can be only be added as a new tab on the record page. You can't embed it within an existing tab.

## Procedure

1.  Navigate to **All &gt; Now Experience Framework &gt; UI Builder**.

2.  Select **Experiences**.

3.  Select **CSM/FSM Configurable Workspace** from the list.

4.  Open any existing record page, or create a record page, add a tab to the page, and then add the **Telecom Customer 360** component.

    For detailed instructions on how to add a component, refer to the [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md) documentation.

5.  Add the Setup Customer360 Context data resource to enable the Telecom Customer 360 component to display the correct consumer or account view.

    See [Add the Setup Customer360 Context data resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-add-data-resource.md) for details.

6.  Configure the Telecom Customer 360 component properties.

    Set the following three properties. Leave all other component properties at their default values.

<table id="table_exz_d1f_kjc"><thead><tr><th>

Label

</th><th>

Name

</th><th>

Value

</th></tr></thead><tbody><tr><td>

**Table**

</td><td>

`Table`

</td><td>

Select the `table` output of the **Setup Customer360 Context** data resource.

</td></tr><tr><td>

**Sys ID**

</td><td>

`sysId`

</td><td>

Select the `sysId` output of the **Setup Customer360 Context** data resource.

</td></tr><tr><td>

**Card definition map**

</td><td>

`cardDefinitionMap`

</td><td>

A JSON object that maps each card key to the sys ID of the card definition record to display. See the following example:```
{
  "insights": "<sys_id_of_insights_card>",
  "contact": "<sys_id_of_contact_card>",
  "interaction": "<sys_id_of_interaction_history_card>",
  "billings": "<sys_id_of_billing_card>",
  "products": "<sys_id_of_products_card>"
}
```

</td></tr></tbody>
</table>    **Note:** The Card definition map uses the sysIds from the `sn_c360_dataconfig_card` table.


## Result

When you navigate to a record on the page where the component is added, the new tab displays the Telecom Customer 360 view for the account or consumer associated with that record. To change the cards that are displayed or the data shown on each card, update the card settings as described in [Configure the Telecommunications Customer 360 variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-configure-variables.md).

## What to do next

Add the Setup Customer360 Context data resource to the page. For more information, see [Add the Setup Customer360 Context data resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-add-data-resource.md).

**Parent Topic:**[Telecommunications Customer 360 component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecommunications-media-and-technology-core/c360-component.md)

