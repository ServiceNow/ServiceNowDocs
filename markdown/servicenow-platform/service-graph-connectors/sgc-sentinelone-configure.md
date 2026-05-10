---
title: Configure the Service Graph Connector for SentinelOne
description: The guided setup for the Service Graph Connector for SentinelOne provides an organized sequence of tasks to configure the integration on your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SentinelOne, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Service Graph Connector for SentinelOne

The guided setup for the Service Graph Connector for SentinelOne provides an organized sequence of tasks to configure the integration on your ServiceNow AI Platform instance.

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-license-module.md), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

**Dependencies and requirements:**

-   The Integration Commons for CMDB store app, which is automatically installed.
-   The CMDB CI Class Models store app store app, which is automatically installed.
-   Discovery Core plugin \(com.snc.discovery.core\), which is automatically installed by Discovery.
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see Request Discovery.
-   Guided Setup \(com.sn.ads.setup\).
-   Data Stream \(com.glide.hub.action\_type.datastream\).
-   ITOM Patterns.

Roles required:

-   SentinelOne Role - viewer
-   ServiceNow AI Platform® Role - admin

## Guided Setup

The guided setup for the Service Graph Connector for SentinelOne provides an organized sequence of tasks to configure the integration on your instance.

## Procedure

1.  Navigate to **Service Graph Connectors** &gt; **SentinelOne** &gt; **Setup**.

2.  On the Home page, select **Continue**.

3.  On the Experience page, select the **Best Experience** from it.

4.  On the Service Graph Connector for SentinelOne page in the Configure the connection page, select the **Configure SentinelOne Authentication Credentials** task and follow these steps:

    1.  In the API Key field, enter your SentinelOne API Key and update the credential record.
    2.  Select the **Mark as Complete** checkbox and select **Continue**.
5.  In the **Configure SentinelOne HTTP Connection** task follow these steps:

    1.  Add the SentinelOne base URL \(Uniform Resource Locator\).
    2.  Select the **Mark as Complete** checkbox and select **Continue**.
6.  In the **Test Connection** task follow these steps:

    1.  Select the **Test Connection** link.

        The Status code field displays `200` if the connection is successful.

    2.  Select the **Mark as Complete** checkbox and select **Continue**.
7.  To create another connection, select the **Update Data Source Access** section and follow these steps:

    1.  Give permission to create and update the data source.
    2.  Select the **Mark as Complete** checkbox and select **Continue**.
    3.  Give permission to create and update the Scheduled Import Sets.
    4.  Select the **Mark as Complete** checkbox and select **Continue**.
    5.  Clear the cache with the code snippet mentioned previously using Scripts-Background.
    6.  Select the **Mark as Complete** checkbox and select **Continue**.
    7.  Add a new connection by clicking the link.
    8.  After you add a new connection, select the **Mark as Complete** checkbox and select **Continue**.
    9.  Select the new connection record and select the **Test Connection link**.

        The Status code field displays `200` if the connection is successful.

    10. Select the **Mark as Complete** checkbox and select **Continue**.
8.  Fill out the fields on the Scheduled Data Import form:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the scheduled job.|
    |Data source|Data source record that defines the data to import.|
    |Run as|Option to run the scheduled job with the credentials of the specified user.|
    |Active|Option to activate the scheduled job. Select this option.|
    |Concurrent Import|Function that loads the data from multiple import sets. The function then processes and transforms the data concurrently.|
    |Partition Method|Partition method for the concurrent import set.|
    |Partition Size|Import set size for early scheduling.|
    |Execute pre-import script|Option to specify a script to run before the import is performed.|
    |Execute post-import script|Option to specify a script to run after the import is performed.|
    |Application|Application that contains this scheduled job.|
    |Run|Frequency of running the import.|
    |Conditional|Conditions under which this job is executed.|

9.  Click **Execute Now**.

10. In the Help task bar, select **Mark as Complete**.


