---
title: Add change processing support for an Azure resource type
description: Add Azure change processing support for an Azure resource type per the needs of your organization.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-02-12"
reading_time_minutes: 1
breadcrumb: [Azure change processing, Discovery for Microsoft Azure Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Add change processing support for an Azure resource type

Add Azure change processing support for an Azure resource type per the needs of your organization.

## Before you begin

Role required: discovery\_admin or cloud\_root\_admin

## About this task

This procedure is applicable only for Discovery and Service Mapping Patterns store versions that are older than 1.21.0. Starting the 1.21.0 version, all supported resource types are listed in the ACP Resource Type table. All the resource types are activated by default. The MID Server property **mid.cmp.azure.event.supported\_resource\_types** is no longer available. You can use the ACP Resource Type table to add an entry for a resource type and to add a query. For information on adding a query see the "Example VM Query" section in [KB1705862](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705862).

To add change processing supports for an Azure resource type in legacy versions, add the resource types to the **mid.cmp.azure.event.supported\_resource\_types** property. As a comma-separated value. Then, create response mappings between the change fields and the Configuration Item \(CI\) fields. Response mappings define a one-on-one mapping between the source data fields and the CI fields. Azure change processing uses the mapping information to update resource change data in the appropriate CI class fields.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  Open the **mid.cmp.azure.event.supported\_resource\_types** property.

3.  In the **Value** field, add the Azure resource type as a comma-separated value.

4.  Select **Update**.

5.  Create response mappings for the change fields that you want to update in the Configuration Management Database \(CMDB\).

    1.  Navigate to the Response Mapping \[sn\_cmp\_response\_mapping\] table.

        `https://<instance name>.service-now.com/sn_cmp_response_mapping_list.do`

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_wly_xpj_5wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI class

</td><td>

Name of the CI class that represents the Azure resource in the CMDB.

</td></tr><tr><td>

Datasource

</td><td>

Name of the input datasource.Set the Datasource field to Azure Resource Changes.

</td></tr><tr><td>

CI class fields

</td><td>

Name of the CI class field that is the logical equivalent of the source field.

</td></tr><tr><td>

Source field

</td><td>

Name of the source field that you want to update in the specified CI class field.

</td></tr></tbody>
</table>        For more information on response mapping, see [Using response mapping](https://www.servicenow.com/community/itom-articles/cmp-using-response-mapping-how-to-populate-cmdb-using-cmp/ta-p/2323213) topic in the ServiceNow Community.

    4.  Select **Submit**.

    5.  Repeat steps [5.b](add-change-processing-support-azure-resource-type.md#step-create-response-mapping) to [5.d](add-change-processing-support-azure-resource-type.md#step-submit-response-mapping) for all the change fields that you want to update in the CMDB.


