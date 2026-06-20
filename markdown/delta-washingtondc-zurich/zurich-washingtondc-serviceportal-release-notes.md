---
title: Combined Service Portal release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Service Portal from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-serviceportal-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Service Portal release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Service Portal from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Portal release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Portal to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

After upgrading, you must specify the tables from which guest users can access data for any public widgets that accept the table input parameter. By default in the Washington DC release, public widgets that accept the table input parameter can't access and return data from any tables for guest users. If you added the **glide.service\_portal.widget.table\_allow\_list** or **glide.service\_portal.widget.allow\_list** system properties before upgrading, the values of these properties will be migrated to the Public Table Allow List for widgets after upgrading. For more information, see [Configure widget security](https://servicenow-staging.fluidtopics.net/access?context=configure-widget-security&family=washingtondc&ft:locale=en-US).

 Additionally, field-level read ACLs are enforced for filter conditions in Simple List widget instances by default. A new system property, **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list**, enforces these ACLs regardless of whether the **Enforce field-level Read ACLs on Filter query terms** option is selected for Simple List widget instances. To use the **Enforce field-level Read ACLs on Filter query terms** option, change the value of **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list** to false. For more information, see [Simple List widget](https://servicenow-staging.fluidtopics.net/access?context=simple-list-widget&family=washingtondc&ft:locale=en-US).

 If a user previously selected a user consent preference for user experience analytics for portals different from the rest of the platform, the preference selected for the platform is also used for portals in the Washington DC release. For example, if users opted out of tracking for portals but opted in to tracking for the rest of the platform in the Vancouver release, user experience analytics for portals are tracked for them in the Washington DC release. Users can update their selection from the user profile page in portals at any time.

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

Between your current release family and Zurich, new features were introduced for Service Portal.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Secure public widgets accessed by guest users](https://servicenow-staging.fluidtopics.net/access?context=configure-widget-security&family=washingtondc&ft:locale=en-US)**

Secure public widgets that accept the table input parameter by specifying the tables from which the widget can access and return data for guest users.

-   **[Close all portal notifications at once](https://servicenow-staging.fluidtopics.net/access?context=properties-service-portal&family=washingtondc&ft:locale=en-US)**

Close all notifications at once instead of having to close them individually by selecting **Clear All**. Portal administrators can use the **glide.service-portal.notification.threshold** system property to configure the number of notifications that must appear before displaying the **Clear All** option. The default value is five.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Deactivate portals](https://servicenow-staging.fluidtopics.net/access?context=deactivate-portal&family=xanadu&ft:locale=en-US)**

Turn off access to a portal that you don't want users to visit and redirect them to another portal.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Analyze the performance of portal pages and their widgets](https://servicenow-staging.fluidtopics.net/access?context=analyze-page-performance&family=yokohama&ft:locale=en-US)**

Set benchmarks against which to analyze the performance of a portal page. Identify widgets on the page that don't meet the performance benchmarks and view details about their performance.

-   **[Compare a cloned widget with its base widget](https://servicenow-staging.fluidtopics.net/access?context=compare-with-base-system&family=yokohama&ft:locale=en-US)**

Compare cloned widgets with the base widget from which they were cloned. View differences between the code of the cloned widget and the base widget highlighted in the code comparator.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Approval Info Record widget](https://servicenow-staging.fluidtopics.net/access?context=approval-info-record-widget&family=zurich&ft:locale=en-US)**

The Service Portal Approval Info Record widget shows details about the approval request and a full record for an approval including the activity stream.

The Approval Info Record widget and the new Now Assist Approval Assistance AI agent maintain parity. To use the new Approval Info Record widget, activate the Approval Details Page Route Map, and uptake the Approval Info Record widget in your custom page.

The new Now Assist Approval Assistance AI agent allows you to see your pending approvals, as well as the details about your pending approvals. For more information, see [Approval assistance AI agent](https://servicenow-staging.fluidtopics.net/access?context=platform-approval-aia&family=zurich&ft:locale=en-US).

-   **[Configure Service Portal Approval Configuration record](https://servicenow-staging.fluidtopics.net/access?context=configure-approval-assistance-ai-agent&family=zurich&ft:locale=en-US)**

Configure the Service Portal Approval Configuration record to make the Approval Assistance AI agent and Approval Info Record widget work better for your specific use case.

-   **[Configure widget loading order in Service Portal](https://servicenow-staging.fluidtopics.net/access?context=configure-widget-loading-order&family=zurich&ft:locale=en-US)**

As an admin, configure the widget loading order to defer their loading. This feature enables faster loading of the page and makes the widgets available for interaction as they load, thus improving the user experience.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Service Portal features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Critical notifications aren't automatically dismissed](https://servicenow-staging.fluidtopics.net/access?context=properties-service-portal&family=washingtondc&ft:locale=en-US)**

Show critical notifications tagged with the `sn-sticky-notification` HTML class attribute until you specifically dismiss them even when automatic dismissal is enabled for non-critical notifications with the **glide.service-portal.notification\_timeout.seconds** system property.

-   **[Unified user consent for tracking user experience analytics](https://servicenow-staging.fluidtopics.net/access?context=sp-analytics&family=washingtondc&ft:locale=en-US)**

Opt in to or out of tracking user experience analytics once for all platform interfaces. Previously, changes to your user consent selection to track user experience analytics in other platform interfaces weren’t honored in portals and vice versa. This choice is now stored centrally with the user consent management \(UCM\) capability used by the rest of the platform so a change for one interface is honored for all interfaces. For more information about user consent management, see [User privacy, tracking, and consent](https://servicenow-staging.fluidtopics.net/access?context=user-exp-analytics-track-options&family=washingtondc&ft:locale=en-US) in the Usage Insights documentation.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Show the current user in the team members list of the User Profile widget](https://servicenow-staging.fluidtopics.net/access?context=user-profile-widget&family=xanadu&ft:locale=en-US)**

Indicate whether to include the logged-in user in the team members list when viewing another team member's user profile from the User Profile widget.

-   **[Additional multi-factor authentication options](https://servicenow-staging.fluidtopics.net/access?context=mfa-use&family=xanadu&ft:locale=en-US)**

Log in to portals using a biometric authenticator or hardware security key with multi-factor authentication \(MFA\).


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Use ECMAScript 2021 \(ES12\) JavaScript mode in server scripts for widgets](https://servicenow-staging.fluidtopics.net/access?context=widget-dev-guide&family=yokohama&ft:locale=en-US)**

Use features supported in the ECMAScript 2021 \(ES12\) JavaScript mode in server-side scripts for widgets by selecting **Turn on ECMAScript 2021 \(ES12\) mode** from the widget record or Widget Editor. For information about features supported in the ECMAScript 2021 \(ES12\) JavaScript mode, see [JavaScript engine feature support](https://servicenow-staging.fluidtopics.net/access?context=javascript-engine-feature-support&family=yokohama&ft:locale=en-US).

-   **[Define roles for page route maps](https://servicenow-staging.fluidtopics.net/access?context=reroute-page&family=yokohama&ft:locale=en-US)**

Control which users are redirected to a new page based on a page route map. Specify the user roles to apply in the Page Route Map form.

-   **[Improved redirection for single sign-on \(SSO\) authentication](https://servicenow-staging.fluidtopics.net/access?context=c_SPSSOLoginAndRedirects&family=yokohama&ft:locale=en-US)**

Improved the experience of logging in to portals that use single sign-on \(SSO\) authentication by redirecting to the SSO Identify Provider \(IdP\) login page without trying to load the portal page first.

-   **[Enforce providing comments when rejecting requests](https://servicenow-staging.fluidtopics.net/access?context=approvals-widget&family=yokohama&ft:locale=en-US)**

Require approvers to provide comments when rejecting a request from the Approvals widget. Administrators can enable requiring comments from the widget instance options.

-   **[Check cross-scope privileges to a table with the Form widget](https://servicenow-staging.fluidtopics.net/access?context=form-widget&family=yokohama&ft:locale=en-US)**

Validate access to tables from which the Form widget fetches data. The Form widget checks for the necessary cross-scope privileges to a table by default.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Service Portal features or functionality were removed.

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

Between your current release family and Zurich, some Service Portal features or functionality were deprecated.

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

Review information on how to activate Service Portal.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Service Portal is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

Service Portal is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Service Portal is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Service Portal is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Portal we have noted them here.

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

If any specific browser requirements were introduced or changed for Service Portal we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The Washington DC release doesn't support Internet Explorer 11. The iOS version of Firefox doesn’t support Service Portal pages.

</td></tr><tr><td>

Xanadu

</td><td>

The Xanadu release doesn't support Internet Explorer 11.

 The iOS version of Firefox doesn’t support Service Portal pages.

 For more information about Service Portal browser support, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

The Yokohama release doesn't support Internet Explorer 11.

 The iOS version of Firefox doesn’t support Service Portal pages.

 For more information about Service Portal browser support, see [Browser support](https://servicenow-staging.fluidtopics.net/access?context=browser-support&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Service Portal, such as specific requirements or compliance levels.

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Portal we have noted them here.

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

If there are specific highlight considerations for Service Portal we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Secure public widgets that accept the table input parameter.
-   Show critical notifications until you dismiss them.
-   Opt in to or out of user experience analytics tracking once for all platform interfaces.
-   Clear all portal notifications at once.

 See [Service Portal](https://servicenow-staging.fluidtopics.net/access?context=c_ServicePortal&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

Deactivate a portal and optionally redirect users to an alternate portal.

 See [Service Portal](https://servicenow-staging.fluidtopics.net/access?context=c_ServicePortal&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Analyze the performance of portal pages and their widgets.
-   Compare cloned widgets with the base widget from which they were cloned.
-   Use ECMAScript 2021 \(ES12\) JavaScript mode in widget server scripts.
-   Enable early single sign-on \(SSO\) redirection.
-   Specify the user roles that apply to a page route map.

 See [Service Portal](https://servicenow-staging.fluidtopics.net/access?context=c_ServicePortal&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use the support for Service Portal in the iOS Google App.
-   As an admin, configure the widget load order on Service Portal pages.
-   As an admin, defer the loading of AI Search assets to enhance page performance.

 See [Service Portal](https://servicenow-staging.fluidtopics.net/access?context=c_ServicePortal&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

