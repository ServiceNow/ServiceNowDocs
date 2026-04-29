---
title: Service Portal properties
description: Service Portal properties control aspects of the portal experience for admin and end users.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 6
breadcrumb: [Service Portal reference, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Portal properties

Service Portal properties control aspects of the portal experience for admin and end users.

The most commonly used Service Portal properties are set on the Service Portal properties page. Some less commonly used properties are available only from the System Properties \[sys\_properties\] table.

You can access the properties listed in the following table by navigating to **All** &gt; **Service Portal** &gt; **Properties**.

<table id="table_gnx_g1d_mz"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default 404 page \(page ID or sp\_page sys\_id\) for Service Portal

 **glide.service\_portal.default\_404\_page**

</td><td>

Set the default page that your users see whenever a page can’t load properly.-   Type: string
-   Default value: 404
-   Learn more: [Assign a default error page](create-a-default-404-page.md)

The string must match the name of the page exactly.

</td></tr><tr><td>

Show a message to admin users in Service Portal pages if a browser error is encountered

 **glide.sp.show\_console\_error**

</td><td>

-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

Maximum number of stream entries displayed in Service Portal \(activity widget, conversation widget, and so on\)

 **glide.service\_portal.stream\_entry\_limit**

</td><td>

Limit the number of entries users can see in the ticket conversation widget. Users only see the most recent entries and can’t go further back in the history than the maximum allowed amount.-   Type: integer
-   Default value: 100

</td></tr><tr><td>

Duration \(in seconds\) info and error messages persist in the Service Portal before auto-dismissal

 **glide.service-portal.notification\_timeout.seconds**

</td><td>

Set the duration in seconds that non-critical notifications remain on the screen before they are auto-dismissed. If set to 0, messages do not auto-dismiss and require that a user close them.

 -   Type: integer
-   Default value: 5

 Critical notifications should be tagged with the `sn-sticky-notification` HTML class attribute to prevent them from being automatically dismissed.

 If the glide.ui.accessibility preference is enabled, messages don’t auto-dismiss, regardless of the system property value. To set this preference, see [Enabling accessibility features](../../../administer/accessibility-508-compliance/concept/c_SetUpSect508ComplianceFeature.md#).

</td></tr><tr><td>

Default sort order for announcements**glide.service\_portal.announcement.default\_sort\_order**

</td><td>

Define the sort order for banner announcements. -   Type: choice list
-   Default value: Start Date Descending

 Options include:

-   Start Date Ascending: The oldest start date appears first.
-   Start Date Descending: The most recent start date appears first.
-   End Date Ascending: The oldest end date appears first.
-   End Date Descending: The most recent end date appears first.

</td></tr><tr><td>

Enable debug runtime information**glide.sp.debug**

</td><td>

Controls whether the Angular.js flag **$compileProvider.debugInfoEnabled** is set to true or false. This option allows debug runtime information in the compiler, such as adding binding information and a reference to the current scope on to DOM elements. This property is turned off by default to improve performance on the instance. -   Type: true \| false
-   Default value: false

</td></tr></tbody>
</table>If [user criteria](user-criteria.md) \[**com.glide.service-portal.user-criteria**\] is enabled, the following properties also appear in the Service Portal properties page:

<table id="search"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr id="user-crit"><td>

Enable use of User Criteria records instead of Roles fields for Service Portal entitlements

 **glide.service\_portal.user\_criteria\_enabled**

</td><td>

Define permissions for Service Portal widgets, widget instances, pages, and search sources.

 -   Type: true \| false
-   Default value: true
-   More information: [User criteria for Service Portal](user-criteria.md)

</td></tr><tr><td>

List of roles \(comma-separated\) that bypass User Criteria validation in Service Portal

 **glide.sp.entitlement.override**

</td><td>

Allow users with a specific role to see any page, widget, widget instance, or search source regardless of user criteria.-   Type: string
-   Default value: admin

</td></tr></tbody>
</table>You can access the properties listed in the following table in the System Properties \[sys\_properties\] table.

<table id="table_ccw_gdy_fvb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list**

</td><td>

Option to always enforce read ACLs for filter conditions specified in Simple List widget instances. If false, the **Enforce field-level Read ACLs on Filter query terms** option in Simple List widget instances determines whether to enforce the ACLs.

 -   Type: true \| false
-   Default value: true
-   For more information, see [Simple List widget](simple-list-widget.md).

</td></tr><tr><td>

**glide.service\_portal.enable\_human\_readable\_urls**

</td><td>

Option to allow configuring human readable keywords in portal page URLs for the instance.

 -   Type: true \| false
-   Default value: true
-   For more information, see [Add human readable keywords to page URLs](../task/add-human-readable-keywords-page-urls.md).

</td></tr><tr><td>

**glide.service\_portal.enforce\_cross\_scope\_check\_in\_form**

</td><td>

Option to enforce validating cross-scope privileges to a table when the form widget fetches data from a table.-   Type: true \| false
-   Default value: true
-   For more information, see [Form widget](form-widget.md).

</td></tr><tr><td>

**glide.service-portal.notification.threshold**

</td><td>

Specify how many notifications should appear before users have the option to clear all notifications at once.

 -   Type: integer
-   Default value: 5

</td></tr><tr><td>

**glide.service\_portal.sso.early\_redirect.portals**

</td><td>

Redirects users to the SSO Identify Provider \(IdP\) login page without first redirecting them to the portal login page. Provide a comma-separated list of portal suffixes.**Note:** If your portal uses a customized version of the Login widget, you must update the `sp_sso_early_redirection` UI macro as needed to redirect users to the SSO Identify Provider \(IdP\) login page without trying to load the portal page first.

-   Type: String
-   Default value: None
-   For more information, see [Single sign-on, logins, and URL redirects](c_SPSSOLoginAndRedirects.md#).

</td></tr><tr><td>

**glide.sp.portals.language\_selector\_enabled**

</td><td>

Allows any user to choose and view content in their preferred language.This property contains a list of portal sys IDs separated by commas. By default, the sys IDs for the Knowledge \(/kb\), Customer Support \(/csm\), and Customer Service \(/csp\) portals are included. For any portal specified, the language selector appears in the portal header if any languages are installed and active on the instance in addition to English.

-   Type: string
-   Default value: 2086b814c3221200f3897bfaa2d3aea8,89275a53cb13020000f8d856634c9c51,45d6680fdb52220099f93691f0b8f5ad
-   For more information, see [Enable a language selector in portal headers](../task/configure-header-menu.md#).

</td></tr><tr><td>

**glide.sp.starting.page.ignore.list**

</td><td>

Ignores intermediate pages used during SSO authentication in order for users to be directed to their starting page rather than an intermediate page. Provide a comma-separated list of page IDs.-   Type: String
-   Default value: login\_with\_sso,idp\_disco

</td></tr><tr><td>

**glide.sp.theme.parse\_scss**

</td><td>

Option to allow compiled SCSS files to be loaded as links to improve repeat page view performance. If set to false, SCSS files are included inline in the page HTML instead.

 -   Type: true \| false
-   Default value: true

</td></tr><tr><td>

**sp\_allow\_perf\_debug\_option\_for\_portals**

</td><td>

Specify the portals to evaluate using the Performance Analyzer by providing a comma-separated list of portal suffixes. For users with the sp\_admin or admin roles, the Performance Analyzer icon \(![Open Performance Analyzer](../image/performance-analyzer-icon.png)\) appears on pages in the specified portals.-   Type: String
-   Default value: sp
-   For more information, see [Evaluate the performance of a portal page](../task/analyze-page-performance.md).

</td></tr></tbody>
</table>**Parent Topic:**[Service Portal reference](reference-service-portal.md)

