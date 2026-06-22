---
title: Validate foundation data sync subscription items
description: Configure the sample data received from the provider to validate a foundation data sync \(FDS\) subscription item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/service-bridge-v2-validate-fds-subscription.html
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure inbound FDS as consumers, Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Validate foundation data sync subscription items

Configure the sample data received from the provider to validate a foundation data sync \(FDS\) subscription item.

## Before you begin

Role required: admin

## About this task

After you create an FDS offering request, the provider acknowledges the request and sends you a sample payload. This payload helps you understand the structure and type of data you’ll receive.

After the provider sends the sample, a subscription is generated for each offering in the FDS offering request and each subscription contains a subscription item for each table the provider is sharing. You must configure the incoming sample data to validate the FDS subscription items.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **FDS Requests**.

2.  Select the request.

3.  From the Foundation Data Consumer Subscriptions related list, open the consumer subscription by selecting the record number in the **Number** column.

4.  From the Subscription Items related list, open the subscription item by selecting the record number in the **Number** column.

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

6.  Configure incoming data using either IntegrationHub ETL or a transform map depending on whether you are working with a Configuration Management Database \(CMDB\), CMDB with **Maintain sysID** enabled by the provider, or a non-CMDB table.

<table id="choicetable_msz_gll_sfc"><thead><tr><th align="left" id="d22533e182">

Option

</th><th align="left" id="d22533e185">

Description

</th></tr></thead><tbody><tr><td id="d22533e191">

**Configure data integration for CMDB tables**

</td><td>

1.  Select the **ETL Transform Map Assistance** button.

A message is displayed stating that you’re about to navigate to the ETL Transform Map Assistant guided setup.

2.  Confirm your choice by selecting **OK**.
3.  Use the guided setup to complete the mapping to integrate third-party data into CMDB. For details, see [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md).

**Note:** Since FDS provides display values for reference fields, if you want to use reference data, you must create a table lookup transform mapping to retrieve the Sys ID from the reference table. For more details, see [Foundation Data Sync :: Known issues and workarounds \[KB2299760\]](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=8a2b463c873aaadc57288519dabb354b)

4.  Close the browser tab to return to the Subscription Item page.


</td></tr><tr><td id="d22533e235">

**Configure data integration for CMDB tables \(__Maintain sysID__ enabled by the provider\)**

</td><td>

1.  Select the **Transform Map** button.

A message is displayed stating that you’re about to navigate to the Transform Map to complete the configuration.

2.  Confirm your choice by selecting **OK**.
3.  Complete the configuration. For details, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md).
4.  Close the browser tab to return to the Subscription Item page.


</td></tr><tr><td id="d22533e277">

**Configure data integration for non-CMDB table**

</td><td>

1.  Select the **Transform Map** button.

A message is displayed stating that you’re about to navigate to the Transform Map to complete the configuration.

2.  Confirm your choice by selecting **OK**.
3.  Complete the configuration. For details, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md).
4.  Close the browser tab to return to the Subscription Item page.


</td></tr></tbody>
</table>    You must configure incoming data for each subscription item except dependent subscription items.


## Result

After you complete the configuration, the state of the subscription item and of the subscription changes to Validated.

## What to do next

[Accept the subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-accept-fds-subscription.md).

