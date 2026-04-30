---
title: Setup metric definition and entity-mapping records
description: Configure your environment so that values extracted using the Document Intelligence for Utility Invoices skill are mapped to the correct Environmental, Social, and Governance metrics and entities. This eliminates manual data entry and improves accuracy.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-26"
reading_time_minutes: 3
breadcrumb: [Activate document intelligence for utility invoices skill, Configure, Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Setup metric definition and entity-mapping records

Configure your environment so that values extracted using the Document Intelligence for Utility Invoices skill are mapped to the correct Environmental, Social, and Governance metrics and entities. This eliminates manual data entry and improves accuracy.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

-   Preconfigured metric definitions with corresponding entity mappings are provided to simplify the initial setup for Now Assist for Operational Sustainability Management. The four preconfigured metric definitions are water, waste, electricity, and natural gas consumption.
-   If the preconfigured metric definitions don’t meet your requirements, you can create a new or use an existing metric definition. Then update the Metric Definition table and create or update mapping records to link the new definition to the appropriate record identifiers. When using custom metric definitions, confirm that all relevant mapping records are updated to reference the new definitions for accurate data association.
-   The metric definition must be activated before using the Document Intelligence for Utility Invoices skill.

Once the metric definitions and entity mappings have been configured, you can begin extracting information from utility invoices. The system then uses the configured mappings to determine where the extracted data should be stored. The extracted utility type \(for example, electricity\) is matched to the correct metric definition based on the metric definition mapping, and the billing address or service address is used to identify the relevant organizational entity via the entity mapping. This process verifies that the extracted consumption or bill amount is accurately assigned to the right metric and entity, streamlining data collection and eliminating manual data entry.

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Metrics** &gt; **Automated metric definitions**.

2.  Select the filter icon and select **Advanced view**.

3.  Build a filter by selecting **Group**, **is**, **Document Intelligence for Utility bills** and select **OK**.

4.  Select a metric definition and select **Details** tab.

5.  On the form, fill in the fields.

    For information on the fields of the form, see [Automated metric definition fields](../../metrics/reuse/automated-metric-definition-fields.md).

6.  Select **Entities** tab and add the entities related to your organization for which you want to collect data.

    **Note:** Repeat the steps before this note for each metric definition you must activate.

7.  Select **Save**.

8.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Administration** &gt; **Entity Mapping**.

9.  Select **New**.

10. On the form, fill in the fields.

<table id="table_inv_xk2_fvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record identifier

</td><td>

A unique record identifier of the entity from which the data is mapped. The identifier should typically be the billing address or service address.

</td></tr><tr><td>

Related record

</td><td>

Entity record associated with the metric definition to be mapped.

</td></tr><tr><td>

Additional information

</td><td>

Field used to specify the information that must be filled in by the administrator. Certain fields such as **Entity class** and **Entity owner** must be manually filled.

</td></tr><tr><td>

State

</td><td>

Review state. Based on the information provided in the **Additional information** field, the administrator must fill in the required information and then change the state of this field. The choices are as follows.-   **No review required**: Use this option when there are no fields to be filled in the entity record by the administrator.
-   **Review required**: Use this option if the administrator must fill some fields in the entity record.
-   **Reviewed**: Use this option if the administrator has already provided the information in the specified fields in the entity records.
 This field is automatically set to **No review required**. You must change the state to **Reviewed** after you provide the information.

</td></tr></tbody>
</table>11. Select **Submit**.


**Parent Topic:**[Activate the document intelligence for utility invoices skill](../concept/activate-the-document-intelligence-for-utility-invoices-skill.md)

