---
title: Combined ServiceNow AI Platform core feature release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for ServiceNow AI Platform core feature from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-servicenowaiplatformcorefeature-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined ServiceNow AI Platform core feature release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for ServiceNow AI Platform core feature from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow AI Platform core feature release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow AI Platform core feature to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   **Upgrade information**

The dynamic schema application framework has been revised in the Zurich release. If you implemented dynamic schema in Xanadu or Yokohama, the application is automatically migrated to a new framework as part of the upgrade to the Zurich release. For details on the migration, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

The dynamic schema application framework was revised in the Zurich release. If you implemented dynamic schema in the Xanadu or Yokohama releases, the application is automatically migrated to a new framework as part of the upgrade to releases starting with the Zurich release. For details on the migration and steps you might need to perform, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow AI Platform core feature.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Add dynamic attributes to a dynamic category](https://www.servicenow.com/docs/access?context=add-dynamic-attributes-dynamic-category&family=yokohama&ft:locale=en-US)**

Add individual attributes or a group of attributes to a dynamic category.

-   **[Reference a dynamic attribute or a list of dynamic attributes](https://www.servicenow.com/docs/access?context=create-dynamic-schema-reference&family=yokohama&ft:locale=en-US)**

Build a dependency between a dynamic attribute store field and either a dynamic attribute or a list of dynamic attributes.

-   **[Edit data in remote tables on an instance](https://www.servicenow.com/docs/access?context=create-remote-table-script&family=yokohama&ft:locale=en-US)**

Insert, update, and delete data in an external data source from a remote table on an instance when you enable editing for the table. Customize the script definitions that enable you to insert, update, or delete data from a remote table.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Hierarchical queries in condition builders](https://www.servicenow.com/docs/access?context=data-hierarchies&family=zurich&ft:locale=en-US)**

Simplify and build queries with fewer conditions using existing hierarchical data in a table. You can also define new hierarchical relationships between records that are in the same table.

-   **[Dynamic namespaces](https://www.servicenow.com/docs/access?context=create-dynamic-namespace&family=zurich&ft:locale=en-US)**

Define categories and attributes once and reuse them using dynamic namespaces across multiple tables and dynamic attribute store fields. A dynamic namespace is automatically created when you add a dynamic attribute store field.

-   **[Audit Management Console and audit retention](https://www.servicenow.com/docs/access?context=audit-mgmt-console&family=zurich&ft:locale=en-US)**

Simplify your audit data management and configuration by using the Audit Management Console module. It includes a new Retention option, which automates and simplifies the deletion of audit data based on your requirements.


</td></tr><tr><td>

Australia

</td><td>

-   **[Access and test pre-release features](https://www.servicenow.com/docs/access?context=feature-preview-program&family=australia&ft:locale=en-US)**

The Feature Preview Program provides a centralized location to discover, activate, and test pre-release capabilities on your instance. When a pre-release feature is added to your instance, you receive a notification and can access the Feature Preview Program to review feature details, activate features for testing, and provide feedback.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow AI Platform core feature features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Updated Access Control Lists \(ACLs\) for Transaction tables and Session Management tables](https://www.servicenow.com/docs/access?context=exploring-access-control-list&family=yokohama&ft:locale=en-US)**

The ACLs for a number of Transaction Management tables and Session Management tables have been updated to enhance security using a combination of Deny and Allow ACLs. All new ACLs have a security attribute. You must have the security attribute to add to the role list of an ACL. For more information, see [Configure an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&family=yokohama&ft:locale=en-US), [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&family=yokohama&ft:locale=en-US), and [\[Placeholder link text to key bundle-psec.allow-acl\]](https://www.servicenow.com/docs/access?context=allow-acl&family=yokohama&ft:locale=en-US).

The updated Transaction Management tables include:

    -   syslog
    -   syslog\_ajax
    -   syslog\_email
    -   syslog\_transaction
    -   syslog\_script
The updated Session Management tables include:

    -   sys\_audit
    -   sys\_security\_acl
    -   sys\_user\_auth
    -   sys\_user\_session
-   **[Configuring plugins for the TinyMCE HTML editor](https://www.servicenow.com/docs/access?context=configuring-the-html-plugins-for-tinymce&family=yokohama&ft:locale=en-US)**

The Accessibility Checker \(a11ychecker\) plugin is now available in the TinyMCE HTML editor. The plugin identifies WCAG and Section 508 accessibility violations and provides an auto-repair feature where applicable. To configure the plugin, see [Change the TinyMCE HTML editor plugins](https://www.servicenow.com/docs/access?context=change-the-tinymce-html-editor-plugins&family=yokohama&ft:locale=en-US). Additional configurations to the accessibility rules, like changing the WCAG level and HTML versions can also be done via **TinyMCEconfigscript** script.

-   **[Field types supported in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&family=yokohama&ft:locale=en-US)**

The following field types are now supported for use in a configurable workspace:

    -   Documentation\_field
    -   Domain\_path
    -   HTML\_Script
    -   Long
    -   Longint
    -   multi\_small
    -   Order index
    -   Radio
For more information, see [Field types reference](https://www.servicenow.com/docs/access?context=r_FieldTypes&family=yokohama&ft:locale=en-US).

-   **[Specify the tables that a REST API access policy restricts](https://www.servicenow.com/docs/access?context=create-api-access-policy&family=yokohama&ft:locale=en-US)**

Specify the tables that a Table REST API access policy applies to on the API Access Policy form.

-   **[Use ISO currency codes with the FX Currency field type](https://www.servicenow.com/docs/access?context=fx-currency&family=yokohama&ft:locale=en-US)**

Use three-digit ISO 4217 currency codes from the **Numeric code** field on the Currency \[fx\_currency\] table with fields of the FX Currency field type.

-   **[Sorting according to the session language](https://www.servicenow.com/docs/access?context=sorting-session-language&family=yokohama&ft:locale=en-US)**

Configure whether string values in columns are sorted according to the user's session language or English.

-   **[Columnstore index type](https://www.servicenow.com/docs/access?context=t_CreateCustomIndex&family=yokohama&ft:locale=en-US)**

Optimize data storage and retrieval by creating a columnstore index. This index type is available with RaptorDB Professional.


</td></tr><tr><td>

Zurich

</td><td>

-   **[AI indicator in forms](https://www.servicenow.com/docs/access?context=ai-indicator-in-configurable-workspace-and-core-ui&family=zurich&ft:locale=en-US)**

The AI indicator is a visual cue that identifies form fields in configurable workspace and Core UI that have been updated with AI-generated content. This feature enhances user experience by providing a consistent and clear indication of AI involvement across the platform.


</td></tr><tr><td>

Australia

</td><td>

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


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow AI Platform core feature features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow AI Platform core feature features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. Instead, [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&family=zurich&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

 -   The **glide.script.use.sandbox** system property has been removed. The script sandbox is enabled by default.
-   Dynamic groups have been removed. Instead, use dynamic attributes in dynamic categories to simplify administration and improve the dynamic schema user experience.

</td></tr><tr><td>

Australia

</td><td>

Starting with the Australia release, the legacy user interfaces commonly referred to as UI11 and UI15 are deprecated. These legacy UIs no longer receive enhancements or defect fixes, and will no longer be supported. Certain system features might continue to display through legacy rendering paths \(for example, printer‑friendly views\) and will be addressed case by case as part of ongoing platform improvements. Use the Next Experience for a modern, accessible, unified interface. For information about activating the Next Experience UI, see [Activation considerations](https://www.servicenow.com/docs/access?context=next-experience-adoption-paths&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow AI Platform core feature.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

The ServiceNow AI Platform core features are active by default.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

The ServiceNow AI Platform core features are active by default.


</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

-   **Accessibility information**

Format Painter plugin for TinyMCE enables you to apply consistent font styles, sizes, and table formats within the HTML editor field. This improvement helps users with cognitive disabilities and low vision by reducing confusion and supporting clear, predictable formatting throughout documents. Keyboard navigation is supported, providing added ease of use for keyboard-only users. For more information, see [Configure the HTML toolbar](https://www.servicenow.com/docs/access?context=t_ConfigureTheTinyMCEHTMLToolbar&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow AI Platform core feature we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   Streamline how you access help content on the system events and job scheduling dashboard by accessing the appropriate help content in each tab.
-   Insert, update, and delete data in an external data source from a remote table.

 See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Simplify and build queries with fewer conditions by leveraging hierarchical relationships in a condition builder.
-   Use additional scripting features, including Promises and Async await, with the ECMAScript 2021 \(ES12\) JavaScript mode.
-   Define dynamic categories and dynamic attributes once and reuse them using dynamic namespaces across multiple tables and dynamic attribute store fields.

 See [Administer](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&family=zurich&ft:locale=en-US) for more information.

 Use the Feature Preview Program to choose which pre-release capabilities to activate and test on your instance.

</td></tr><tr><td>

Australia

</td><td>

Control whether read-only fields can be updated through client scripts and server-side operations by configuring read-only options.

 See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&family=australia&ft:locale=en-US) for more information.

 Use the Feature Preview Program to choose which pre-release capabilities to activate and test on your instance.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

