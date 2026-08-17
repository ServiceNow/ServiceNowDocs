---
title: Combined Service Catalog release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Service Catalog from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-servicecatalog-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Service Catalog release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Service Catalog from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Catalog release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Catalog to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Service Catalog.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Create complex catalog items in Catalog Builder](https://www.servicenow.com/docs/access?context=create-client-scripts-in-catalog-builder&family=zurich&ft:locale=en-US)**

Enable catalog item creators to create complex catalog items effortlessly in Catalog Builder.

They can create, edit, or delete client scripts to build a complex catalog item. Creators can also configure questions, set dynamic and advanced reference qualifiers, and scripted default values.


-   **[Use Catalog browse component](https://www.servicenow.com/docs/access?context=catalog-builder&family=zurich&ft:locale=en-US)**

Use the Catalog browse component in UI Builder to add catalog item browsing in your custom pages. Drag it onto the Next Experience UI page to use the Catalog browse component.

The component enables requesters to explore and request items from various catalogs and categories, providing a hierarchical view to sort by catalog, category, or subcategory. The component provides a grid or list view for items and a search function to search for items as needed.


</td></tr><tr><td>

Australia

</td><td>

-   **[Enable editing of catalog items by multiple users](https://www.servicenow.com/docs/access?context=set-up-cat-builder&family=australia&ft:locale=en-US)**

Enable other users, who are added to the **Secondary owner** field, to edit catalog items. To enable these users, add people to the **Secondary owner** user-criteria field in the sc\_cat\_item and sc\_cat\_item\_producer tables, enabling others to make changes to catalog items owned by another person.

-   **[Define and add stages in fulfilment step](https://www.servicenow.com/docs/access?context=configure-flow-sf-flow&family=australia&ft:locale=en-US)**

Define and add distinct stages and states in the fulfillment step when building a catalog item in Catalog Builder, enabling requesters to view the request-related current stages and their states together.

-   **[Use advanced UI policy capabilities in Catalog Builder](https://www.servicenow.com/docs/access?context=set-up-cat-builder&family=australia&ft:locale=en-US)**

Configure catalog UI policies with scripts and multiple catalog UI policy actions in the Catalog Builder to facilitate the creation of complex catalog items. With these enhancements, catalog item creators can confidently take advantage of advanced options, simplifying and speeding up the entire catalog development process.

-   **[Configure variable visibility on multi-row variable set grids](https://www.servicenow.com/docs/access?context=service-catalog&family=australia&ft:locale=en-US)**

Configure the visibility of a variable on the grid layout within a multi-row variable set \(MRVS\) for a catalog item by using the **Hide on grid** check box. By default, the check box is not selected.

-   **[Configure update set prefix](https://www.servicenow.com/docs/access?context=service-catalog&family=australia&ft:locale=en-US)**

Configure the update set prefix to set a custom name for the update set that gets generated automatically in Catalog Builder, making update sets easy to identify and track for consistency. Use the **glide.sc.cb.item.update\_set\_prefix** property to standardize update set names. By default, the property uses the value **CB\_$\{template\_name\}\_$\{item\_name\}\_$\{timestamp\}**.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Service Catalog features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[A property to delete a draft of catalog item](https://www.servicenow.com/docs/access?context=save-draft-catalog-item&family=zurich&ft:locale=en-US)**

Use the property **glide.sc.delete\_draft\_item\_on\_version\_change** to determine whether to delete a saved draft of a catalog item on its modification.

-   **[Dynamic Lookup Choices and Enhanced Table Sourcing](https://www.servicenow.com/docs/access?context=t_CreateAVariableForACatalogItem&family=zurich&ft:locale=en-US)**

Lookup questions are now more flexible and user-friendly. You can effortlessly display choices directly from a specific table field, offering similar ease for select box configurations. Additionally, create dynamic dependent lookups where the choices refresh automatically based on the values selected in other fields on the same form, guiding users to more relevant selections.

-   **[Enhanced Sorting Control for Lookup Fields](https://www.servicenow.com/docs/access?context=t_CreateAVariableForACatalogItem&family=zurich&ft:locale=en-US)**

Customize the display order in lookup select boxes, look up multiple choice, and list collector fields with the new **ref\_ac\_order\_by** attribute. This attribute enables options to be sorted primarily by a specified data column, and then by their display label, providing a more logical and predictable presentation for users.


</td></tr><tr><td>

Australia

</td><td>

-   **[Use UI Policy tab to add and manage the UI policies](https://www.servicenow.com/docs/access?context=create-ui-policies-in-catalog-builder&family=australia&ft:locale=en-US)**

Previously, when creating or editing a question in Catalog Builder, users could define UI policies or dynamic behavior by selecting the UI policies icon \(\[Omitted image "image.dyn-beh-quest"\] Alt text: UI policies icon\). This option has been removed. Now, users must directly use the UI Policy tab to add and manage the UI policies \(actions, conditions, scripts, and other required details\) to the catalog item.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Service Catalog features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Service Catalog features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Service Catalog.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Service Catalog is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Service Catalog is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Catalog we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Service Catalog we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Service Catalog, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Catalog we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Service Catalog we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Enable catalog item creators to create complex catalog items in Catalog Builder with ease. They can create, edit, or delete client scripts, or create advanced reference qualifiers.
-   Help requesters complete catalog item forms faster on portals and Next Experience UIs using caller-provided key-value pairs that pre-fill catalog item forms.
-   Ease the work of catalog item requesters by letting them drag one or more attachments directly onto the form for faster submissions.
-   Use the Catalog browse component for an enhanced catalog item browsing experience on the Next Experience UI for catalog users.

 See [Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Enable other users, who are added to the **Secondary owner** field, to edit catalog items.
-   Let your requesters view the stage and the state of their requests while using the service fulfillment step.
-   Configure catalog UI policies with scripts and multiple catalog UI policy actions in the Catalog Builder to facilitate the creation of complex catalog items.
-   Hide or show variables on a grid layout of the multi-row variable set \(MRVS\) for a catalog item.
-   Configure the update set prefix to set a custom name for the update set that gets generated automatically in the Catalog Builder.

 See [Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

