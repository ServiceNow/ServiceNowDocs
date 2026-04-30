---
title: Service offering to catalog item relationships
description: Manage the relationships between your service offerings and catalog items by associating your pre-existing catalog items to your service offerings and vice versa. View relationships in both ServiceNow AI Platform form related lists and Service Owner Workspace.
locale: en-US
release: xanadu
product: Service Owner Workspace
classification: service-owner-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Service Owner Workspace, Service Owner Workspace, IT Service Management]
---

# Service offering to catalog item relationships

Manage the relationships between your service offerings and catalog items by associating your pre-existing catalog items to your service offerings and vice versa. View relationships in both ServiceNow AI Platform form related lists and Service Owner Workspace.

**Important:** As of the San Diego release, Service Owner Workspace is in a planned deprecation. New customers can't find or activate Service Owner Workspace. ServiceNow® continues to support existing customers with Service Owner Workspace. For information on the product replacement and the deprecation process, see [Service Owner Workspace](SPM2-premium.md). For information about this topic, see [Subscribe users to a service offering in Service Portfolio Management](../../service-portfolio-management2/task/SPM2-subscribe-to-service-offering.md).

## Required roles and actions

Service owners and catalog administration managers can edit relevant forms to associate and manage pre-existing service offering to catalog item relationships. This feature is in addition to the **Create Catalog Item** feature that enables you to create a new catalog item.

With the service\_editor role, you can add, change, and remove catalog items associated with an owned service offering via the Service Offering form Catalog Item related list. You can also create a catalog item from a service offering via Service Owner Workspace by clicking the **Create Catalog Item** link. A single service offering may have many related catalog items. Click the **Link** button in the Catalog Item related list to make a change.

**Note:** If a catalog item is already associated with a service offering, you cannot associate the item to a new offering. You will have to contact a catalog\_admin to remove the existing association so that you can make changes.

With the catalog\_admin role, you can add, change, and remove service offerings associated with a catalog item via the Catalog Item form Service Offerings related list. A single catalog item can be related to one service offering.

Click the **Link** button in the related list to make a change. You can remove the association if needed with the related list **Delete** button.

**Note:** If a service offering is already associated to a catalog item, the **Link** button does not appear in the related list. For details about viewing and editing Catalog Items, refer to [Create or edit a catalog item](https://www.servicenow.com/docs/access?context=t_DefineACatalogItem&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Catalog items in Service Owner Workspace

View catalog items related to a service offering in Service Owner Workspace from the offering page **Catalog Items** tab. Click to open a catalog item to drill down into more details and even open up the form view.

Monitor fulfilled requests for all associated catalog items and order guides in the offering **Trend** tab **Activity** metric.

Hover over the **Trends** tab **Activity** metric to view both the catalog item name and the 30 day average running count.

When you click the trend line for an individual catalog item, only **Requested Items** for that catalog item and the offering are visible on the list view of the report viewer.

## Things to keep in mind

-   Avoid model phase conflicts between offerings and catalog items.
    -   Catalog items can only be associated to service offerings in the **Catalog** phase.
    -   The service offering must be operational for catalog items to be active.
    -   Inactive catalog items can be associated to operational service offerings.
-   Order guides are not referenced as associated items.

    In Service Owner Workspace, **Activity** metrics are driven by catalog items that compose an order guide.


