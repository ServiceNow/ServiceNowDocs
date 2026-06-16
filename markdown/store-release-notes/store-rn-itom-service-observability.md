---
title: Service Observability release notes
description: Version history for the Service Observability application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-service-observability.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Observability release notes

Version history for the Service Observability application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.13.3 - June 2026**
    -   Improved:
        -   Service Observability roles now see the default alert view and havefull-read data access to alerts and incidents.
        -   Improvements to the filtering experience when viewing MetricBase data in Service Observability dashboards.
-   **Version 1.12.2 - May 2026**
    -   New: New third-party integrations with LogicMonitor
    -   Improved:
        -   Data Mapping page performance enhancements
        -   The Data Mapping page now loads faster when a large number of services are being mapped.
        -   The Data Mapping list view now displays the number of services configured in the map. Click that link to view the affected services.
-   **Version 1.11.9 - March 2026**
    -   New:
        -   Two new NowAssist skills that summarize Service Observability dashboards:
            -   The Analyze Service Observability dashboard skill uses generative AI to summarize a single Service Observability dashboard and calls out any insights it finds in charts. This summary helps operators quickly orient to and understand a particular dashboard.
            -   The Analyze Service Health skill uses generative AI to analyze all available Service Observability dashboards for the selected service in the Service Operations Workspace \(SOW\). It generates a summary of a service’s health and calls out any insights it finds in the charts. This skill is available from the header of a service record in the SOW. This skill also runs automatically as part of the alerts autonomous workflow, and from theInvestigate tab in Incident Management.
    -   New third-party integrations:
        -   Zabbix
        -   CiscoThousandEyes
        -   Splunk Enterprise:You can now include business metrics derived from logs directly in the context of a service
    -   Network metrics dashboards: Service Observability can now display metrics from network performance monitoring systems. Out-of-the-box dashboards include:
        -   SolarWinds NPM
        -   CiscoThousandEyes synthetic tests
        -   Zabbix \(on-premises\)
    -   Improved:
        -   Service Observability can now display additional metrics from previous integrations:
            -   Dynatrace integration now supports Grail \(DQL\) and Classic queries, as well as metrics from on-premises Dynatrace environments \(Dynatrace Managed\)
            -   Splunk metrics now includemetrics fromlogs
            -   Note that you must have metadata tagging in place to support the additional metrics.
-   **Version 1.10.12 - December 2025**
    -   New:
        -   Integrations with AppDynamics and Prometheus data sources
        -   Import charts/dashboards from Azure and AWS
        -   Add Health Log Analytics data to charts
    -   Changed:
        -   Return Dynatrace metrics from Processes and Process Groups
        -   Use service fields as variables in data mapping tag key/value configuration, and then use those variables in a chart's query
        -   Test data mappings before saving
        -   View Service Observability Overview dashboard from the Incident Management \(Investigation\) tab
        -   Improved chart metadata
-   **Version 1.6.4 - May 2025**
    -   New:
        -   The dashboard templates used for the Observability and Overview tabs can now be customized
        -   Service Observability now supports domain separation
    -   Changed:
        -   Services no longer require activation with SRM before they can be used with Service Observability
        -   Service Observability admins can now set up Service Observability in the SOW Admin Center without the need for a sysadmin
    -   If you are upgrading from a previous version of Service Observability, you must run the "populate service\_ci column from SRM serv" fix script to update data mappings to work with this version.
    -   If using Service Observability v1.6.4 you can upgrade to SRM version 6.3.1.
-   **Version 1.5.0 - February 2025**
    -   Through ServiceNow's comprehensive approach to managing the hybrid IT estate, we can help connect the data and insights from your technologies to provide a seamless view into the performance of your business-critical applications.
    -   Service Observability enables organizations to connect data and insights to quickly and efficiently resolve problems by improving the accuracy of root cause assessment and quantifying business impact. With Service Observability, organizations can:
        -   Gain end-to-end visibility of the performance of business-critical applications to bridge IT and business
        -   Calculate blast radius and reduce mean time to resolution \(MTTR\) by overlaying changes of your application to underlying infrastructure.
        -   Maximize your existing technology investments. Consolidate data from multiple toolsets into one platform for faster root cause analysis.
    -   ServiceNow's approach to AIOps provides robust integration points with monitoring tools and hybrid/multi-cloud environments to prevent the impact of issues and automate resolution.

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)

