---
title: Combined ServiceNow AI Platform core feature release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for ServiceNow AI Platform core feature from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-servicenowaiplatformcorefeature-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined ServiceNow AI Platform core feature release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for ServiceNow AI Platform core feature from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow AI Platform core feature release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow AI Platform core feature to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for ServiceNow AI Platform core feature.

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing ServiceNow AI Platform core feature features.

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


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some ServiceNow AI Platform core feature features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some ServiceNow AI Platform core feature features or functionality were deprecated.

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

