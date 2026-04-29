---
title: Service definitions with catalog items
description: Enable service definitions to use service catalog items. Agents can select these catalog items and use the associated record producers to create cases of the correct type in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Service definitions with catalog items

Enable service definitions to use service catalog items. Agents can select these catalog items and use the associated record producers to create cases of the correct type in CSM Configurable Workspace.

Users with the admin role can configure service definitions to use service catalog items. These catalog items are displayed as cards in the service selector. If a service definition has more than one associated service catalog item, the system shows all of the associated catalog items as cards in the service selector.

When an agent selects a catalog item from the service selector, the system displays the record producer associated with the catalog item in a workspace record page. Completing and submitting the record producer creates a case of the correct type and displays the case in CSM Configurable Workspace.

## Configuring a service definition to use catalog items

Users with the admin role can configure a service definition to use catalog items.

1.  [Create a service definition](../task/create-csm-service-definition.md) or edit an existing service definition record.
2.  Enable the **Use service catalog item** field.
3.  Add the associated catalog items for this service definition to the Catalog Service Relationships related list.

For more information, see [Configuring service definitions](csm-service-definitions-configure.md).

## Using a service definition with catalog items to create a case

For service definitions that are configured to use catalog items, agents can create cases by selecting a catalog item from the service selector. The system displays the record producer page associated with the catalog item in CSM Configurable Workspace.

The agent adds information to the record producer fields and selects **Submit**. The system creates the case and displays the record page for the correct case type.

## Information messages

If a service definition is configured to use service catalog items but does not have any associated catalog items in the Catalog Service Relationships related list, the system displays the following message: "A service definition has the "Use service catalog item" field enabled but has no associated catalog items for the user to select."

If an agent does not have access to the catalog item associated with a service definition, the system displays following message: "You do not have access to the selected catalog item. Request access from your manager so that you can use the catalog item to create a case."

## Service Definition record

The Service Definition record includes the **Use service catalog item** field. When this field is enabled, the system displays the catalog items in the service selector that are associated with the service definition.

The Catalog Service Relationships related list stores the catalog items that are associated with the service definition. A service definition can have one or more associated catalog items.

Users with the admin role can enable the **Use service catalog item** field on the Service Definition record and associate service catalog items in the Catalog Service Relationships related list.

## CSM record producer page

The CSM record producer page includes the service catalog UI Builder component, which can be associated with a record producer and displays the record producer fields.

The CSM record producer page is displayed for all service definition records that have the **Use service catalog item** field enabled and one or more associated catalog items.

Selecting a catalog item in the service selector displays the CSM record producer page in CSM Configurable Workspace. Completing and submitting the record producer displays the record page for the correct case type.

Default page settings:

-   Page name: CSM record producer page
-   Table: Record Producer \[sc\_cat\_item\_producer\]
-   Order: -1000

