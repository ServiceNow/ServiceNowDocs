---
title: Tag-based mapping in the Service Mapping Workspace
description: The Tag-based service mapping dashboard offers an intuitive way to manage tag-based services. Use the widgets, data visualizations, and list navigation to review and update your services, or create new tag-based services in a few steps. The dashboard enhances the Service Mapping Workspace, offering an efficient and user-friendly interface for organizing and optimizing your service mappings.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-06-16"
reading_time_minutes: 2
breadcrumb: [Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Tag-based mapping in the Service Mapping Workspace

The Tag-based service mapping dashboard offers an intuitive way to manage tag-based services. Use the widgets, data visualizations, and list navigation to review and update your services, or create new tag-based services in a few steps. The dashboard enhances the Service Mapping Workspace, offering an efficient and user-friendly interface for organizing and optimizing your service mappings.

## Prerequisites

Access to tag-based service mapping in the Service Mapping workspace requires the installation of Service Mapping Plus version 1.16.3. For more information, see [Install Service Mapping Plus](../task/install-service-mapping-plus.md).

## Required role

service\_mapping\_admin

## Access

To open the dashboard, navigate to **Workspaces** &gt; **Service Mapping**, then select the Tag-based service mapping \(![tag icon](../../../reuse/icons/product-icons/tag-outline-24.svg)\) icon from the navigation pane.

![Tag-based mapping dashboard with data widgets and a graph](../image/tag-mapping-dashboard.png)

## Key metrics

Selecting a widget in this section redirects you to the list for more detailed information.

-   **Tag-based service maps**

    The number of service maps created using tag-based service mapping.

-   **Service families with categories**

    The number of service families created to store service candidates and service maps.

-   **Tag categories**

    The number of tag categories, which group tags that have a related use.


## Report

<table id="table_kfd_jhj_rfc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total number of tag-based service maps vs. service candidates

</td><td>

Two-variable line graph

 ![](../../../use/reporting/image/inline-data-vis-96px-area.png)

</td><td>

A chart that shows the tag-based service candidates and the tag-based service maps created on a given day over a 30-day period. Use this information to evaluate the actual number of services mapped as compared to the number of service candidates created.

</td></tr></tbody>
</table>## List navigation

The List navigation pane displays tag-based service mapping information.![View of tag-based mapping list navigation pane](../image/list-nav-tag-mapping-dashboard.png)

Display tag-based information and access tag-based actions through the following pages:

-   **Tag-based service maps**
    -   View or delete existing service maps.
    -   Initiate the flow to create a tag-based service.
-   **Tag-based families with categories**
    -   View service families that have at least one selected category.
    -   Select a service family to view detailed information including mapped services and service candidates.
    -   Initiate the flow to create a tag-based service.
-   **Tag categories**
    -   View or delete existing tag categories.
    -   Select a tag category to view detailed information, including tag keys.
    -   Initiate the flow to create a tag category.

## Domain separation

When creating a service family for mapping services based on tags in domain-separated environment, you must pick the relevant leaf domain. Service Mapping populates tag-based services based on this service family only with CIs belonging to the leaf domain to which the service family belongs. If you have domain separation without Performance Analytics domain support, you can't see data visualization for the total number of tag-based service maps versus service candidates. You’re then redirected to install the Performance Analytics Domain Support plugin.

For more information about domain separation and Service Mapping, see [Domain separation and Service Mapping](../concept/domain-separation-service-mapping.md).

-   **[About the tag-based application service form](../concept/tag-based-service-form.md)**  
The tag-based application service form provides a centralized location for viewing detailed information about a selected tag-based service, including its configuration and its associated configuration items.

**Parent Topic:**[Exploring Service Mapping](../concept/service-mapping-get-started.md)

