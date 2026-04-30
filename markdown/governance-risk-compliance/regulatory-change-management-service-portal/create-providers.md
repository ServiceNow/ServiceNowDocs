---
title: Configure a provider taxonomy configuration record
description: Align the provider with the appropriate taxonomy profile to categorize regulatory intelligence data and feeds for informational reporting purposes. This approach is particularly useful when integrating multiple feed sources, as it ensures consistent naming conventions across systems or applications.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the RSS feeds infrastructure, Configure, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Configure a provider taxonomy configuration record

Align the provider with the appropriate taxonomy profile to categorize regulatory intelligence data and feeds for informational reporting purposes. This approach is particularly useful when integrating multiple feed sources, as it ensures consistent naming conventions across systems or applications.

## Before you begin

Role required: sn\_grc\_reg\_change.admin

**Note:** Certain fields on this form are only visible if the **Default Taxonomy Configuration** property is set to **true**.

## Procedure

1.  Navigate to **Application** &gt; **Regulatory Change Management** &gt; **RSS Feeds** &gt; **Provider Taxonomy Configuration**.

2.  Select **New** on the page.

3.  On the form, fill in the fields.

<table id="table_mpb_j2x_4mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Provider of the taxonomy configuration record.

</td></tr><tr><td>

Default taxonomy configuration

</td><td>

Option to use the default taxonomy configuration. Clear the default taxonomy configuration option to see the Taxonomy Loader configuration.

</td></tr><tr><td>

Taxonomy

</td><td>

Internal taxonomy to which the external taxonomy is mapped. Unlock the list to add the taxonomy.

</td></tr><tr><td>

Taxonomy Loader

</td><td>

Taxonomy Loader configuration field when the default taxonomy configuration option is unchecked. Select the import mode for importing the taxonomy data:-   Data source: Use Data source if the taxonomy can be imported via ServiceNow platform data source.
-   Custom script: Use Custom script if the taxonomy import needs custom logic.
 For Data source: Update the following fields:

-   Data source: Data source to be defined such as Azure AD, Auth0. For more information, refer to, [Create a data source](https://www.servicenow.com/docs/access?context=c_CreateNewDataSource&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
-   Scheduled data import: The import job that runs the data source frequently. For more information, refer to [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
 For Custom script: Update the following fields:

-   Taxonomy file required: Select the check box if the data to be imported via the selected mode needs a file to be attached.
-   Variables: Use the variables defined in the script.
-   Script: Script to be populated. This is a required step.


</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The new provider taxonomy configuration record is listed on the Provider taxonomy configuration page.

