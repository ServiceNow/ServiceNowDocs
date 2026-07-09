---
title: Edit a unified service
description: Add or remove services to update a unified service. The flow is available using the Service Mapping workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/unified-map-edit-unified-service.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Service Mapping Plus, CSDM, business context]
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Edit a unified service

Add or remove services to update a unified service. The flow is available using the Service Mapping workspace.

## About this task

[Multi-source service mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/multi-source-service-mapping.md)

## Before you begin

You must have at least Australia platform version installed.

You must have the latest version of Service Mapping Plus.

[Create a service instance from various data sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/unified-map-create-service-instance.md)

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Mapping**.

2.  Select the **Mapped application services** widget.

3.  Select a service of type Unified, and then select **Edit**

4.  Edit the unified service details if needed, and select **Next**.

5.  To add mapped and unmapped services to your unified map, add criteria in the **Search criteria** section.

    1.  Enter a service name to add a service for unification.

    2.  Enter a server name to add a server for unification.

    3.  Enter a URL or multiple URLs separated by commas.

    4.  Enter a tag key to add a resource for unification.

    5.  Select **Find matching services** to add services by the matching criteria.

    6.  Review the service details, using the info icon, and select the check box to add it to the unified service.

    7.  Review the "Selected services" panel and remove service instances if needed.

        The "Delete service" button is for removing the entire unified service.

    8.  Select **Next** when your list of services in the "Selected services" panel is final.

6.  Enrich your service by linking it to its business context.

    Provide the business and operational details that connect this service to the rest of your organization. These details help drive visibility and reporting.

    1.  Set relationships and connect this service to its CSDM components.

        All three fields are optional. Leaving any or all fields empty is valid and does not prevent you from proceeding to the next step.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business application

</td><td>

Search for and select a business application. This field allows you to link your service instance to the business application it supports.

 Single selection only. If you type text without selecting from the list, an error state appears \(red border\) and the **Next** button is disabled until you select a valid option or clear the field.

</td></tr><tr><td>

Parent service

</td><td>

Search for and select a parent application service. Use this field to establish hierarchical relationships and build logical context for your service instance.

 Single selection only. If you type text without selecting from the list, an error state appears \(red border\) and the **Next** button is disabled until you select a valid option or clear the field.

</td></tr><tr><td>

Business service offerings

</td><td>

Business service offerings represent specific workflows or solutions that are delivered through business services.

 Select one or more business service offerings. Multiple selections allowed. Selected offerings appear as removable tags.

</td></tr></tbody>
</table>    2.  Select **Next**.

7.  Review the service details and select **Update**.

    Your unified service is updated.

    In the process of editing the unified service, the list of configuration items \(CI\) is updated. After completion, a map refresh is needed to present the updated unified service.


**Parent Topic:**[Using Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/using-service-mapping.md)

**Related topics**  


[Delete a unified service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/unified-map-delete-unified-service.md)

