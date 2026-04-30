---
title: Service Observability release notes
description: The ServiceNow Service Observability application helps operations teams triage and manage incidents in a complex and distributed production system. Service Observability combines telemetry and platform insights from multiple observability tools into a single workflow in the Service Operations Workspace \(SOW\). Service Observability is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Service Observability release notes

The ServiceNow® Service Observability application helps operations teams triage and manage incidents in a complex and distributed production system. Service Observability combines telemetry and platform insights from multiple observability tools into a single workflow in the Service Operations Workspace \(SOW\). Service Observability is a new application in the Yokohama release.

## Service Observability highlights for the Yokohama release

-   Connect operators with subject matter experts \(SMEs\) using critical signals from existing monitoring tools and the ServiceNow platform.
-   Centralize critical signals and bridge workflows to help increase agility and reliability.
-   Calculate the blast radius and help reduce mean time to resolution \(MTTR\) by viewing changes to your application and the underlying infrastructure.

See [Service Observability](https://www.servicenow.com/docs/access?context=service-observability&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** Service Observability is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Service Observability features

-   **[Create and manage data mappings](https://www.servicenow.com/docs/access?context=create-and-manage-observability-data-mappings&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Map services in the CMDB Workspace to the data from a connected application performance monitoring \(APM\) data source. Service Observability supports Dynatrace and New Relic. This mapping lets you view metrics from entities deep within your system, like a database or host, that might be affecting the health of a service.

    Starting in version 1.7.3, metrics from Datadog are supported.

    Starting in version 1.7.3, you can map Business Services and Service Offerings to APM data. Service Offerings are not available in Xanadu.

-   **[View overall service health](https://www.servicenow.com/docs/access?context=view-overall-service-health&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Use the Overview tab to view rate, error, and duration \(RED\) metrics from the APM related to a service. You can also view related open alerts, incidents, and change requests from the Configuration Management Database \(CMDB\) to help identify possible causes and blast radius.

-   **[View service health metrics](https://www.servicenow.com/docs/access?context=view-service-health-metrics&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    View the extended health metrics for a service on the new **Observability** tab when issues are found on the **Overview** tab. In addition to the extended health metrics, you can view host and database metrics related to the service based on the configured data mappings.

-   **Customize dashboard templates**

    Starting in version 1.6.4, customize the templates used to display dashboards in the **Overview** and **Observability** tabs.

-   **Domain separation**

    Starting in version 1.6.4, Service Observability can be run in separate domains.


## UI changes

-   **[New Overview tab in the SOW](https://www.servicenow.com/docs/access?context=view-overall-service-health&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    After services are activated for the **Overview** tab in Service Observability, the Service Details page in SOW now shows reliability metrics from Service Reliability Management \(SRM\) as well as metrics from Service Observability.

-   **[New Observability tab in the SOW](https://www.servicenow.com/docs/access?context=view-service-health-metrics&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The **Observability** tab on the Service Details page in SOW shows related metrics from connected APM vendors.

-   **[Admin Center support for activating services and data sources](https://www.servicenow.com/docs/access?context=activate-teams-and-services&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    You can activate services to use in Service Observability and then connect and map APM data sources to those services.

    Starting in version 1.6.4, you no longer need to activate services. Any of the supported service types in the CMDB can be used

    Starting in version 1.6.4, the Service Observability admin role can configure Service Observability in the Admin Center without involving an administrator.


## Activation information

Install Service Observability by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

For the best experience, an APM instance should be installed and an API Key Credential for that instance should be configured on the ServiceNow® platform. Service Observability supports Datadog, Dynatrace, or New Relic.

## Related ServiceNow applications and features

-   **[Service Operations Workspace for ITOM](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    You can access Service Observability from the Service Details page of the SOW.

-   **[Service Reliability Management](https://www.servicenow.com/docs/access?context=sr-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    You can view the reliability metrics of SRM in the same view as Service Observability, giving you a holistic view of service health. Services that are activated for Service Observability are also activated for SRM. Starting in version 1.6.4, services no longer need to be registered with SRM to use them in Service Observability.


