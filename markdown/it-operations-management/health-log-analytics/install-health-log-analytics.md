---
title: Health Log Analytics \(HLA\) installation
description: Request ServiceNow Health Log Analytics installation from ServiceNow Customer Support.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [HLA installation, installing HLA, installing Health Log Analytics, installing ServiceNow HLA, installing ServiceNow Health Log Analytics]
breadcrumb: [Exploring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Health Log Analytics \(HLA\) installation

Request ServiceNow Health Log Analytics installation from ServiceNow Customer Support.

## Before you begin

The minimum version of the ServiceNow AI Platform required for Health Log Analytics installation is Xanadu.

**Important:** Health Log Analytics uses the default user sn\_occ\_occultus for internal communication. Make sure that this user is active and do not deactivate it.

Role required: admin

## Procedure

1.  Ensure that the Health Log Analytics application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements.

    To obtain the entitlements, contact your ServiceNow Solution Consultant.

2.  Opt into the ITOM Health product.

    1.  Go to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website and search for the Health Log Analytics app.

        ![The Health Log Analytics app in the ServiceNow Store.](../image/hla-store.png "Health Log Analytics app in the ServiceNow Store")

    2.  Select Health Log Analytics.

        The Health Log Analytics product page displays.

        ![The Health Log Analytics app product page in the ServiceNow Store.](../image/hla-store-hla-page.png "Health Log Analytics product page in the ServiceNow Store")

    3.  Select **View Products**.

    4.  Select **Opt-in**.

        ![The ITOM Health product.](../image/hla-install-itom-health.png "ITOM Health product")

3.  Install the Health Log Analytics application on your instance.

    1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    2.  Find the Health Log Analytics application using the search bar.

    3.  On the Health Log Analytics tile, select **Install**.

        When the application is successfully installed on the instance, an automatic change request \(CHG\) is triggered to request provisioning for the necessary endpoints. The instance admin receives the request and any relevant notifications.

        **Note:** Even when the Health Log Analytics application is successfully installed, it will not work until the endpoints have been provisioned.

    4.  Ensure that the application and its dependencies were installed successfully, as illustrated in the figure.

        ![Health Log Analytics is installed on the instance.](../image/hla-verify-installation.png "Health Log Analytics is installed on the instance")

4.  Observe the status of the provisioning process by reviewing the CHG.

    **Note:** Some steps in the provisioning process might require your explicit approval. In such cases, ServiceNow Customer Support will reach out.

5.  When provisioning is completed, ensure that the Health Log Analytics application is up and running.

    1.  In the Filter navigator, enter `sn_occ_stats.do`.

        The Health Log Analytics Package Dependencies and Versions table displays.

        ![Health Log Analytics Package Dependencies and Versions table.](../image/hla-sn-occ-stats.png "Health Log Analytics Package Dependencies and Versions table")

        The provisioned endpoints are listed along with their version number:

        -   Occultus
        -   MetricBase
        -   ElasticSearch

## Result

The Health Log Analytics application is installed and provisioned on your instance.

## What to do next

-   [Set up the data input process for Health Log Analytics](../concept/hla-implement.md)
-   \(Optional\) Install the ServiceNow® Agent Client Collector Log Analytics \(ACC-L\) plugin.

    Agent Client Collector Log Analytics enables you to stream log data from Linux and Windows hosts to a ServiceNow instance using the Agent Client Collector. For more information, see the [Agent Client Collector Log Analytics](../../agent-client-collector/concept/acc-log-analytics.md) documentation.


**Parent Topic:**[Exploring Health Log Analytics](../concept/hla-exploring.md)

