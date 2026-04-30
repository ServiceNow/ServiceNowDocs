---
title: Now Assist: Fulfillment, access, and portal setting functions
description: In addition to catalogs, categories, and topics, Now Assist allows you to set three other key fields for a catalog item: Access, Fulfillment flow, and Portal settings. You can configure these simply by describing your requirements in plain language.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 2
breadcrumb: [Catalog item generation reference, Now Assist in Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Now Assist: Fulfillment, access, and portal setting functions

In addition to catalogs, categories, and topics, Now Assist allows you to set three other key fields for a catalog item: Access, Fulfillment flow, and Portal settings. You can configure these simply by describing your requirements in plain language.

## Setting access

Access controls are managed through two lists: "Available for," which specifies who can view and request the item, and "Not available for," which defines who is excluded. Both lists rely on User Criteria \(UC\) records. You can add multiple UC records to either list. Now Assist processes your input as follows:

-   Exact match found: The user criteria record is applied to the appropriate list automatically.
-   Multiple matches or no match found: Now Assist doesn't guess. It displays a prompt in the chat for you to search for and select or enter the correct user criteria record.

**Note:** User criteria records define groups of users based on conditions such as role, department, or location. These records manage who can view or request a catalog item.

## Setting the fulfillment flow

Each catalog item is limited to one fulfillment flow, which defines the process executed when a request is submitted. Now Assist handles fulfillment flow selection as follows:

-   Exact match found: The fulfillment flow is set automatically.
-   Multiple matches or no match found: Now Assist prompts you to select or enter the correct fulfillment flow in the chat.
-   Item uses an execution plan: If the catalog item already has an execution plan, Now Assist prevents a fulfillment flow from being added and explain why this field can't be changed.

## Setting portal settings

Portal settings for a catalog item can be updated using Now Assist, following the same process as for any other field.

## When a template is in control

If Access, Fulfillment, or Portal settings are locked due to template enforcement, these values can't be changed. When you attempt to update a locked field, Now Assist notifies you that the value is controlled by the template and is not editable.

## When some fields are locked and some are not

If you request updates to multiple fields and some are locked by a template while others remain editable, Now Assist will:

-   Apply updates to the fields that can be changed.
-   Notify you about which fields were not updated because they are controlled by the template.

**Note:** User criteria records define groups of users based on conditions such as role, department, or location. These records manage who can view or request a catalog item.

**Parent Topic:**[Catalog item generation reference](catalog-item-generation-reference.md)

