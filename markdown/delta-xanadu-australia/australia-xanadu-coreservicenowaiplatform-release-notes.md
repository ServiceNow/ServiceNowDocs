---
title: Combined Core ServiceNow AI Platform release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Core ServiceNow AI Platform from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-coreservicenowaiplatform-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Core ServiceNow AI Platform release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Core ServiceNow AI Platform from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Core ServiceNow AI Platform release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Core ServiceNow AI Platform to Australia

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

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Core ServiceNow AI Platform.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Dynamic schema for storing attributes](https://www.servicenow.com/docs/access?context=dynamic-schema&family=xanadu&ft:locale=en-US)**

Create and store structured groups of attributes and their values in a dynamic attribute store field.

-   **[Use ECMAScript 2021 \(ES12\) features in any server-side script](https://www.servicenow.com/docs/access?context=set-es12-mode-scripts&family=xanadu&ft:locale=en-US)**

Use the latest JavaScript features supported with ECMAScript 2021 \(ES12\) mode in individual scripts in applications that use ES5 Standards mode or Compatibility mode. From a script’s record, select **Turn on ECMAScript 2021 \(ES12\) mode**.

-   **[Automated jobs scheduling and manual scaling of jobs](https://www.servicenow.com/docs/access?context=auto-job-scheduling&family=xanadu&ft:locale=en-US)**

Starting with the Xanadu release, you can opt for automated job scheduling using queue registration. Select a queue in the new event form. As an admin, you can also manually define the number of jobs running at a queue level by scaling it either up or down as required in the Queue Details form.

-   **[Migrate existing sys event applications to Message Processing Framework](https://www.servicenow.com/docs/access?context=auto-job-scheduling&family=xanadu&ft:locale=en-US)**

Migrate your existing sys event queues to Message Processing Framework. You can also roll back a queue back to its previous configurations.

-   **[Geo point functions](https://www.servicenow.com/docs/access?context=platform-support-functions&family=xanadu&ft:locale=en-US)**

Convert longitude and latitude columns to a geo point field. Convert a geo point field or any valid numeric values or columns into longitude and latitude columns or values.

-   **[System Events and Scheduled Jobs enhancements](https://www.servicenow.com/docs/access?context=track-events&family=xanadu&ft:locale=en-US)**

Try the new **Active Jobs** tile in the System Events dashboard that states the number of jobs associated for a queue in processing framework. You can also review the details of the completed jobs by using the new **Stuck Jobs** and **Permanent Error Jobs** tiles on the Scheduled Jobs dashboard.


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
</table>## Changes

Between your current release family and Australia, some changes were made to existing Core ServiceNow AI Platform features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[TinyMCE upgrade](https://www.servicenow.com/docs/access?context=c_UseHTMLFields&family=xanadu&ft:locale=en-US)**

The HTML editor field now uses upgraded version of TinyMCE. TinyMCE has been upgraded from v4 to v6.8.2. This upgrade provides enhanced table functions as well as enhanced formatting and editing features like accordion, addition of custom styles through dictionary attributes, enable/disable text menubar, enhanced power paste. These enhancements enable users to format content to better suit their needs. Add the supported plugins to the system property **glide.ui.html.editor.enabled\_plugins​** and add the supported toolbar options to the system property **glide.ui.html.editor.toolbar** to configure the editor according to your needs. The upgrade includes changes in plugin names, toolbar names and new system properties to support configurations for the new version.

-   **[Business calendar enhancements](https://www.servicenow.com/docs/access?context=define-business-calendar-entries&family=xanadu&ft:locale=en-US)**

Business calendar enhancements include the ability to create business calendar spans and their names \(accessible across both global and scoped applications\), add a new calendar field called **Calendar type**, and differentiate more easily between similar calendar names.

-   **[Send REST Request - Inbound test step supports mutual authentication](https://www.servicenow.com/docs/access?context=atf-send-rest-request-inbound&family=xanadu&ft:locale=en-US)**

Use mutual authentication with the **Send REST Request - Inbound** test step by selecting an X.509 certificate.

-   **[Apply ACLs to GraphQL API paths](https://www.servicenow.com/docs/access?context=build-graphql-scripted-schema&family=xanadu&ft:locale=en-US)**

Specify which level of a GraphQL API to apply ACLs to with the **Path ACL Depth** field.

-   **[REST and SOAP API analytics dashboards migrated to Platform Analytics experience](https://www.servicenow.com/docs/access?context=c_APIAnalyticsReports&family=xanadu&ft:locale=en-US)**

The REST and SOAP API analytics dashboards have been migrated from Core UI to the Platform Analytics experience. Access the dashboards from **All** &gt; **System Web Services** &gt; **Analytics Usage Overview**. After upgrading, the Core UI dashboards are still available from **All** &gt; **System Web Services**.

-   **[Control access for HTTP headers in CORS requests](https://www.servicenow.com/docs/access?context=t_DefineACORSRule&family=xanadu&ft:locale=en-US)**

Configure whether to allow credentials in requests with the **Access-Control-Allow-Credentials** field and which HTTP headers to allow in requests with the **Access-Control-Allow-Headers** field.

-   **[Deactivate CORS rules](https://www.servicenow.com/docs/access?context=t_DefineACORSRule&family=xanadu&ft:locale=en-US)**

Turn a CORS rule \[sys\_cors\_rule\] on or off with the **Active** field.

-   **[Rhino update for the JavaScript engine on the platform](https://www.servicenow.com/docs/access?context=c_JS_engine_upgrade&family=xanadu&ft:locale=en-US)**

Rhino was updated to improve the performance of the JavaScript engine on the platform.

-   **[Web requests from integration users update the Last login and Last login time fields on user records](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&family=xanadu&ft:locale=en-US)**

By default, the Last login and Last login time fields in a user record \[sys\_user\] are updated when an integration user sends a web request to an instance. To turn off this functionality, set both the **glide.basicauth.update\_last\_login\_time** and the **glide.oauth.update\_last\_login\_time** system properties to false.


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
</table>## Removed

Between your current release family and Australia, some Core ServiceNow AI Platform features or functionality were removed.

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

Between your current release family and Australia, some Core ServiceNow AI Platform features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   The System Performance Dashboard is deprecated as of the Xanadu release. [Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&family=xanadu&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more.
-   Starting with the Xanadu release, Application Insights is being prepared for future deprecation. It will be hidden and no longer available in the ServiceNow Store but will continue to be supported. Instead, [Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&family=xanadu&ft:locale=en-US) offers a powerful solution for enhancing system performance. Contact your account manager to discover more. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

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
</table>## Activation information

Review information on how to activate Core ServiceNow AI Platform.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

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

If any specific browser requirements were introduced or changed for Core ServiceNow AI Platform we have noted them here.

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

Review details on accessibility information for Core ServiceNow AI Platform, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

</td></tr><tr><td>

Australia

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

If there are specific highlight considerations for Core ServiceNow AI Platform we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Use ECMAScript 2021 \(ES12\) features in any server-side script.
-   The TinyMCE upgrade from V4 to V6.8.2 includes enhanced formatting options and editing, as well as extended functions to enable users to format their content to better suit their needs.
-   Capture multiple attributes and their values in a single column instead of adding new columns to a table.
-   Experience the new Automatic Jobs Scheduling feature with rollback and configuration retrieval abilities for events processing.

 See [Administer the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&family=xanadu&ft:locale=en-US) for more information.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

