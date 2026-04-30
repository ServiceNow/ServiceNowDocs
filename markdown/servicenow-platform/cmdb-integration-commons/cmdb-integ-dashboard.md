---
title: CMDB Integrations Dashboard
description: You can use the CMDB Integrations Dashboard that provides a central view of status, processing results, and processing errors of all installed Service Graph Connectors and any custom integrations created in IntegrationHub ETL run.Access the CMDB Integrations Dashboard provided with the Integration Commons for CMDB store app for maintaining data consistency and accuracy across multiple data sources.
locale: en-US
release: yokohama
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Integrations Dashboard

You can use the CMDB Integrations Dashboard that provides a central view of status, processing results, and processing errors of all installed Service Graph Connectors and any custom integrations created in IntegrationHub ETL run.

**Note:** Starting with the Xanadu release, the CMDB Integrations Dashboard is available in the Next Experience user interface. For more information on the Next Experience user interface, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

On the CMDB Integrations Dashboard, you can see metrics for all Service Graph Connector runs, or filter the view to a specific connector, a specific time duration, or a specific connector run.

Learn more about the CMDB Integrations Dashboard from the following video.

CMDB Integrations Dashboard overview

## Access CMDB Integrations Dashboard

Access the CMDB Integrations Dashboard provided with the Integration Commons for CMDB store app for maintaining data consistency and accuracy across multiple data sources.

### Before you begin

Role required: None

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Dashboards**.

    **Tip:** Alternatively, you can navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  On the Dashboards view, select **CMDB Integrations Dashboard** and perform any of the following tasks:

    -   Select the **CMDB Execution Status** tab to see metrics such as the total number of integrations and processed rows, integration runs actively running, daily statistics, and details about the classes that were updated.
    -   Select the **CMDB Integration Errors** tab to see metrics such as number of import and integration errors, and number of erroneous imported records.
    -   Point to the score on the various tiles to drill down to the list views for the associated records. Point to the charts to show more details for the chart.
    -   Narrow down the scope of the integration runs included in the metrics on the dashboard by configuring filters on the right-hand side of the dashboard. Set any of the following filters and then select **Apply**. The filter settings apply to any metric with a filter icon in its upper left corner.

        |Filter|Description|
        |------|-----------|
        |Import Date|Select **All** or a time period, such as **Last 7 days**, from which to include integration runs in metrics.|
        |CMDB Applications|Select **All**, or a CMDB application, such as **SCCM**, or a custom integration, from which to include integration runs in metrics.|
        |CMDB Import|Select **All**, or a specific integration run to include in metrics.|


