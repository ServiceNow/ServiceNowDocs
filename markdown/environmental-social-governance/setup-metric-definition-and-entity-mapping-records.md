---
title: Setup metric definition and entity-mapping records
description: Configure your environment so that values extracted using the Document Intelligence for Utility Invoices skill map to the correct Environmental, Social, and Governance metrics and entities. This eliminates manual data entry and improves accuracy.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Activate document intelligence for utility invoices skill, Configure, Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Setup metric definition and entity-mapping records

Configure your environment so that values extracted using the Document Intelligence for Utility Invoices skill map to the correct Environmental, Social, and Governance metrics and entities. This eliminates manual data entry and improves accuracy.

## Before you begin

Before configuring entity mappings, verify that organizational entity records exist for each location you want to collect utility data from. Identify the billing and service addresses used in your utility bills so you can match them to entity records during setup.

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

-   Preconfigured metric definitions with corresponding entity mappings are provided to simplify the initial setup for Now Assist for Operational Sustainability Management. The four preconfigured metric definitions are water, waste, electricity, and natural gas consumption. These metric definitions are active by default, no additional activation step is required for the preconfigured definitions.
-   If the preconfigured metric definitions don’t meet your requirements, you can create or use an existing metric definition. Then update the Metric Definition table and create or update mapping records to link the new definition to the appropriate record identifiers. When using custom metric definitions, confirm that all relevant mapping records are updated to reference the new definitions for accurate data association.
-   The metric definition must be activated before using the Document Intelligence for Utility Invoices skill.

The metric definitions are only one part of the setup. The entity mapping table ships empty and must be populated before the skill can route extracted data. For each billing or service address in your utility invoices, create an entity mapping record that links the address to the corresponding organizational entity. Once the metric definitions and entity mappings are both configured, the system uses them to determine where extracted data belongs. The extracted utility type \(for example, electricity\) is matched to the correct metric definition based on the metric definition mapping, and the billing or service address identifies the relevant organizational entity. The extracted consumption or bill amount is then assigned to the correct metric data task.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Metrics** &gt; **Automated metric definitions**.

2.  Select the filter icon and select **Advanced view**.

3.  Build a filter by selecting **Group**, **is**, **Document Intelligence for Utility bills** and select **OK**.

4.  Select a metric definition and select **Details** tab.

5.  On the form, fill in the fields.

    For information on the fields of the form, see [Automated metric definition fields](../../metrics/reuse/automated-metric-definition-fields.md).

6.  Select the **Entities** tab and add the entities related to your organization for which you want to collect data.

    **Note:** Repeat the steps before this note for each metric definition you must activate.

7.  Select **Save**.

    After activating all required metric definitions, create entity mapping records to link the billing and service addresses on your utility invoices to the corresponding organizational entities in your instance.

8.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Administration** &gt; **Entity Mapping**.

    **Note:** The Entity Mapping table is empty by default. Create a record for each billing or service address that appears on your utility invoices before using the Document Intelligence for Utility Invoices skill.

9.  Select **New**.

10. On the form, fill in the fields.

<table id="table_inv_xk2_fvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record identifier

</td><td>

Exact billing or service address as it appears on the utility bill. The value must match character-for-character, including spacing, punctuation, and capitalization. For example, if the bill prints the address as “1201 W Lake Street Unit 4”, enter that exact string. A partial or differently formatted address doesn’t match and the extracted data isn’t routed to any entity.

</td></tr><tr><td>

Table

</td><td>

Automatically set to Entity \[sn\_grc\_profile\]. No action required.

</td></tr><tr><td>

Related record

</td><td>

Organizational entity record corresponding to the billing or service address, such as a facility, building, or business unit that owns or occupies the location in Record identifier. When a utility bill is processed, the system assigns the extracted data to this entity’s metric data task.

</td></tr><tr><td>

Additional information

</td><td>

Field used to specify information that must be filled in by the administrator. Certain fields such as **Entity class** and **Entity owner** must be manually filled. The system may populate this field with entity record fields that require completion. Review this field and update the entity record before changing the State field.

</td></tr><tr><td>

State

</td><td>

Review state. Based on the information provided in the **Additional information** field, the administrator must fill in the required information and then change the state of this field. The choices are as follows.-   **No review required**: Use this option when there are no fields to be filled in the entity record by the administrator.
-   **Review required**: Use this option if the administrator must fill some fields in the entity record.
-   **Reviewed**: Use this option if the administrator has already provided the information in the specified fields in the entity records.
 This field is automatically set to **No review required**. You must change the state to **Reviewed** after you provide the information.

</td></tr></tbody>
</table>11. Select **Submit**.


## Example

An uploaded electricity bill contains a $416 charge and lists the service address as “1201 W Lake Street, Unit 4”. If an entity mapping record exists with Record identifier set to “1201 W Lake Street, Unit 4” and Related record set to the “Chicago Office” entity, the system automatically assigns the $416 charge to that entity’s electricity metric data task. Without the entity mapping record, the system can’t determine where to route the extracted data.

**Parent Topic:**[Activate the document intelligence for utility invoices skill](../concept/activate-the-document-intelligence-for-utility-invoices-skill.md)

