---
title: Service Observability release notes
description: The ServiceNow Service Observability application helps operations teams triage and manage incidents in a complex and distributed production system. Service Observability combines telemetry and platform insights from multiple observability tools into a single workflow in the Service Operations Workspace \(SOW\). Service Observability was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Service Observability release notes

The ServiceNow® Service Observability application helps operations teams triage and manage incidents in a complex and distributed production system. Service Observability combines telemetry and platform insights from multiple observability tools into a single workflow in the Service Operations Workspace \(SOW\). Service Observability was enhanced and updated in the Zurich release.

## Service Observability highlights for the Zurich release

-   Integrate with a number of new application performance management \(APM\) vendors.
-   Add service-scoped ServiceNow AI Platform charts to Service Observability dashboards, including charts from MetricBaseand as of 1.10, Health Log Analytics \(HLA\).
-   Customize your Service Observability dashboards to add more advanced charts using full vendor queries and template variables. As of 1.10, you can directly import charts from AWS and Azure.
-   Create dashboards for additional service types.
-   Connect to data sources efficiently with an improved flow.
-   As of 1.10, test your data mappings before using them to create charts and dashboards.
-   As of 1.10, use any field on a service as a tag key value in a data mapping and then use that tag as a variable in your chart queries.

See [Service Observability](https://www.servicenow.com/docs/access?context=service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** Service Observability is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Service Observability to Zurich

If you have the snc\_sow\_svcobs.manager role, you must belong to a user groups with a type of `srm`.

## New in the Zurich release

-   **[New Service Observability integrations](https://www.servicenow.com/docs/access?context=exploring-service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Integrate with more APM vendors to bring third-party data into Service Observability dashboards. New integrations for this release include:

    -   SolarWinds on-premise
    -   Amazon CloudWatch
    -   Microsoft Azure Monitor
    -   Splunk Observability
    -   As of 1.10, AppDynamics
    -   As of 1.10, Prometheus
    -   As of 1.10, support for Dynatrace process and process groups
-   **[Support for additional ServiceNow AI Platform data in Service Observability dashboards](https://www.servicenow.com/docs/access?context=edit-sn-based-charts&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Add data from problem records and business app records to your dashboards. The data displayed is scoped to the service being investigated.

-   **Support for HLA data in Service Observability dashboards**

    As of 1.10, add service-related log data to your dashboards.

-   **[Support for full vendor queries](https://www.servicenow.com/docs/access?context=customize-service-observability-dashboard-templates&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Recreate any supported vendor time series chart in your Service Observability dashboard using full queries and template variables to represent entities and start and end times.As of 1.10, import selected charts from an existing AWS or Azure APM dashboard.

-   **[Use data mapping tags as variables in a chart's query](https://www.servicenow.com/docs/access?context=service-observability-template-variables&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.10, key/tags used in a data mapping can also be used as a template variable in a chart's query.

-   **[Additional service types](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Map all service offering types to APM data instead of just the types that have a technical service as a parent.

-   **[Test your data mapping](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.10, you can test your data mapping before using it to create charts and dashboards.

-   **[Use any field on a service as a variable in your data mapping query](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.10, when creating a data mapping, if your key represents a service, for convenience a drop down shows fields from the corresponding CI for the service, including custom fields, that can be used as a variable.

-   **[Improved data source connection flow](https://www.servicenow.com/docs/access?context=connect-an-observability-data-source&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Create APM connections without leaving the SOW.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Improved chart metadata](https://www.servicenow.com/docs/access?context=using-service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.10, charts have been improved to provide more detailed axis labels.

-   **[Improved data mapping UI](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    As of 1.10, you can now create and test your data mapping in the same UI.


## Activation information

Install Service Observability by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[ITOM AIOps release notes](itom-health-rn.md)

