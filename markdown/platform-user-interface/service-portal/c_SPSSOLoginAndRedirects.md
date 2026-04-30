---
title: Single sign-on, logins, and URL redirects
description: Service Portal uses a combination of system properties and script includes to determine how the system handles URL redirects for users logging in to the portal.Direct all unauthenticated users to a portal login page to log in. The portal login page becomes the primary login page for your instance.Conditionally redirect users to a Service Portal page after logging in.Debug the URL redirects for logging in to Service Portal and redirecting to the first page.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Single sign-on, logins, and URL redirects

Service Portal uses a combination of system properties and script includes to determine how the system handles URL redirects for users logging in to the portal.

Only users who understand SSO, URL redirects, and the ServiceNow platform should make any changes.

## Single sign-on and Service Portal

To use single sign-on with Service Portal, you must enable the Integration - Multiple Provider Single Sign-On Installer plugin \(com.snc.integration.sso.multi.installer\).

If you are using the system property to automatically redirect to your primary IdP, then Service Portal automatically redirects to that IdP. If you have multiple identity providers, Service Portal shows a link on the login page to **Use external login**. For more information on SSO and authentication in the platform, see [Multiple-Provider single sign-on \(SSO\)](https://www.servicenow.com/docs/access?context=c_MultipleProviderSingleSignOn&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

To redirect users to the SSO Identify Provider \(IdP\) login page without first redirecting them to the portal login page, you can configure the **glide.service\_portal.sso.early\_redirect.portals** system property. For more information, see [Service Portal properties](properties-service-portal.md). If your portal uses a customized version of the Login widget, you must update the `sp_sso_early_redirection` UI macro as needed to redirect users to the SSO Identify Provider \(IdP\) login page without trying to load the portal page first.

**Note:** Service Portal has a known issue related to using Multi-Provider SSO and Okta. For more information about this issue and a workaround, see the [Service Portal: After enabling Multi SSO, end users are able to access navpage.do through OKTA if they are already logged in \[KB0687717\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0687717) article in the Now Support Knowledge Base.

## Require authentication for a Service Portal page

If you want to require authentication for a Service Portal page, ensure that the **Public** flag on the page record is not selected. For more information, see [Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#). If a user navigates to a non-public page, they are redirected to the login page for the requested portal.

Because every page request is routed through the **$sp** page, this page must be public. The following values in the Public Pages `sys_public` table define the page as public:

-   **Page**: `$sp`
-   **Active**: `true`

**Parent Topic:**[Managing portal access](portal-security.md)

## Configure a portal as the instance login page

Direct all unauthenticated users to a portal login page to log in. The portal login page becomes the primary login page for your instance.

### Before you begin

Role required: admin

### Procedure

1.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) with the following settings:

    -   Name: glide.entry.page.script
    -   Type: string
    -   Value:

        ```
        new SPEntryPage().getLoginURL()
        ```

2.  If you need to direct users to a portal other than the default portal, edit the portal specified in the SPEntryPage script include.

    SPEntryPage uses the default portal on the instance as the portal path to redirect to. Employee Center \(esc\) is the default portal by default.

    **Note:** If you edit the script include, it won't be upgraded with future updates.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    2.  From the Script Includes \[sys\_script\_include\] table, search for a script include named **SPEntryPage**.

    3.  In the **Script** field, edit the script to change the assigned portal to the portal\_suffix you want.

        For example, change `this.portal = this.getDefaultPortal();` to `this.portal = "/sp/";` to redirect to Service Portal.

        ```javascript
        SPEntryPage.prototype = {
        
            initialize: function() {
                this.logVariables = false; // for debugging 
                this.portal = this.getDefaultPortal(); // The URL suffix for default portal
            },
        
        ```

        **Note:** The slash character \(/\) after `/sp` may cause issues when configuring single sign-on. If you're experiencing issues, try removing the character from the script.


## Redirect to Service Portal after login

Conditionally redirect users to a Service Portal page after logging in.

### Before you begin

Role required: admin

### Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  In the System Properties \[sys\_properties\] table, add the following properties and values.

<table id="table_sx1_5cn_sv"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.entry.first.page.script

</td><td>

string

</td><td>

`new SPEntryPage().getFirstPageURL()`

</td><td>

First page after authentication

</td></tr><tr><td>

glide.entry.page.script

</td><td>

string

</td><td>

Server script that redirects users to where to log in. For example:`new SPEntryPage().getLoginURL()`

</td><td>

Contains the call to the server script include method that determines where to log in

</td></tr></tbody>
</table>    getFirstPageURL primarily does the following:

    -   Redirects to `login_redirect.do` to break out of the frameset \(if there is one\).
    -   Redirects to the default portal if the user has no roles or to the full platform for users with roles who are not trying to go to a portal directly.

        When the user has no roles, they are redirected to the portal equivalent of a page. For example,

        `https://<instance_name>.service-now.com/nav_to.do?uri=change_request_list.do`

        sends users without roles to:

        `https://<instance_name>.service-now.com/sp/?id=list&table=change_request`.

    **Note:** This change does not prevent users without roles from accessing the full platform. To prevent users without roles from accessing the platform and always redirect to a portal, set the value of the **glide.entry.loggedin.page\_ess** system property to the portal suffix, such as `/sp`.

3.  Customize the after-login behavior in the **SPEntryPage** script include.

    For more information about modifying script includes, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

    For example, if you want users with certain roles to be redirected to Service Portal, you could modify `user.hasRoles()` in the following code.

    ```
    if (user.hasRoles() && !redirectURL && !isServicePortalURL)
    ```

    **Note:**

    -   If you edit the script include, it won't be upgraded with future updates.
    -   Users with the admin role always pass a `user.hasRoles()` check.
    -   If you are using external authentication, ensure that your IdP supports the RelayState URL parameter. This parameter retains the originally requested URL while the user authenticates, and is necessary for redirection after login.

### What to do next

To debug redirection, see [Debug Service Portal URL redirects](c_SPSSOLoginAndRedirects.md#). For additional redirection troubleshooting information, see the [Frequently Asked Questions on redirection with service portal \[KB0747432\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0747432) article in the Now Support Knowledge Base.

## Debug Service Portal URL redirects

Debug the URL redirects for logging in to Service Portal and redirecting to the first page.

To view debug output from SPEntryPage and see the session variables it redirects based on:

1.  Make sure the system property glide.entry.first.page.script has the value: `new SPEntryPage().getFirstPageURL()`.
2.  From the SPEntryPage script include, set `this.logVariables = true`.
3.  In a separate browser, log in.
4.  From the system navigator, view the log output by navigating to **System Logs** &gt; **System Log** &gt; **All**.

