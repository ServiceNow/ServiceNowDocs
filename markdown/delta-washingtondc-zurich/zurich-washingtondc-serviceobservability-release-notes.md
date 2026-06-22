---
title: Combined Service Observability release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Service Observability from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-serviceobservability-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Service Observability release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Service Observability from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Observability release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Observability to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

If you have the snc\_sow\_svcobs.manager role, you must belong to a user groups with a type of `srm`.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Service Observability.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Create and manage mappings](https://servicenow-staging.fluidtopics.net/access?context=create-and-manage-observability-data-mappings&family=yokohama&ft:locale=en-US)**

Map services in the CMDB Workspace to the data from a connected application performance monitoring \(APM\) data source. Service Observability supports Dynatrace and New Relic. This mapping lets you view metrics from entities deep within your system, like a database or host, that might be affecting the health of a service.

Starting in version 1.7.3, metrics from Datadog are supported.

Starting in version 1.7.3, you can map Business Services and Service Offerings to APM data. Service Offerings are not available in Xanadu.

-   **[View overall service health](https://servicenow-staging.fluidtopics.net/access?context=view-overall-service-health&family=yokohama&ft:locale=en-US)**

Use the Overview tab to view rate, error, and duration \(RED\) metrics from the APM related to a service. You can also view related open alerts, incidents, and change requests from the Configuration Management Database \(CMDB\) to help identify possible causes and blast radius.

-   **[View service health metrics](https://servicenow-staging.fluidtopics.net/access?context=view-service-health-metrics&family=yokohama&ft:locale=en-US)**

View the extended health metrics for a service on the new **Observability** tab when issues are found on the **Overview** tab. In addition to the extended health metrics, you can view host and database metrics related to the service based on the configured data mappings.

-   **[Customize dashboard templates](https://servicenow-staging.fluidtopics.net/access?context=customize-service-observability-dashboards&family=yokohama&ft:locale=en-US)**

Starting in version 1.6.4, customize the templates used to display dashboards in the **Overview** and **Observability** tabs.

-   **[Domain separation](https://servicenow-staging.fluidtopics.net/access?context=domain-separation-and-service-observability&family=yokohama&ft:locale=en-US)**

Starting in version 1.6.4, Service Observability can be run in separate domains.


</td></tr><tr><td>

Zurich

</td><td>

-   **[New Service Observability integrations](https://servicenow-staging.fluidtopics.net/access?context=exploring-service-observability&family=zurich&ft:locale=en-US)**

Integrate with more APM vendors to bring third-party data into Service Observability dashboards. New integrations for this release include:

    -   SolarWinds on-premise
    -   Amazon CloudWatch
    -   Microsoft Azure Monitor
    -   Splunk Observability
    -   As of 1.10, AppDynamics
    -   As of 1.10, Prometheus
    -   As of 1.10, support for Dynatrace process and process groups
-   **[Support for additional ServiceNow AI Platform data in Service Observability dashboards](https://servicenow-staging.fluidtopics.net/access?context=edit-sn-based-charts&family=zurich&ft:locale=en-US)**

Add data from problem records and business app records to your dashboards. The data displayed is scoped to the service being investigated.

-   **[Support for HLA data in Service Observability dashboards](https://servicenow-staging.fluidtopics.net/access?context=display-hla-data-on-a-dashboard&family=zurich&ft:locale=en-US)**

As of 1.10, add service-related log data to your dashboards.

-   **[Support for full vendor queries](https://servicenow-staging.fluidtopics.net/access?context=customize-service-observability-dashboard-templates&family=zurich&ft:locale=en-US)**

Recreate any supported vendor time series chart in your Service Observability dashboard using full queries and template variables to represent entities and start and end times.As of 1.10, import selected charts from an existing AWS or Azure APM dashboard.

-   **[Use data mapping tags as variables in a chart's query](https://servicenow-staging.fluidtopics.net/access?context=service-observability-template-variables&family=zurich&ft:locale=en-US)**

As of 1.10, key/tags used in a data mapping can also be used as a template variable in a chart's query.

-   **[Additional service types](https://servicenow-staging.fluidtopics.net/access?context=create-and-manage-observability-data-mappings&family=zurich&ft:locale=en-US)**

Map all service offering types to APM data instead of just the types that have a technical service as a parent.

-   **[Test your data mapping](https://servicenow-staging.fluidtopics.net/access?context=create-and-manage-observability-data-mappings&family=zurich&ft:locale=en-US)**

As of 1.10, you can test your data mapping before using it to create charts and dashboards.

-   **[Use any field on a service as a variable in your data mapping query](https://servicenow-staging.fluidtopics.net/access?context=create-and-manage-observability-data-mappings&family=zurich&ft:locale=en-US)**

As of 1.10, when creating a data mapping, if your key represents a service, for convenience a drop down shows fields from the corresponding CI for the service, including custom fields, that can be used as a variable.

-   **[Improved data source connection flow](https://servicenow-staging.fluidtopics.net/access?context=connect-an-observability-data-source&family=zurich&ft:locale=en-US)**

Create APM connections without leaving the SOW.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Service Observability features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Service Observability features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Service Observability features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Service Observability.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Install Service Observability by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Service Observability by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Observability we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

For the best experience, an APM instance should be installed and an API Key Credential for that instance should be configured on the ServiceNow® platform. Service Observability supports Datadog, Dynatrace, or New Relic.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Service Observability we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Service Observability, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Observability we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Service Observability we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   Connect operators with subject matter experts \(SMEs\) using critical signals from existing monitoring tools and the ServiceNow platform.
-   Centralize critical signals and bridge workflows to help increase agility and reliability.
-   Calculate the blast radius and help reduce mean time to resolution \(MTTR\) by viewing changes to your application and the underlying infrastructure.

 See [Service Observability](https://servicenow-staging.fluidtopics.net/access?context=service-observability&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Integrate with a number of new application performance management \(APM\) vendors.
-   Add service-scoped ServiceNow AI Platform charts to Service Observability dashboards, including charts from MetricBaseand as of 1.10, Health Log Analytics \(HLA\).
-   Customize your Service Observability dashboards to add more advanced charts using full vendor queries and template variables. As of 1.10, you can directly import charts from AWS and Azure.
-   Create dashboards for additional service types.
-   Connect to data sources efficiently with an improved flow.
-   As of 1.10, test your data mappings before using them to create charts and dashboards.
-   As of 1.10, use any field on a service as a tag key value in a data mapping and then use that tag as a variable in your chart queries.

 See [Service Observability](https://servicenow-staging.fluidtopics.net/access?context=service-observability&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

