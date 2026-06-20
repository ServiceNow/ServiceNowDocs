---
title: Combined Core ServiceNow AI Platform release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Core ServiceNow AI Platform from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-coreservicenowaiplatform-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Core ServiceNow AI Platform release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Core ServiceNow AI Platform from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Core ServiceNow AI Platform release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Core ServiceNow AI Platform to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Previously, if a transaction was canceled, certain auditable operations were not being recorded. This behavior of missing audit records is because the platform executes some operations between the record change and is canceled before audit creation. But now, audits are created immediately after the record is changed, reducing the chance of a canceled transaction aborting the operation before the audit is recorded. To facilitate this update, audits are now recorded in the same thread as the transaction. Earlier audits were created in a background thread.

 This change redefines the default value of the `glide.db.audit.lazy` property from true to false. Ideally, this property is not defined in the Properties table, which means that the majority of instances start using the new default value and behavior with the Washington DC release. On some instances, this property may have been inserted with the value set to true, which means that these instances won’t be able to use this change to audit behavior. Delete this property to leverage this update.

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

Between your current release family and Zurich, new features were introduced for Core ServiceNow AI Platform.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Arabic language support](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateALanguage&family=washingtondc&ft:locale=en-US)**

Accommodate Arabic-language users with Arabic translations of the base system UI string content in your instance. Activate the I18N: Arabic Translations plugin \(com.snc.i18n.arabic\) to get these translations.

-   **[GraphQL Explorer](https://servicenow-staging.fluidtopics.net/access?context=test-gql-schema&family=washingtondc&ft:locale=en-US)**

Test GraphQL APIs using an integrated GraphQL testing tool. The GraphQL Explorer facilitates the development and debugging of GraphQL APIs.

-   **[Support for JavaScript modules and third-party libraries with the ServiceNow SDK](https://servicenow-staging.fluidtopics.net/access?context=servicenow-sdk-landing&family=washingtondc&ft:locale=en-US)**

Create custom JavaScript modules to organize and reuse code, improve maintainability, and leverage functionality from third-party JavaScript libraries in scoped applications with the ServiceNow SDK. Use the ServiceNow SDK to create, download, and modify scoped applications with custom modules and third-party libraries in Visual Studio Code and then deploy those applications to an instance.

-   **[Improvements for archiving related records](https://servicenow-staging.fluidtopics.net/access?context=c_ArchiveData&family=washingtondc&ft:locale=en-US)**

When defining related records, control the depth of cascading by specifying the archive rule for each archive related record. Related records without a specified archive rule aren't cascaded.

-   **[Drop custom indexes](https://servicenow-staging.fluidtopics.net/access?context=drop-custom-index&family=washingtondc&ft:locale=en-US)**

Drop custom indexes using the Tables module.

-   **[Flow logic for remote tables](https://servicenow-staging.fluidtopics.net/access?context=create-remote-table-flow&family=washingtondc&ft:locale=en-US)**

Build a flow to retrieve data for a remote table query. Use the ServiceNow® capabilities of triggers and actions to respond to triggers and fetch remote data.

-   **[New sys property to enable locale-based language sorting](https://servicenow-staging.fluidtopics.net/access?context=show-hide-filter&family=washingtondc&ft:locale=en-US)**

Enable the **guide.ui.condition\_builder.sort\_labels\_by\_locale** system property to sort the fields of the Show/hide filter according to the locale-based language. The system property is set to False by default.

-   **[Show Syslog Records UI action](https://servicenow-staging.fluidtopics.net/access?context=r_LogUtilities&family=washingtondc&ft:locale=en-US)**

Use the new **Show Syslog Records** UI action on Transactions and Active Transactions forms to view any System Log entries that were generated during the execution of the transaction.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Dynamic schema for storing attributes](https://servicenow-staging.fluidtopics.net/access?context=dynamic-schema&family=xanadu&ft:locale=en-US)**

Create and store structured groups of attributes and their values in a dynamic attribute store field.

-   **[Use ECMAScript 2021 \(ES12\) features in any server-side script](https://servicenow-staging.fluidtopics.net/access?context=set-es12-mode-scripts&family=xanadu&ft:locale=en-US)**

Use the latest JavaScript features supported with ECMAScript 2021 \(ES12\) mode in individual scripts in applications that use ES5 Standards mode or Compatibility mode. From a script’s record, select **Turn on ECMAScript 2021 \(ES12\) mode**.

-   **[Automated jobs scheduling and manual scaling of jobs](https://servicenow-staging.fluidtopics.net/access?context=auto-job-scheduling&family=xanadu&ft:locale=en-US)**

Starting with the Xanadu release, you can opt for automated job scheduling using queue registration. Select a queue in the new event form. As an admin, you can also manually define the number of jobs running at a queue level by scaling it either up or down as required in the Queue Details form.

-   **[Migrate existing sys event applications to Message Processing Framework](https://servicenow-staging.fluidtopics.net/access?context=auto-job-scheduling&family=xanadu&ft:locale=en-US)**

Migrate your existing sys event queues to Message Processing Framework. You can also roll back a queue back to its previous configurations.

-   **[Geo point functions](https://servicenow-staging.fluidtopics.net/access?context=platform-support-functions&family=xanadu&ft:locale=en-US)**

Convert longitude and latitude columns to a geo point field. Convert a geo point field or any valid numeric values or columns into longitude and latitude columns or values.

-   **[System Events and Scheduled Jobs enhancements](https://servicenow-staging.fluidtopics.net/access?context=track-events&family=xanadu&ft:locale=en-US)**

Try the new **Active Jobs** tile in the System Events dashboard that states the number of jobs associated for a queue in processing framework. You can also review the details of the completed jobs by using the new **Stuck Jobs** and **Permanent Error Jobs** tiles on the Scheduled Jobs dashboard.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Core ServiceNow AI Platform features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Warning when plugin upgrade or activation fails](https://servicenow-staging.fluidtopics.net/access?context=c_ServiceNowPlugins&family=washingtondc&ft:locale=en-US)**

A warning message now appears if the alter or create table operation fails when upgrading or activating a plugin.

-   **[System tables excluded from archive rules](https://servicenow-staging.fluidtopics.net/access?context=t_CreateAnArchiveRule&family=washingtondc&ft:locale=en-US)**

You can no longer create archive rules for certain tables.

-   **[Link a destroy rule with an archive rule](https://servicenow-staging.fluidtopics.net/access?context=t_CreateADestructionRule&family=washingtondc&ft:locale=en-US)**

You must now specify a related archive rule when creating an archive destroy rule. Linking an archive rule to the archive destroy rule improves performance when deleting archived records.

-   **[Peripheral records deleted with archive destroy](https://servicenow-staging.fluidtopics.net/access?context=t_CreateADestructionRule&family=washingtondc&ft:locale=en-US)**

Peripheral records in the Journal Entry \[sys\_journal\_field\], Attachment \[sys\_attachment\], and Sys Audit \[sys\_audit\] tables are now automatically deleted when data is deleted during an archive destroy.

-   **[Enhanced Capacity feature in remote tables](https://servicenow-staging.fluidtopics.net/access?context=remote-tables&family=washingtondc&ft:locale=en-US)**

Enhanced Capacity enables additional rows to be stored for a remote table if the retrieved data exceeds 1,000 rows.

-   **[Non-cancellable audit records](https://servicenow-staging.fluidtopics.net/access?context=exploring-auditing&family=washingtondc&ft:locale=en-US)**

Reduce the chances of audit records not being written when a transaction is canceled with the new default setting.

-   **[Notification and meeting invitation changes on Granular Delegate form](https://servicenow-staging.fluidtopics.net/access?context=create-delegation-admin&family=washingtondc&ft:locale=en-US)**

The **All Notifications** and **Meeting invitations** options on the Granular Delegate form are now set to False by default, to avoid concerns around getting notifications that have security critical and sensitive data. You can select these options if you want the delegate to receive the delegation notification and meeting invitations.

-   **[Enhanced logging security improvements](https://servicenow-staging.fluidtopics.net/access?context=enhanced-log-security&family=washingtondc&ft:locale=en-US)**

Explore the new field in the node log lines to identify the script or component that generated the log message. Transaction start lines include a new field specifying what type of request was made.

-   **[Localization of product and application names](https://servicenow-staging.fluidtopics.net/access?context=c_LangInternationalizationSupport&family=washingtondc&ft:locale=en-US)**

Existing product and application names are being localized incrementally in supported languages, starting with Dutch, French, French \(Canadian\), German, Korean, Italian, Japanese, Portuguese \(Brazilian\), and Spanish. New product and application names are localized in all supported languages.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[TinyMCE upgrade](https://servicenow-staging.fluidtopics.net/access?context=c_UseHTMLFields&family=xanadu&ft:locale=en-US)**

The HTML editor field now uses upgraded version of TinyMCE. TinyMCE has been upgraded from v4 to v6.8.2. This upgrade provides enhanced table functions as well as enhanced formatting and editing features like accordion, addition of custom styles through dictionary attributes, enable/disable text menubar, enhanced power paste. These enhancements enable users to format content to better suit their needs. Add the supported plugins to the system property **glide.ui.html.editor.enabled\_plugins​** and add the supported toolbar options to the system property **glide.ui.html.editor.toolbar** to configure the editor according to your needs. The upgrade includes changes in plugin names, toolbar names and new system properties to support configurations for the new version.

-   **[Business calendar enhancements](https://servicenow-staging.fluidtopics.net/access?context=define-business-calendar-entries&family=xanadu&ft:locale=en-US)**

Business calendar enhancements include the ability to create business calendar spans and their names \(accessible across both global and scoped applications\), add a new calendar field called **Calendar type**, and differentiate more easily between similar calendar names.

-   **[Send REST Request - Inbound test step supports mutual authentication](https://servicenow-staging.fluidtopics.net/access?context=atf-send-rest-request-inbound&family=xanadu&ft:locale=en-US)**

Use mutual authentication with the **Send REST Request - Inbound** test step by selecting an X.509 certificate.

-   **[Apply ACLs to GraphQL API paths](https://servicenow-staging.fluidtopics.net/access?context=build-graphql-scripted-schema&family=xanadu&ft:locale=en-US)**

Specify which level of a GraphQL API to apply ACLs to with the **Path ACL Depth** field.

-   **[REST and SOAP API analytics dashboards migrated to Platform Analytics experience](https://servicenow-staging.fluidtopics.net/access?context=c_APIAnalyticsReports&family=xanadu&ft:locale=en-US)**

The REST and SOAP API analytics dashboards have been migrated from Core UI to the Platform Analytics experience. Access the dashboards from **All** &gt; **System Web Services** &gt; **Analytics Usage Overview**. After upgrading, the Core UI dashboards are still available from **All** &gt; **System Web Services**.

-   **[Control access for HTTP headers in CORS requests](https://servicenow-staging.fluidtopics.net/access?context=t_DefineACORSRule&family=xanadu&ft:locale=en-US)**

Configure whether to allow credentials in requests with the **Access-Control-Allow-Credentials** field and which HTTP headers to allow in requests with the **Access-Control-Allow-Headers** field.

-   **[Deactivate CORS rules](https://servicenow-staging.fluidtopics.net/access?context=t_DefineACORSRule&family=xanadu&ft:locale=en-US)**

Turn a CORS rule \[sys\_cors\_rule\] on or off with the **Active** field.

-   **[Rhino update for the JavaScript engine on the platform](https://servicenow-staging.fluidtopics.net/access?context=c_JS_engine_upgrade&family=xanadu&ft:locale=en-US)**

Rhino was updated to improve the performance of the JavaScript engine on the platform.

-   **[Web requests from integration users update the Last login and Last login time fields on user records](https://servicenow-staging.fluidtopics.net/access?context=r_AvailableSystemProperties&family=xanadu&ft:locale=en-US)**

By default, the Last login and Last login time fields in a user record \[sys\_user\] are updated when an integration user sends a web request to an instance. To turn off this functionality, set both the **glide.basicauth.update\_last\_login\_time** and the **glide.oauth.update\_last\_login\_time** system properties to false.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Core ServiceNow AI Platform features or functionality were removed.

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

Between your current release family and Zurich, some Core ServiceNow AI Platform features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Starting with the Washington DC release, Internet Explorer and Internet Explorer mode in Edge are no longer supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Xanadu

</td><td>

-   The System Performance Dashboard is deprecated as of the Xanadu release. [Impact Instance Observer](https://servicenow-staging.fluidtopics.net/access?context=io-overview&family=xanadu&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more.
-   Starting with the Xanadu release, Application Insights is being prepared for future deprecation. It will be hidden and no longer available in the ServiceNow Store but will continue to be supported. Instead, [Impact Instance Observer](https://servicenow-staging.fluidtopics.net/access?context=io-overview&family=xanadu&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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

Review information on how to activate Core ServiceNow AI Platform.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Core ServiceNow AI Platform is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

ServiceNow AI Platform is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Core ServiceNow AI Platform we have noted them here.

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

If any specific browser requirements were introduced or changed for Core ServiceNow AI Platform we have noted them here.

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

Review details on accessibility information for Core ServiceNow AI Platform, such as specific requirements or compliance levels.

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

-   **TinyMCE Upgrade**

Tiny MCE is an open-source rich text editor used in the HTML editor field. The upgrade of TinyMCE from v.4 to v.6.8.2 provides the following accessibility improvements:

    -   **Keyboard**:
        -   The color picker slider is now accessible using both keyboards and screen readers.
        -   There is also now a check mark to indicate the color selected by the user.
        -   The close dialog buttons in the modal dialogs are now accessible.
        -   The keyboard focus indicator is now clearly visible in the font color selection menu items.
    -   **Screen reader**:
        -   The selected value of drop-down menus like **Font** and **Font-size** is now announced by the screen reader.
    -   **Low vision**:
        -   The script editor and the HTML editor tool bar is now dark theme compatible.
-   **Admin Center and Adoption Blueprints accessibility enhancements**

Accessibility issues have been fixed for the following personas as part of Xanadu in Admin Center and Adoption Blueprints:

    -   persona\_low\_vision
    -   persona\_no\_vision
    -   persona\_color
    -   persona\_auditory
    -   persona\_speech
    -   persona\_cognitive
    -   persona\_physical

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Core ServiceNow AI Platform we have noted them here.

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

If there are specific highlight considerations for Core ServiceNow AI Platform we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Create a flow and set the triggers and actions for a remote table to retrieve data from external sources. If the retrieved data is large, use the Enhanced Capacity feature in the remote tables.
-   Test GraphQL APIs with the GraphQL Explorer.
-   Reduce the chances of missing audits being recorded when a transaction is canceled by creating the audits immediately after the record is modified.
-   Manage cascading when archiving multiple levels of related records.

 See [Administer the ServiceNow AI Platform](https://servicenow-staging.fluidtopics.net/access?context=intro-now-platform-landing&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Use ECMAScript 2021 \(ES12\) features in any server-side script.
-   The TinyMCE upgrade from V4 to V6.8.2 includes enhanced formatting options and editing, as well as extended functions to enable users to format their content to better suit their needs.
-   Capture multiple attributes and their values in a single column instead of adding new columns to a table.
-   Experience the new Automatic Jobs Scheduling feature with rollback and configuration retrieval abilities for events processing.

 See [Administer the ServiceNow AI Platform](https://servicenow-staging.fluidtopics.net/access?context=intro-now-platform-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

