---
title: Service Catalog release notes
description: The ServiceNow Service Catalog application provides a requester view of the available services and products offered by the departments within your organization. Service Catalog was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Service Catalog release notes

The ServiceNow® Service Catalog application provides a requester view of the available services and products offered by the departments within your organization. Service Catalog was enhanced and updated in the Australia release.

## Service Catalog highlights for the Australia release

-   Enable other users, who are added to the **Secondary owner** field, to edit catalog items.
-   Let your requesters view the stage and the state of their requests while using the service fulfillment step.
-   Configure catalog UI policies with scripts and multiple catalog UI policy actions in the Catalog Builder to facilitate the creation of complex catalog items.
-   Hide or show variables on a grid layout of the multi-row variable set \(MRVS\) for a catalog item.
-   Configure the update set prefix to set a custom name for the update set that gets generated automatically in the Catalog Builder.

See Service Catalog for more information.

## New in the Australia release

-   **Enable editing of catalog items by multiple users**

    Enable other users, who are added to the **Secondary owner** field, to edit catalog items. To enable these users, add people to the **Secondary owner** user-criteria field in the sc\_cat\_item and sc\_cat\_item\_producer tables, enabling others to make changes to catalog items owned by another person.

-   **Define and add stages in fulfilment step**

    Define and add distinct stages and states in the fulfillment step when building a catalog item in Catalog Builder, enabling requesters to view the request-related current stages and their states together.

-   **Use advanced UI policy capabilities in Catalog Builder**

    Configure catalog UI policies with scripts and multiple catalog UI policy actions in the Catalog Builder to facilitate the creation of complex catalog items. With these enhancements, catalog item creators can confidently take advantage of advanced options, simplifying and speeding up the entire catalog development process.

-   **Configure variable visibility on multi-row variable set grids**

    Configure the visibility of a variable on the grid layout within a multi-row variable set \(MRVS\) for a catalog item by using the **Hide on grid** check box. By default, the check box is not selected.

-   **Configure update set prefix**

    Configure the update set prefix to set a custom name for the update set that gets generated automatically in Catalog Builder, making update sets easy to identify and track for consistency. Use the **glide.sc.cb.item.update\_set\_prefix** property to standardize update set names. By default, the property uses the value **CB\_$\{template\_name\}\_$\{item\_name\}\_$\{timestamp\}**.


## Changed in this release

-   **Use UI Policy tab to add and manage the UI policies**

    Previously, when creating or editing a question in Catalog Builder, users could define UI policies or dynamic behavior by selecting the UI policies icon \(![UI policies icon](../../product/service-catalog-management/image/dyn-beh-quest.png)\). This option has been removed. Now, users must directly use the UI Policy tab to add and manage the UI policies \(actions, conditions, scripts, and other required details\) to the catalog item.


## Activation information

Service Catalog is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **Now Assist in Catalog Builder**

    Use ServiceNow® Now Assist in Catalog Builder to create catalog items of your choice in Catalog Builder by giving text inputs.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

