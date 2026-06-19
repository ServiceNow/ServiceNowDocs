---
title: Configure an account recovery user
description: Configure an account recovery user to perform account recovery activities on your instance.Configure an account recovery from the Account Recovery properties page.Configure an administrator as an account recovery user from the admin user profile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/config-acr.html
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Account recovery \(ACR\), Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Configure an account recovery user

Configure an account recovery user to perform account recovery activities on your instance.

An account recovery user is a user account that administrators can use to perform account recovery tasks, such as addressing an SSO misconfiguration or addressing expired certificates.

**Note:** If you are using account recovery on your instance, you must configure an account recovery user. This step is necessary before enabling multiple-provider single sign-on on an instance.

## Configure an account recovery user from the Account Recovery Properties page

Configure an account recovery from the Account Recovery properties page.

### Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

For a fresh instance to configure ACR, you must do the following:

-   Activate Mutli-SSO plugin \(`com.snc.integration.sso.multi.installer`\)
-   Enable ACR \(`glide.sso.acr.enabled`\) - This is enabled by default in case of a fresh instance.
-   Before enabling SSO property \(`glide.authenticate.multisso.enabled`\), the administrator must enroll as an ACR user.
-   Administrator must set a password for local login and register MFA before enrolling as an ACR user.

For an upgraded instance to use ACR, you must do the following:

-   Activate Mutli-SSO plugin \(`com.snc.integration.sso.multi.installer`\)
-   Enable ACR \(`glide.sso.acr.enabled`\)

    **Note:** In case of upgraded instance, the administrator must enable ACR.

-   Before enabling SSO property \(`glide.authenticate.multisso.enabled`\), the administrator must enroll as an ACR user.

    **Note:** Setting this property to false will not disable multi-provider SSO if Account Recovery \(ACR\) is also enabled on the instance. To log in with a username and password ACR must also be disabled using the **glide.sso.acr.enabled** property. For details on this property see [Account recovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/acr-properties.md).

-   Administrator must set a password for local login and register MFA before enrolling as an ACR user.

### Procedure

1.  Navigate to **All** &gt; **Account Recovery** &gt; **Properties**.

2.  Select **Enable account recovery**.

    **Note:** You need to enable account recovery when SSO is enable. Account recovery users will be limited to SSO configuration and troubleshooting-related tasks.

3.  Select the **here** text in the Step 2.

    \[Omitted image "acct-recover-click.png"\] Alt text: Account recovery warning with a link to account recovery setup

4.  Following the on-screen directions in the **Configure account recovery for Multi-SSO** modal.

    \[Omitted image "acct-recover-setup.png"\] Alt text: Configure account recovery for Multi-SSO modal

    After completing the on-screen steps, the **Enable account recovery** is enabled.

5.  Select **Enable account recovery**.

6.  Select **Save**.


### Result

You have configured your user account as an account recovery user. You can verify this account, and see any other configured account recovery users by navigating to **Multi-Provider SSO** &gt; **Account Recovery** &gt; **Users**.

## Configure an account recovery user from an admin user profile

Configure an administrator as an account recovery user from the admin user profile.

### Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

### Procedure

1.  Log into your instance using an administrator account.

2.  Click on the user name in the instance header, and select **Profile**.

    \[Omitted image "user-profile-1.png"\] Alt text: User profile location

3.  In the **User** form, click **Enable Account Recovery** in the **Related Links** section.

    \[Omitted image "user-profile-2.png"\] Alt text: User profile location

    **Note:**

    If the selected user already has account recovery enabled, **Enable Account Recovery** does not appear in the related links. There will be a **Disable Account Recovery** option instead.

4.  Following the on-screen directions in the **Configure account recovery for Multi-SSO** modal.

    \[Omitted image "acct-recover-setup.png"\] Alt text: Configure account recovery for Multi-SSO modal

    After completing the on-screen steps, the **Enable account recovery** is enabled.

5.  Click **Enable account recovery**.


### Result

You have configured your user account as an account recovery user. You can verify this account, and see any other configured account recovery users by navigating to **Multi-Provider SSO** &gt; **Account Recovery** &gt; **Users**.

