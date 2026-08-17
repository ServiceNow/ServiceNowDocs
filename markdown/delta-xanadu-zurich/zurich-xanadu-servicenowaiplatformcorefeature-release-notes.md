---
title: Combined ServiceNow AI Platform core feature release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for ServiceNow AI Platform core feature from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-servicenowaiplatformcorefeature-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined ServiceNow AI Platform core feature release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for ServiceNow AI Platform core feature from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow AI Platform core feature release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow AI Platform core feature to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

The dynamic schema application framework has been revised in the Zurich release. If you implemented dynamic schema in Xanadu or Yokohama, the application is automatically migrated to a new framework as part of the upgrade to the Zurich release. For details on the migration, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for ServiceNow AI Platform core feature.

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

-   **[Enhance instance security for sandbox scripts with guarded script](https://www.servicenow.com/docs/access?context=guarded-script&family=yokohama&ft:locale=en-US)**

The guarded script evaluator restricts the JavaScript features and APIs available to untrusted, client-generated scripts running in the script sandbox environment. Beginning with the Yokohama Patch 13 release, incompatible scripts sent to the server by guest users are rejected on all instances by default. Scripts sent by authenticated users are evaluated using a phased approach to enforcement that varies by the type of instance to provide time to detect and review incompatible scripts before rejecting them. Scripts that use unsupported features are recorded in the Incompatible Guarded Scripts list, where you can rewrite them or create exemptions for scripts that can't be rewritten.

-   **[Add dynamic attributes to a dynamic category](https://www.servicenow.com/docs/access?context=add-dynamic-attributes-dynamic-category&family=yokohama&ft:locale=en-US)**

Add individual attributes or a group of attributes to a dynamic category.

-   **[Reference a dynamic attribute or a list of dynamic attributes](https://www.servicenow.com/docs/access?context=create-dynamic-schema-reference&family=yokohama&ft:locale=en-US)**

Build a dependency between a dynamic attribute store field and either a dynamic attribute or a list of dynamic attributes.

-   **[Edit data in remote tables on an instance](https://www.servicenow.com/docs/access?context=create-remote-table-script&family=yokohama&ft:locale=en-US)**

Insert, update, and delete data in an external data source from a remote table on an instance when you enable editing for the table. Customize the script definitions that enable you to insert, update, or delete data from a remote table.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Access and test pre-release features](https://www.servicenow.com/docs/access?context=feature-preview-program&family=zurich&ft:locale=en-US)**

The Feature Preview Program provides a centralized location to discover, activate, and test pre-release capabilities on your instance. When a pre-release feature is added to your instance, you receive a notification and can access the Feature Preview Program to review feature details, activate features for testing, and provide feedback.

-   **[Enhance instance security for sandbox scripts with guarded script](https://www.servicenow.com/docs/access?context=guarded-script&family=zurich&ft:locale=en-US)**

The guarded script evaluator restricts the JavaScript features and APIs available to untrusted, client-generated scripts running in the script sandbox environment. Beginning with the Zurich Patch 9 release, incompatible scripts sent to the server by guest users are rejected on all instances by default. Scripts sent by authenticated users are evaluated using a phased approach to enforcement that varies by the type of instance to provide time to detect and review incompatible scripts before rejecting them. Scripts that use unsupported features are recorded in the Incompatible Guarded Scripts list, where you can rewrite them or create exemptions for scripts that can't be rewritten.

-   **[Hierarchical queries in condition builders](https://www.servicenow.com/docs/access?context=data-hierarchies&family=zurich&ft:locale=en-US)**

Simplify and build queries with fewer conditions using existing hierarchical data in a table. You can also define new hierarchical relationships between records that are in the same table.

-   **[Dynamic namespaces](https://www.servicenow.com/docs/access?context=create-dynamic-namespace&family=zurich&ft:locale=en-US)**

Define categories and attributes once and reuse them using dynamic namespaces across multiple tables and dynamic attribute store fields. A dynamic namespace is automatically created when you add a dynamic attribute store field.

-   **[Experimentation framework](https://www.servicenow.com/docs/access?context=experimentation-framework&family=zurich&ft:locale=en-US)**

Help enable innovation by trying new ServiceNow® feature variants in your instance. Only single customer instances or Gen AI Innovation Program participants have early access to new innovations via experimentation framework. You can opt out of specific experiments or turn off the framework entirely.

-   **[Audit Management Console and audit retention](https://www.servicenow.com/docs/access?context=audit-mgmt-console&family=zurich&ft:locale=en-US)**

Simplify your audit data management and configuration by using the Audit Management Console module. It includes a new Retention option, which automates and simplifies the deletion of audit data based on your requirements.

-   **[Monitor requestors' API usage rates through the Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=inbound-api-integration-usage-dashboard&family=zurich&ft:locale=en-US)**

Inbound integrations track web service requests for OAuth registered applications and user accounts making those requests.

-   **[Use schemas to define the structure and format of REST API responses and requests](https://www.servicenow.com/docs/access?context=define-scripted-rest-api-schema&family=zurich&ft:locale=en-US)**

When you define a schema in the ServiceNow AI Platform, the schema can be used to define the structure of requests and responses within the associated REST API. The schema data for the requests and responses is then available in the exportable OpenAPI specification for the API.

-   **[Automatically generate request definitions for scripted REST API resources](https://www.servicenow.com/docs/access?context=autogenerate-api-request-definitions&family=zurich&ft:locale=en-US)**

Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource and the related scripted REST API service.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing ServiceNow AI Platform core feature features.

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

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://www.servicenow.com/docs/access?context=javascript-engine-feature-support&family=zurich&ft:locale=en-US)**

Use additional scripting features, including Promises and Async await, in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[Stream multipart responses with REST APIs](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=zurich&ft:locale=en-US)**

Stream multipart responses rather than buffering responses until complete by default with REST APIs that support the multipart/mixed requests, such as the Batch API. The **glide.rest.serialize.disable\_response\_stream\_buffering** system property controls this behavior and applies only to instances configured with Application Delivery Controller, version 2 \(ADCv2\).

-   **[Additional field types supported in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&family=zurich&ft:locale=en-US)**

The following field types are now supported for use in a configurable workspace:

    -   **datetime**
    -   **email\_script**
    -   **int**
    -   **integer\_time**
    -   **related\_tags**
    -   **user\_input**
-   **[Vertical layout configuration for radio buttons in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&family=zurich&ft:locale=en-US)**

Configurable workspaces now support a vertical layout configuration of radio buttons.

-   **[More dictionary attributes available for selected fields in a configurable workspace](https://www.servicenow.com/docs/access?context=r_FieldTypes&family=zurich&ft:locale=en-US)**

Applicable fields used in a configurable workspace now support the following dictionary attributes:

    -   **choice**
    -   **decimal**
    -   **float**
    -   **html\_editor**
    -   **integer**
    -   **ip\_addr**
    -   **is\_searchable\_choice**
    -   **phone\_number\_e164**
    -   **readonly\_clickthrough**
    -   **ref\_ac\_columns**
    -   **translated\_html\_editor**
    -   **types**
-   **[New plugins available for the TinyMCE HTML editor](https://www.servicenow.com/docs/access?context=configuring-the-html-plugins-for-tinymce&family=zurich&ft:locale=en-US)**

The TinyMCE HTML editor now supports two new plugins in Core UI and configurable workspaces:

    -   The Image Editing \(editimage\) plugin adds a contextual editing toolbar to images in the editor.
    -   The Help plugin \(help\) enables you to check shortcuts and keyboard navigation for accessibility.
-   **[New run types available for scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&family=zurich&ft:locale=en-US)**

The following run types are now available for all scheduled job types, enabling flexible scheduling:

    -   **Day and Month in Year**
    -   **Day in Week in Month in Year**
    -   **Week in Month**
The new run types are available in the following standard scheduled job types:

    -   **Scheduled Email of Report**
    -   **Scheduled Entity Generation**
    -   **Scheduled Script Execution**
To enable these new run types in other scheduled job child tables, you must configure your applicable form view to include the fields **Day**, **Month**, and **Year**. For more information, see [Enable run types for scheduled job child tables](https://www.servicenow.com/docs/access?context=customize-run-times-for-scheduled-jobs&family=zurich&ft:locale=en-US).

-   **[New advanced options available for scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&family=zurich&ft:locale=en-US)**

The following new advanced options are available when configuring scheduled jobs, offering greater flexibility in job planning, execution, and recurrence:

    -   **Starting**
    -   **Ending**
    -   **Repeat every**
-   **[Export lists to Google Sheets](https://www.servicenow.com/docs/access?context=setup-gsheet-export&family=zurich&ft:locale=en-US)**

Export your lists to Google Sheets directly from the Export menu.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some ServiceNow AI Platform core feature features or functionality were removed.

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

-   The **glide.script.use.sandbox** system property has been removed. The script sandbox is enabled by default.
-   Dynamic groups have been removed. Instead, use dynamic attributes in dynamic categories to simplify administration and improve the dynamic schema user experience.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some ServiceNow AI Platform core feature features or functionality were deprecated.

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

</td></tr><tr><td>

Zurich

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

</td></tr><tr><td>

Zurich

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

-   ****

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

