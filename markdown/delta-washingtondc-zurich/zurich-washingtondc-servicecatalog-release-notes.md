---
title: Combined Service Catalog release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Service Catalog from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-servicecatalog-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Service Catalog release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Service Catalog from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Catalog release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Catalog to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Service Catalog.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **Save catalog item forms as drafts**

Enable catalog item requesters to save the drafts of the catalog item forms on the portals, such as the ServiceNow® Employee Center and ServiceNow® Service Portal, and on the Now® Mobile app.

Requesters can save the drafts when they come across situations, such as lengthy forms and requesters that don't have enough information to submit the record but don't want to discard the forms. They can save the draft and start editing from wherever they left off. Requesters can access the saved drafts from the My Request widget in a new **Drafts** tab.

-   **[Set values for questions in catalog items](https://servicenow-staging.fluidtopics.net/access?context=t_CreatUIPolicyForSvcCalgIt&family=washingtondc&ft:locale=en-US)**

Set values in Catalog UI Policy Actions for questions in a catalog item without the need to script. The value that you set for the question is displayed when the specified condition is met. You can set the values using Catalog UI Policy Actions in the ServiceNow AI Platform and using dynamic behavior in Catalog Builder.

For example, on a catalog item to order a company phone, you might want to automatically set the color to black if the storage size selected is 1 TB because that's the only option available. You can now configure this behavior without the need to write any scripts.

**Note:**

After upgrading from any previous release to Washington DC release, the **Clear the variable value** check box will not be displayed. If you’ve already selected the **Clear the variable value** check box in any previous release, then in the Washington DC release, this option is automatically set as **Clear value** in the Value action drop-down list.

For the attachment and masked variables, you will still view the Clear the variable value option to clear the value in the Washington DC release.

-   **[Set field message for questions in catalog items](https://servicenow-staging.fluidtopics.net/access?context=edit-question-cat-builder&family=washingtondc&ft:locale=en-US)**

Set field messages for the questions in a catalog item without the need to script. Field messages appear below the question as helpful text when a specified condition is met. You can set the field messages using the Catalog UI Policy Actions in the ServiceNow AI Platform and using the dynamic behavior in Catalog Builder.

For example, you can set a warning message to be displayed on the type of laptop question to read `Advanced laptop would need department head approval` when the type that you chose is **Advanced**.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Added inline render type support of catalog item in Virtual Agent](https://servicenow-staging.fluidtopics.net/access?context=request-topic-blocks-va&family=xanadu&ft:locale=en-US)**

Fill a catalog item form inline in the Virtual Agent powered by Natural Language Understanding \(NLU\).

For example, while requesting a catalog item that’s marked inline render type, the requester can fill the item and its options within the Virtual Agent conversation.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Use non-English language for creating or editing catalog items](https://servicenow-staging.fluidtopics.net/access?context=create-item-cat-builder&family=yokohama&ft:locale=en-US)**

Enable your users to use supported languages when creating or editing catalog items. A non-English language user can create or edit a catalog item in their language that is supported in Catalog Builder. For example, if a Spanish language user logs in to Catalog Builder and creates or edits an item, the Spanish version of the item is created or updated.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create complex catalog items in Catalog Builder](https://servicenow-staging.fluidtopics.net/access?context=create-client-scripts-in-catalog-builder&family=zurich&ft:locale=en-US)**

Enable catalog item creators to create complex catalog items effortlessly in Catalog Builder.

They can create, edit, or delete client scripts to build a complex catalog item. Creators can also configure questions, set dynamic and advanced reference qualifiers, and scripted default values.


-   **[Use Catalog browse component](https://servicenow-staging.fluidtopics.net/access?context=catalog-builder&family=zurich&ft:locale=en-US)**

Use the Catalog browse component in UI Builder to add catalog item browsing in your custom pages. Drag it onto the Next Experience UI page to use the Catalog browse component.

The component enables requesters to explore and request items from various catalogs and categories, providing a hierarchical view to sort by catalog, category, or subcategory. The component provides a grid or list view for items and a search function to search for items as needed.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Service Catalog features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[A property to delete a draft of catalog item](https://servicenow-staging.fluidtopics.net/access?context=save-draft-catalog-item&family=zurich&ft:locale=en-US)**

Use the property **glide.sc.delete\_draft\_item\_on\_version\_change** to determine whether to delete a saved draft of a catalog item on its modification.

-   **[Dynamic Lookup Choices and Enhanced Table Sourcing](https://servicenow-staging.fluidtopics.net/access?context=t_CreateAVariableForACatalogItem&family=zurich&ft:locale=en-US)**

Lookup questions are now more flexible and user-friendly. You can effortlessly display choices directly from a specific table field, offering similar ease for select box configurations. Additionally, create dynamic dependent lookups where the choices refresh automatically based on the values selected in other fields on the same form, guiding users to more relevant selections.

-   **[Enhanced Sorting Control for Lookup Fields](https://servicenow-staging.fluidtopics.net/access?context=t_CreateAVariableForACatalogItem&family=zurich&ft:locale=en-US)**

Customize the display order in lookup select boxes, look up multiple choice, and list collector fields with the new **ref\_ac\_order\_by** attribute. This attribute enables options to be sorted primarily by a specified data column, and then by their display label, providing a more logical and predictable presentation for users.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Service Catalog features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Service Catalog features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

Service Catalog is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

Service Catalog is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Service Catalog is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Accessibility checker in the TinyMCE toolbar enables you to identify and resolve accessibility related issues when creating a catalog item in Service Catalog. See [Accessibility checker in the toolbar](https://servicenow-staging.fluidtopics.net/access?context=service-catalog-accessibility-checker&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Washington DC

</td><td>

-   Let your catalog item requesters save drafts of catalog item forms so that requesters can edit the drafts later.
-   Set values for questions in a catalog item without the need to script in the ServiceNow AI Platform® and Catalog Builder.
-   Set field messages for the questions in a catalog item without the need to script in the ServiceNow AI Platform and Catalog Builder.
-   Experience the support for single check box in Virtual Agent for catalog conversations.

 See [Service Catalog](https://servicenow-staging.fluidtopics.net/access?context=service-catalog&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Fill a catalog item form inline in the Virtual Agent conversation.
-   Let users experience the support of Zero Trust Access \(ZTA\) security model for Service Catalog.
-   Experience the faster loading of popular catalog items in the Popular Items widgets.

 See [Service Catalog](https://servicenow-staging.fluidtopics.net/access?context=service-catalog&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enable your users to experience the flexibility of using supported languages when creating or editing catalog items in Catalog Builder.
-   Identify and resolve accessibility-related issues during catalog item generation through a new accessibility checker button in the TinyMCE toolbar in Service Catalog.

 See [Service Catalog](https://servicenow-staging.fluidtopics.net/access?context=service-catalog&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Enable catalog item creators to create complex catalog items in Catalog Builder with ease. They can create, edit, or delete client scripts, or create advanced reference qualifiers.
-   Help requesters complete catalog item forms faster on portals and Next Experience UIs using caller-provided key-value pairs that pre-fill catalog item forms.
-   Ease the work of catalog item requesters by letting them drag one or more attachments directly onto the form for faster submissions.
-   Use the Catalog browse component for an enhanced catalog item browsing experience on the Next Experience UI for catalog users.

 See [Service Catalog](https://servicenow-staging.fluidtopics.net/access?context=service-catalog&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

