---
title: Service Catalog release notes
description: The ServiceNow Service Catalog application provides a requester view of the available services and products offered by the departments within your organization. Service Catalog was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Service Catalog release notes

The ServiceNow® Service Catalog application provides a requester view of the available services and products offered by the departments within your organization. Service Catalog was enhanced and updated in the Zurich release.

## Service Catalog highlights for the Zurich release

-   Enable catalog item creators to create complex catalog items in Catalog Builder with ease. They can create, edit, or delete client scripts, or create advanced reference qualifiers.
-   Help requesters complete catalog item forms faster on portals and Next Experience UIs using caller-provided key-value pairs that pre-fill catalog item forms.
-   Ease the work of catalog item requesters by letting them drag one or more attachments directly onto the form for faster submissions.
-   Use the Catalog browse component for an enhanced catalog item browsing experience on the Next Experience UI for catalog users.

See [Service Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/service-catalog.md) for more information.

## New in the Zurich release

-   **[Create complex catalog items in Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/create-client-scripts-in-catalog-builder.md)**

    Enable catalog item creators to create complex catalog items effortlessly in Catalog Builder.

    They can create, edit, or delete client scripts to build a complex catalog item. Creators can also configure questions, set dynamic and advanced reference qualifiers, and scripted default values.


-   **[Use Catalog browse component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/catalog-builder.md)**

    Use the Catalog browse component in UI Builder to add catalog item browsing in your custom pages. Drag it onto the Next Experience UI page to use the Catalog browse component.

    The component enables requesters to explore and request items from various catalogs and categories, providing a hierarchical view to sort by catalog, category, or subcategory. The component provides a grid or list view for items and a search function to search for items as needed.


## Changed in this release

-   **[A property to delete a draft of catalog item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/save-draft-catalog-item.md)**

    Use the property **glide.sc.delete\_draft\_item\_on\_version\_change** to determine whether to delete a saved draft of a catalog item on its modification.

-   **[Dynamic Lookup Choices and Enhanced Table Sourcing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/t_CreateAVariableForACatalogItem.md)**

    Lookup questions are now more flexible and user-friendly. You can effortlessly display choices directly from a specific table field, offering similar ease for select box configurations. Additionally, create dynamic dependent lookups where the choices refresh automatically based on the values selected in other fields on the same form, guiding users to more relevant selections.

-   **[Enhanced Sorting Control for Lookup Fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/t_CreateAVariableForACatalogItem.md)**

    Customize the display order in lookup select boxes, look up multiple choice, and list collector fields with the new **ref\_ac\_order\_by** attribute. This attribute enables options to be sorted primarily by a specified data column, and then by their display label, providing a more logical and predictable presentation for users.


## Activation information

Service Catalog is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/catalog-builder.md)**

    You can create or edit a catalog item \(catalog item or record producer\) using a visual and guided experience along with specified restrictions. The Catalog Builder experience enables you to delegate the creation and maintenance of the catalog.


-   **[AI Authoring for Catalog Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-for-catalog-generation.md)**

    Use ServiceNow® Now Assist in Catalog Builder to create catalog items of your choice in Catalog Builder by giving text inputs.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-capabilities-rn-landing.md)

