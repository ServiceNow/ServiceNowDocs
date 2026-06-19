---
title: Install Health Log Analytics \(HLA\)
description: Install Health Log Analytics by requesting ServiceNow HLA installation from ServiceNow Customer Support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/health-log-analytics/install-health-log-analytics.html
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [HLA installation, Health Log Analytics installation, installing HLA, installing Health Log Analytics, installing ServiceNow HLA, installing ServiceNow Health Log Analytics]
breadcrumb: [Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Install Health Log Analytics \(HLA\)

Install Health Log Analytics by requesting ServiceNow HLA installation from ServiceNow Customer Support.

## Before you begin

Verify that the Health Log Analytics application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. To obtain the entitlements, contact your ServiceNow Solution Consultant.

The minimum version of the ServiceNow AI Platform required for Health Log Analytics installation is Zurich.

**Important:** Health Log Analytics uses the default user sn\_occ\_occultus for internal communication. Make sure that this user is active and do not deactivate it.

Role required: admin

## Procedure

1.  On the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website, opt into the ITOM AIOps product.

    1.  Go to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website and search for the Health Log Analytics app.

        \[Omitted image "hla-store.png"\] Alt text: The Health Log Analytics app in the ServiceNow Store.

    2.  Select the Health Log Analytics tile.

        The Health Log Analytics product page displays.

        \[Omitted image "hla-store-hla-page.png"\] Alt text: The Health Log Analytics app product page in the ServiceNow Store.

    3.  Under **Included in Products**, select ITOM AIOps.

    4.  Select **Opt-in** to opt-in to ITOM AIOps.

2.  Install the Health Log Analytics application on your ServiceNow instance.

    1.  On your instance, navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Find the Health Log Analytics application using the search bar.

    3.  On the Health Log Analytics tile, select **Install**.

        When the application is successfully installed on the instance, an automatic change request \(CHG\) is triggered to request provisioning for the necessary endpoints. The instance admin receives the request and any relevant notifications.

        **Note:** Even when the Health Log Analytics application is installed successfully, it will not work until the endpoints have been provisioned. Provisioning endpoints configures your source systems to collect and send their log data to your ServiceNow instance. Health Log Analytics depends on this ingested data to detect anomalies, correlate events, and generate alerts.

    4.  On the **Installed** tab, verify that the application and its dependencies were installed successfully.

        \[Omitted image "hla-verify-installation.png"\] Alt text: Application Manager shows that Health Log Analytics is installed on your instance.

3.  Observe the status of the provisioning process by reviewing the CHG.

    **Note:** Some steps in the provisioning process might require your explicit approval. In such cases, ServiceNow Customer Support will reach out.

4.  When provisioning is completed, verify that the Health Log Analytics application is up and running on your ServiceNow instance.

    1.  On the instance, enter `sn_occ_stats.do` in the navigator and press the **Enter** keyboard key.

        The Health Log Analytics Package Dependencies and Versions table displays.

        \[Omitted image "hla-sn-occ-stats.png"\] Alt text: Health Log Analytics Package Dependencies and Versions table.

        The provisioned endpoints are listed along with their version number:

        -   Occultus
        -   MetricBase
        -   ElasticSearch
        The Health Log Analytics application is up and running on your instance.


## Result

The Health Log Analytics application is installed and provisioned on your instance.

## What to do next

-   [Set up the data input process for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/health-log-analytics/hla-implement.md)
-   \(Optional\) Install the ServiceNow® Agent Client Collector Log Analytics \(ACC-L\) plugin.

    Agent Client Collector Log Analytics enables you to stream log data from Linux and Windows hosts to a ServiceNow instance using the Agent Client Collector. For more information, see the [Agent Client Collector Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-log-analytics.md) documentation.


