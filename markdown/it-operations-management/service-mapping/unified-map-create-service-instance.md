---
title: Create a service instance from various data sources
description: Search for mapped and unmapped services to unify. The flow is available using the Service Mapping workspace.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Service Mapping Plus, ITOM]
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Create a service instance from various data sources

Search for mapped and unmapped services to unify. The flow is available using the Service Mapping workspace.

## About this task

[Multi-source service mapping](../concept/multi-source-service-mapping.md)

## Before you begin

You must have at least Australia platform version installed.

You must have the latest version of Service Mapping Plus.

At least two existing services to merge, or at least two sources of data that are actively updated.

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Mapping**.

2.  Select **Create service instance**

3.  Add service details.

    1.  Fill in the basic details form.

<table id="table_ld2_23x_13c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service instance name

</td><td>

Enter a descriptive name for this service instance. For example: Payment processing.

 You will not be able to proceed unless you enter a value in this field.

</td></tr><tr><td>

Support group

</td><td>

Select the group responsible for supporting this service instance. For example: Application support.

 You won’t be able to proceed unless you enter a value in this field.

</td></tr><tr><td>

Service instance owner

</td><td>

Select the person accountable for this service instance.

</td></tr><tr><td>

Short description

</td><td>

Provide a brief summary of what this service instance does. For example: Unified service containing tag-based services and ML-suggestion-based services for payment processes.

</td></tr></tbody>
</table>    2.  Expand the Additional fields section and customize additional fields as needed. For example, add production environment or operational status.

        Field availability is configured by your administrator.

    3.  Select **Next**.

4.  Find and select services to unify.

    To add mapped and unmapped services to your unified map, add criteria in the **Search criteria** section. You can search for services by entering different types of criteria.

    **Note:** A maximum of ten services can be unified by default \(configurable via the sn\_sm\_scoped\_app.sm.unified\_services.max\_children\_per\_service system property\).

    1.  Enter a service name to add a service for unification.

    2.  Enter a server name to add a server for unification.

    3.  Enter a tag key to add a resource for unification.

        You can add as many tags as you need. You can add multiple tag values per each tag key.

    4.  Enter a URL or multiple URLs separated by commas.

        You can add as many URLs as needed.

    5.  Select **Find matching services**.

        Services that match the criteria are listed in two ways:

        -   Top recommendations: The top 50 services that match the criteria, including unmapped services.
        -   All matching services: All mapped services that match the criteria.
    6.  Select the services to unify using the check boxes.

        While selecting the services to unify, details and preview maps are available for unmapped and mapped services, using the info icon. A list of configuration items \(CI\) is displayed for review before the final step of creating the unified service. The CIs origins are mentioned in the **Parents** field.

        **Note:** Map preview isn’t supported for unmapped tag-based services.

    7.  Select **Next**

    8.  Review the service details and select **Create**.

    When the process of creating the unified service is complete, the unified service map is displayed in the "Unified map" format. You can review the map using the CMDB Workspace, showing the complete consolidated view. It can take a few minutes for the map to load.

    **Note:**

    The unified service is created as non-operational by default. All selected unmapped services convert into non-operational mapped services.


**Parent Topic:**[Using Service Mapping](../concept/using-service-mapping.md)

**Related topics**  


[Edit a unified service](unified-map-edit-unified-service.md)

[Delete a unified service](unified-map-delete-unified-service.md)

