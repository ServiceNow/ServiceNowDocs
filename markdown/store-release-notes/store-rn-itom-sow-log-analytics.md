---
title: Service Operations Workspace Log Analytics release notes
description: Version history for the Service Operations Workspace Log Analytics application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-sow-log-analytics.html
release: store
topic_type: reference
last_updated: "2024-03-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Service Operations Workspace Log Analytics release notes

Version history for the Service Operations Workspace Log Analytics application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 23.0.0 - March 2024**

    Hidden app.

-   **Version 24.0.3 - November 2023**

    Several bug fixes.

-   **Version 22.5.2 - November 2023**

    No changes.

-   **Version 22.1.2 - August 2023**
    -   New: Added support for drill-down from dashboards to Log Viewer.
    -   Fixed: Bug fixes.
-   **Version 22.0.0 - May 2023**

    Fixed: Several bug fixes.

-   **Version 21.3.2 - February 2023**
    -   New:
        -   MID Server cluster: Health Log Analytics now supports MID Server clusters for all puller data inputs. For failover protection, MID Server clusters use a configured order to determine which available MID Server to use next when a failure occurs.
        -   Test Outcome table: Added to the Data Input Mapping form, the table shows the outcome of your mapping script on log samples, log sources and source types. The table is updated when the log samples are refreshed and you select Test to test the script.
    -   Changed: Improvements to the Data Input Mapping form: The maximum number of log samples was increased to 5000 and responsiveness was updated.
    -   Fixed: Several bug fixes
-   **Version 21.2.7 - November 2022**
    -   New:
        -   HLA configuration migration: Enables you to export data inputs and source types configuration as an update set, import the update set to the target instance, and start streaming logs using the imported configuration.
        -   Test mode: A designated mode for stabilizing data input mapping. When Test mode is On, the streamed logs do not go through the standard log processing flow but are instead stored under a temporary component in Elasticsearch, which is deleted when Test mode is set to Off.
        -   Test data input connection: Ensures that the data input is configured correctly. When you select Test connection, Health Log Analytics tries to connect the MID Server to the data repository.
        -   Out-of-the-box Operational dashboard: A predefined dashboard with the most common log data visualizations​ to help you monitor your log data. Using this dashboard, you can view log behavior in the last 24 hours and better understand the health of your application services.
        -   Content packs: The ability to configure data streaming for Linux systems with one simple click using the new content packages. This process automatically triggers different functions that shorten onboarding time for the Health Log Analytics application by implementing content packs. The packs contain default source types and mapping script templates that save you the time it takes to create them from scratch.
    -   Changed:
        -   Improvements in the data input mapping form that show the log sources to be created by the current mapping script. Added the ability to increase the number of log samples to 500.
        -   The ability to delete log sources together with their associated indices in Elasticsearch.
    -   Fixed: Surrounding logs issues.
-   **Version 21.1.3 - August 2022**

    The initial release of Service Operations Workspace Log viewer

-   **Version 21.0.2 - June 2022**

    New: Service Operations Workspace Log viewer


