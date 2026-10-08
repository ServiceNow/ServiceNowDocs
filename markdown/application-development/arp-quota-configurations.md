---
title: Quota configurations
description: Quota configurations define limits on the resources that an application can use at runtime. Application Runtime Policy uses these limits to prevent a single application from consuming excessive platform resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/arp-quota-configurations.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Explore, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Quota configurations

Quota configurations define limits on the resources that an application can use at runtime. Application Runtime Policy uses these limits to prevent a single application from consuming excessive platform resources.

Quota configurations enforce limits on how many resources your application can use, including API transactions, UI transactions, scheduled jobs, and event handlers. Activating Application Runtime Policy \(ARP\) automatically configures a set of default quota limits for an application that's in development. For information about the default values for automatically generated quota configurations, see [Default Quota Configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/default-quota-configuration-form.md).

You can change quota limits from the default in the automatically generated record if needed by updating the Default Quota Configuration form.

If an application exceeds the default quota configurations, requests beyond that limit are rejected, deferred, or logged based on the selected default quota configuration mode.

The Default Quota Configurations table displays the following information:

-   **Configuration name**

    A unique name used to identify the configuration.

-   **Application Condition**

    Additional conditions that determine the scope for the default quota configurations.

-   **Enable Auto-Generated Quotas**

    When true, enables automatic generation of application resource quotas in instances that install the application.

-   **Order**

    Dictates the order in which application quotas are evaluated. If multiple default quota configurations apply to an application, the default quota configuration with the lowest number is applied first.

-   **API Transaction Quota %**

    Total percentage of threads that can execute API requests for a given application and scope. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, API requests are rejected.

    Default value: 30%.

-   **Event Handler Quota %**

    Percentage of total processing time that can be allocated to event handlers. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, event handler processing is deferred until the next time window.

    Default value: 20%.

-   **Interactive Transaction Quota %**

    Total percentage of threads that can execute UI requests. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, UI requests are rejected.

    Default value: 30%.

-   **Scheduled Job Quota %**

    Percentage of total processing time that can be allocated to jobs. When the default quota configuration is in enforcing mode and the quota threshold is exceeded, scheduled jobs are deferred until the next time window.

    Default value: 20%.

-   **Mode**

    Determines how default quota configurations are enforced.

    -   **Disabled** prevents enforcements of a default quota configuration.
    -   **Enforced** causes requested resources to be deferred or rejected when the quota threshold is exceeded.
    -   **Log Only** adds log entries to the Runtime Policy Violation Log to indicate when the quota threshold is exceeded. No resources are rejected or deferred.

