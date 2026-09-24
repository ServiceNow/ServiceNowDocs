---
title: Combined ServiceNow AI Platform core feature release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for ServiceNow AI Platform core feature from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-servicenowaiplatformcorefeature-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined ServiceNow AI Platform core feature release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for ServiceNow AI Platform core feature from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow AI Platform core feature release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow AI Platform core feature to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

The dynamic schema application framework was revised in the Zurich release. If you implemented dynamic schema in the Xanadu or Yokohama releases, the application is automatically migrated to a new framework as part of the upgrade to releases starting with the Zurich release. For details on the migration and steps you might need to perform, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow AI Platform core feature.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Access and test pre-release features](https://www.servicenow.com/docs/access?context=feature-preview-program&family=australia&ft:locale=en-US)**

The Feature Preview Program provides a centralized location to discover, activate, and test pre-release capabilities on your instance. When a pre-release feature is added to your instance, you receive a notification and can access the Feature Preview Program to review feature details, activate features for testing, and provide feedback.


 -   **[Enhance instance security for sandbox scripts with guarded script](https://www.servicenow.com/docs/access?context=guarded-script&family=australia&ft:locale=en-US)**

The guarded script evaluator restricts the JavaScript features and APIs available to untrusted, client-generated scripts running in the script sandbox environment. Beginning with the Australia Patch 2 release, incompatible scripts sent to the server by guest users are rejected on all instances by default. Scripts sent by authenticated users are evaluated using a phased approach to enforcement that varies by the type of instance to provide time to detect and review incompatible scripts before rejecting them. Scripts that use unsupported features are recorded in the Incompatible Guarded Scripts list, where you can rewrite them or create exemptions for scripts that can't be rewritten.


 -   **[Automatically generate request definitions for scripted REST API resources](https://www.servicenow.com/docs/access?context=autogenerate-api-request-definitions&family=australia&ft:locale=en-US)**

Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource and the related scripted REST API service.


 -   **[Granular read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US)**

Control the editability of read-only fields by configuring read-only options, allowing for customized behavior that balances usability and security. Read-only options provide granular control over whether read-only fields can be updated through client scripts and server-side operations. You can also test stricter read-only controls in non-production instances before implementing them in production.

-   **[Support for reference data types in Dynamic Schema](https://www.servicenow.com/docs/access?context=add-dynamic-attributes&family=australia&ft:locale=en-US)**

Create dynamic attributes using reference data types.

-   **[Work with Dynamic Schema elements in the Workspace condition builder](https://www.servicenow.com/docs/access?context=dynamic-schema&family=australia&ft:locale=en-US)**

Filter Workspace lists using dynamic schema elements in the condition builder.

-   **[Toggle the mail icon display](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&family=australia&ft:locale=en-US)**

Show or hide the mail icon in email fields by configuring the hide\_email\_icon dictionary attribute.

-   **[AI indicator in forms](https://www.servicenow.com/docs/access?context=c_FormFields&family=australia&ft:locale=en-US)**

Easily identify AI involvement across the ServiceNow AI Platform® through a visual cue that identifies form fields in configurable workspace and Core UI that have been updated with AI-generated content.

-   **[Guest API access control](https://www.servicenow.com/docs/access?context=c_RESTAPI&family=australia&ft:locale=en-US)**

Manage guest access to REST and GraphQL API endpoints using path-based ACLs while maintaining separate authenticated user controls.

-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=granular-admin-roles&family=australia&ft:locale=en-US)**

Grant specific permissions to developers or users who perform minor administrative tasks without granting them unrestricted access to the full admin role by reviewing and assigning available granular admin roles.

-   **[Optional trailing slash configuration](https://www.servicenow.com/docs/access?context=api-rest&family=australia&ft:locale=en-US)**

Align with external specifications and industry standards by configuring REST APIs with optional trailing slash support.

-   **[Path-based REST ACL control](https://www.servicenow.com/docs/access?context=api-rest&family=australia&ft:locale=en-US)**

Control access to REST services by creating path-based ACLs using specific HTTP method and path combinations.

-   **[Resource-level security configuration](https://www.servicenow.com/docs/access?context=api-rest&family=australia&ft:locale=en-US)**

Enable public access or custom ACL authorization by configuring resource-level security settings.

-   **[Address field type with auto-suggestions](https://www.servicenow.com/docs/access?context=address-field-type&family=australia&ft:locale=en-US)**

Reduce manual entry errors through a new Address field type for Core UI and Workspace forms, which provides real-time address suggestions displayed as you type.

-   **[New dot-walk scoping security properties and table attribute](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=australia&ft:locale=en-US)**

Strengthen scope boundary enforcement when dot-walking across application scopes using Reference Fields through additional properties and a table attribute. For more information, see the [Dot-Walk Scoping Security Enhancement \[KB2793170\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2793170) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Brazil

</td><td>

-   **AI indicators now visible in Core UI lists**

Rows in Core UI lists that are created or modified by an AI agent now display an AI indicator. The indicator clears automatically when a user makes an inline edit to the row, keeping the indicator accurate as data changes.

-   **Caching for repeated metadata queries**

The platform caches repeated metadata queries to optimize processing of metadata requests.

-   **[Monitor daily slow-pattern trends](https://www.servicenow.com/docs/access?context=daily_slow_patterns&family=brazil&ft:locale=en-US)**

Track day-over-day trends in slow-pattern data with daily snapshots that automatically identify new or worsening patterns. High-significance changes are highlighted in list views, helping you quickly spot meaningful changes and prioritize investigation efforts. Built-in data retention and filtering keep historical comparisons accurate and relevant for up to 33 days.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow AI Platform core feature features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Data Egress and Usage by Domain tabs added to the Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=inbound-api-integration-usage-dashboard&family=australia&ft:locale=en-US)**

View data volumes returned in integration responses and monitor domain-level usage.


 -   **[Country setting added to Language and Region preferences](https://www.servicenow.com/docs/access?context=next-experience-language-preferences&family=australia&ft:locale=en-US)**

Users can select their country from the Next Experience language and region preferences.

-   **[New options for date and time format in the User record](https://www.servicenow.com/docs/access?context=user&family=australia&ft:locale=en-US)**

Users can select from new options for Date format and Time format in the User record.

-   **[Control whether date and time formats reflect the user locale by default](https://www.servicenow.com/docs/access?context=set-localization-props&family=australia&ft:locale=en-US)**

Configure date and time formats to reflect the user locale when no date or time format has been selected in user preferences through the **glide\_i18n.date.default\_to\_locale** system property.

-   **[Control how to set the language for guest users](https://www.servicenow.com/docs/access?context=set-localization-props&family=australia&ft:locale=en-US)**

Use a guest user's IP address to set their language through the **glide\_i18n.ip\_geolocation** system property.

-   **[Activate additional choices for countries](https://www.servicenow.com/docs/access?context=activate-country-choices&family=australia&ft:locale=en-US)**

Activate additional choices for countries in the Next Experience language and region preferences or in a User record.

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://www.servicenow.com/docs/access?context=javascript-engine-feature-support&family=australia&ft:locale=en-US)**

Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[JavaScript engine updated with changes from the Rhino engine](https://www.servicenow.com/docs/access?context=updates-javascript-engine&family=australia&ft:locale=en-US)**

The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **[New Normalization Data Services system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=australia&ft:locale=en-US)**

Create duplicate records in core\_company extension tables by setting the **com.glide.acl\_check\_all\_filter\_on\_new** system property to true to reference account records.

-   **[System properties secured by default](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=australia&ft:locale=en-US)**

Glide properties that can impact instance security are set to secure values by default. For more information about which system properties are affected and why, see the [Glide Property Hardening \[KB1982254\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1982254) article in the Now Support Knowledge Base.

-   **[Tracking records in unauthenticated users' sessions](https://www.servicenow.com/docs/access?context=web-embeddables&family=australia&ft:locale=en-US)**

Track records created, modified, or deleted by unauthenticated users to enable session-based ACL access on public forms, portals, or workflows.

-   **[Manage guest user access to records](https://www.servicenow.com/docs/access?context=web-embeddables&family=australia&ft:locale=en-US)**

Restrict guest user access to records they created or updated during their current session using the 'is in session' condition builder on the ACL form for Sys ID fields.

-   **[Session-based guest access](https://www.servicenow.com/docs/access?context=web-embeddables&family=australia&ft:locale=en-US)**

Manage REST GraphQL security with path-based ACLs that are enforced without needing to require authentication for access to an API.


 -   **[Support duplicate company names across core\_company extension tables](https://www.servicenow.com/docs/access?context=enhanced-nds-for-duplicate-records&family=australia&ft:locale=en-US)**

Avoid normalization conflicts when creating records with the same company name in both the Company \[core\_company\] table and its extension tables, such as Customer Account \[customer\_account\], using the **glide.cmdb.canonical.use\_base\_core\_company\_only** property. It ensures that uniqueness enforcement applies only to base core\_company records.


</td></tr><tr><td>

Brazil

</td><td>

-   **[AI indicators updated for form fields](https://www.servicenow.com/docs/access?context=platai-ai-indicator-form-fields&family=brazil&ft:locale=en-US)**

AI indicators for form fields in Core UI and configurable workspaces now support AI color gradients and have been updated to reflect the latest ServiceNow Otto name and iconography.

-   **[TinyMCE version 8.3.0 upgrade](https://www.servicenow.com/docs/access?context=c_UseHTMLFields&family=brazil&ft:locale=en-US)**

The HTML editor in Core UI and configurable workspaces is upgraded from TinyMCE version 6.8.2 to version 8.3.0.

-   **[Text pattern configuration in the HTML editor](https://www.servicenow.com/docs/access?context=configuring-the-html-system-properties-in-tinymce&family=brazil&ft:locale=en-US)**

Text patterns in the HTML editor can now be turned on or off using the **glide.ui.html.editor.textpatterns** system property.

-   **[Configurable choice field empty option labels](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=brazil&ft:locale=en-US)**

Configure choice fields to display either None or --None-- for empty options using the **glide.ui.choice.display\_none** system property.

-   **[Base cross-scope access on the latest source code updates](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=brazil&ft:locale=en-US)**

Control how the system invalidates Restricted Caller Access records when a source code record, such as a script include, in a cross-scope access table is committed in an update set with the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property. By default, a database listener monitors update set commits on source code tables and invalidates RCA records at the time of the commits so that cross-scope access is based on the latest source code updates.

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://www.servicenow.com/docs/access?context=javascript-engine-feature-support&family=brazil&ft:locale=en-US)**

Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[JavaScript engine updated with changes from the Rhino engine](https://www.servicenow.com/docs/access?context=updates-javascript-engine&family=brazil&ft:locale=en-US)**

The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **[Configure row threshold for exports to Excel](https://www.servicenow.com/docs/access?context=c_ExportLimits&family=brazil&ft:locale=en-US)**

Configure the row limit for exports to Excel using the properties **glide.export.xls.max.rows.per.sheet** and **glide.export.xlsx.max.rows.per.sheet**.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some ServiceNow AI Platform core feature features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some ServiceNow AI Platform core feature features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

Starting with the Australia release, the legacy user interfaces commonly referred to as UI11 and UI15 are deprecated. These legacy UIs no longer receive enhancements or defect fixes, and will no longer be supported. Certain system features might continue to display through legacy rendering paths \(for example, printer‑friendly views\) and will be addressed case by case as part of ongoing platform improvements. Use the Next Experience for a modern, accessible, unified interface. For information about activating the Next Experience UI, see [Activation considerations](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&family=australia&ft:locale=en-US).

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow AI Platform core feature.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

The ServiceNow AI Platform core features are active by default.


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

The ServiceNow AI Platform core features are active by default.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow AI Platform core feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow AI Platform core feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow AI Platform core feature, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Accessibility information**

Format Painter plugin for TinyMCE enables you to apply consistent font styles, sizes, and table formats within the HTML editor field. This improvement helps users with cognitive disabilities and low vision by reducing confusion and supporting clear, predictable formatting throughout documents. Keyboard navigation is supported, providing added ease of use for keyboard-only users. For more information, see [Configure the HTML toolbar](https://www.servicenow.com/docs/access?context=t_ConfigureTheTinyMCEHTMLToolbar&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow AI Platform core feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow AI Platform core feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

Control whether read-only fields can be updated through client scripts and server-side operations by configuring read-only options.

 See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&family=australia&ft:locale=en-US) for more information.

 Use the Feature Preview Program to choose which pre-release capabilities to activate and test on your instance.

</td></tr><tr><td>

Brazil

</td><td>

-   Access platform capabilities, discover new applications, and get intelligent, actionable insights.
-   Install and manage licensed applications and plugins for your instance and understand your subscriptions and entitlements.
-   Configure core features, such as tables and data, users, search, notifications, and localization.
-   Maintain and monitor the ServiceNow AI Platform to identify issues or enhance performance.
-   Plan and manage ServiceNow AI Platform upgrades to patches and new releases.

 See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

