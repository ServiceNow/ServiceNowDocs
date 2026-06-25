---
title: Validate FDS subscriptions items as a provider
description: Configure the sample data received from the consumer to validate a foundation data sync \(FDS\) subscription item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/service-bridge-v2-fds-validate-subs-items-provider.html
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [foundation data sync, FDS subscription, validate subscription, field mapping, provider inbound]
breadcrumb: [Configure inbound FDS as providers, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Validate FDS subscriptions items as a provider

Configure the sample data received from the consumer to validate a foundation data sync \(FDS\) subscription item.

## Before you begin

Role required: admin \(sb\_admin\)

## About this task

After you create an FDS offering request, the consumer acknowledges the request and sends you a sample payload. This payload helps you understand the structure and type of data you will receive.

After the consumer sends the sample, the system creates a subscription for each offering in the FDS request. Each subscription includes a subscription item for every table the consumer shares. Configure the incoming sample data to validate each subscription item.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Open Records** &gt; **FDS Requests**.

2.  From the **Type: Inbound**, select the request.

3.  From the Foundation Data Provider Inbound Subscriptions related list, open the provider subscription by selecting the record number in the **Number** column.

4.  From the Subscription Items related list, open the subscription item by selecting the record number in the **Number** column.

    Each subscription item represents a specific table that the consumer is sharing with you.

5.  Resolve missing relationships on your instance.

    When the source instance includes relationships that aren't present on your instance, the subscription item displays a warning banner.

    Do the following steps to resolve the missing relationships:

    1.  Select **Review and resolve**.

    2.  In the **Missing Relationships** window, review the listed relationships, and select a resolution option.

        -   **Fix automatically**: The system creates the missing relationships to match the source instance.
        -   **Resolve manually**: You create and configure the missing relationships.

            **Note:** If you select **Resolve manually**, the ETL Transform Map Assistant doesn't automatically map the missing relationships. Create and configure them manually in the CMDB so that the data syncs correctly.

    3.  Select **Confirm**.

        The system posts a work note recording the relationships it created or your manual resolution choice.

        For unresolved relationships, the banner remains until you complete the configuration.

6.  Configure incoming data using either IntegrationHub ETL or a transform map depending on whether you are working with a Configuration Management Database \(CMDB\) or a non-CMDB table.

<table id="choicetable_msz_gll_sfc"><thead><tr><th align="left" id="d36153e203">

Option

</th><th align="left" id="d36153e206">

Description

</th></tr></thead><tbody><tr><td id="d36153e212">

**Configure data integration for CMDB tables**

</td><td>

1.  Select the **ETL Transform Map Assistance** button.

A message is displayed stating that you're about to navigate to the ETL Transform Map Assistant guided setup.

2.  Confirm your choice by selecting **OK**.
3.  Use the guided setup to complete the mapping to integrate the consumer's data into your CMDB. For details, see [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integrationhub-etl.md).

The system creates a basic field mappings based on matching field names. Review and customize the mappings as needed for your instance.

**Note:** Since FDS provides display values for reference fields, if you want to use reference data, you must create a table look up transform mapping to retrieve the Sys ID from the reference table. For more details, see [Foundation Data Sync :: Known issues and workarounds \[KB2299760\]](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=8a2b463c873aaadc57288519dabb354b)

4.  Close the browser tab to return to the Subscription Item page.


</td></tr><tr><td id="d36153e258">

**Configure data integration for CMDB tables \(__Maintain sysID__ enabled by the provider\)**

</td><td>

1.  Select the **Transform Map** button.

A message is displayed stating that you’re about to navigate to the Transform Map to complete the configuration.

2.  Confirm your choice by selecting **OK**.
3.  Complete the configuration. For details, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/t_CreateATransformMap.md).
4.  Close the browser tab to return to the Subscription Item page.


</td></tr><tr><td id="d36153e300">

**Configure data integration for non-CMDB table**

</td><td>

1.  Select the **Transform Map** button.

A message is displayed stating that you're about to navigate to the Transform Map to complete the configuration.

2.  Confirm your choice by selecting **OK**.
3.  Complete the configuration. For details on working with transform maps, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/t_CreateATransformMap.md).
4.  Close the browser tab to return to the Subscription Item page.


</td></tr></tbody>
</table>    You must configure incoming data for each subscription item except dependent subscription items.


## Result

After you complete the configuration, the state of the subscription item and of the subscription changes to Validated.

## What to do next

[Accept the subscription.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-fds-accept-sups-provider.md)

**Related topics**  


[Foundation data sync](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-explore-foundation-data-sync.md)

[Configuring inbound foundation data sync as providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-configure-inboun-fds-providers.md)

[Configure outbound foundation data sync as consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/using-provider-bound-fds-consumer.md)

