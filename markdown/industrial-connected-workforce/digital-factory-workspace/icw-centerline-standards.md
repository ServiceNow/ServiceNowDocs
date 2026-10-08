---
title: Centerline standards
description: A centerline standard defines which equipment settings operators confirm, where those settings apply, and which materials they cover. Centerline tasks generated from the standard check each setting against its setting specification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/icw-centerline-standards.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 2
breadcrumb: [Industrial Centerlines, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Centerline standards

A centerline standard defines which equipment settings operators confirm, where those settings apply, and which materials they cover. Centerline tasks generated from the standard check each setting against its setting specification.

A centerline standard is a type of Industrial Standards standard. It reuses the Industrial Standards framework for publishing, scheduling, and task generation, and adds a centerline configuration that selects the setting definitions to confirm.

The Industrial Centerlines standard author role is required to create and update centerline standards in the Draft state. The Industrial Centerlines user role is required to view centerline standards.

## Centerline standards in the Standards Hub

Centerline standards are displayed as cards in the Standards Hub, together with other types of standards. You can search the standards and filter the list, for example, to show only centerline standards.

The actions available on a centerline standard card depend on the state of the standard:

-   Draft: Select **Edit** to open and update the standard.
-   Published: Select **Create task** to create a centerline task from the standard.

## Centerline standard form

A new centerline standard opens in the Draft state. The centerline standard form includes the fields that all standards share, and the following centerline-specific information:

-   **Where**

    The functional locations, equipment models, or equipment that the standard applies to, and the material classifications and material models that the standard covers.

-   **How**

    Supporting information for operators, such as a related knowledge article and the skills required to perform the task.

-   **Centerline configuration**

    The settings that operators confirm when they execute a task generated from the standard:

    -   **Query**: Conditions that filter the setting definitions available for the standard. All conditions must be met.
    -   **Setting definition**: The setting definitions to include in the standard. Only setting definitions that match the query are available to select.

The material scope that you configure on the standard determines which materials are available when operators execute the task on mobile. The material used during task execution determines which setting specifications apply.

By default, the standard applies to all materials.

## Centerline standard actions

The following actions are available on a centerline standard form in the Workspace:

-   **Use as template for new standard**

    Creates a copy of the current standard. Use this action to reuse an existing standard's configuration as the starting point for a new one. The copy opens as a new record with a new number.

-   **Create new version**

    Creates a new version of the current standard. This action is available when the standard is eligible for versioning. The new version opens in the Draft state and inherits the configuration of the previous version.


## Open tasks on a centerline standard

When open centerline tasks are associated with a standard, the standard shows an Open tasks list with these tasks. The list appears only when at least one open task exists.

## Centerline standard lifecycle

Centerline standards follow the Industrial Standards life cycle. Publishing, approvals, versioning, retiring, scheduling, and task generation work the same way as for other standards. For more information, see [Exploring Industrial Standards](https://www.servicenow.com/docs/access?context=industrial-standards-landing-page).

-   **[Create a centerline standard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/create-centerline-standard.md)**  
Create a centerline standard to define which equipment settings operators confirm, and for which equipment and materials.

**Parent Topic:**[Using Industrial Centerlines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/using-industrial-centerlines.md)

