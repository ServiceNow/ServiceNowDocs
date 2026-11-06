---
title: AWS events-driven discovery
description: Use AWS events-driven discovery to keep your CMDB current automatically when AWS resource configurations change, without waiting for a scheduled Discovery run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/aws-events-driven-discovery.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-10-15"
reading_time_minutes: 3
breadcrumb: [Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# AWS events-driven discovery

Use AWS events-driven discovery to keep your CMDB current automatically when AWS resource configurations change, without waiting for a scheduled Discovery run.

## How it works

\[Omitted image "aws-events-driven-discovery.png"\] Alt text: Overview of the AWS events-driven discovery

1.  AWS Config detects a change in the lifecycle state or configuration of a cloud resource.
2.  AWS Config sends a Simple Notification Service \(SNS\) notification to the ServiceNow Cloud Events REST API.
3.  The API writes the event to the Cloud Event \[sn\_cmp\_cloud\_event\] table if it meets any of the following criteria:
    -   The **Type** of the event is **SubscriptionConfirmation**.
    -   The **Type** of the event is **Notification**and **messageType** is **ConfigurationItemChangeNotification**.
    -   Amazon CloudWatch raised the event for a tag change on a Configuration Item \(CI\).
4.  The Cloud Event Scheduler picks up events in the Ready state for batch processing and updates the affected resource in the CMDB. When response mappings are available, event-driven discovery uses them to update the CI. Otherwise, it triggers the appropriate Discovery pattern.

## Requirements for AWS events-driven discovery

Before configuring AWS events-driven discovery, verify the following requirements are met:

-   The Discovery \(com.snc.discovery\) plugin is activated.
-   Valid AWS service accounts with associated logical datacenters are discovered.
-   Required roles: discovery\_admin and sn\_cmp.cloud\_event\_integration.
-   An AWS role with access to SNS, AWS Config, and the resource types you want to track.
-   Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

For setup instructions, see [Configure AWS Config event notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/aws-config-service-cloud-mgt.md).

## Configuration properties

<table id="table_config_properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_cmp.cloud\_event.use\_response\_mapping\_aws**

</td><td>

Determines the CMDB update method. When set to True and suitable response mappings are available, event-driven discovery uses response mappings to create or update the CI in the CMDB. Otherwise, event-driven discovery triggers the appropriate Discovery pattern. -   Type: Boolean
-   Default: true

</td></tr><tr><td>

**sn\_cmp.cloud\_event.parallel\_scheduler\_count**

</td><td>

Controls the number of Cloud Event Scheduler instances running in parallel. Increase this value to improve event processing rate when event inflow is high. For more information, see [Scale the AWS cloud event schedulers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/scale-aws-cloud-event-schedulers.md). -   Type: Integer
-   Default: 1

</td></tr><tr><td>

**sn\_cmp.error\_events.default\_domain**

</td><td>

The sys\_id of the service-provider domain. Set this property to limit the visibility of failed events to the service-provider administrator.-   Type: String
-   Default: global

</td></tr></tbody>
</table>## Domain separation

During event processing, the Cloud Event Scheduler identifies the domain of the associated service account and assigns it to the event. If domain identification fails before processing, the event can remain unassigned and be visible across all domains. To limit the visibility of failed events to the service-provider administrator, set the **sn\_cmp.error\_events.default\_domain** property to the sys\_id of the service-provider domain.

**Related topics**  


[Configure AWS Config event notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/aws-config-service-cloud-mgt.md)

[Scale the AWS cloud event schedulers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/scale-aws-cloud-event-schedulers.md)

[Create a database index for the Cloud Events table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/improve-aws-event-processing-performance.md)

[AWS discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/data-discovered-aws-patterns.md)

[AWS Events pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery-and-service-mapping-patterns/aws-events-pattern.md)

