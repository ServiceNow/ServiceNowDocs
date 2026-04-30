---
title: Non-interactive sessions
description: The Non-Interactive Sessions plugin creates a distinction between interactive and non-interactive users.Non-interactive users can only connect to a ServiceNow instance from an API protocol. Use this feature to set up user accounts for web service authentication purposes.Manually switch a non-interactive user to an interactive user.If your instance requires strict security, add the soap role to any user accounts used for web services.You can specify whether non-interactive sessions require authentication from the High Security Settings module.
locale: en-US
release: yokohama
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Monitoring user activity, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Non-interactive sessions

The Non-Interactive Sessions plugin creates a distinction between interactive and non-interactive users.

-   **Interactive users**

    New users added to the instance automatically become interactive users. Interactive users can perform the following actions:

    -   Use their user name and password to log in to the UI or a service portal.
    -   Connect to an instance from a URL that calls a UI page, form, or list, for example, https://&lt;instance name&gt;.service-now.com/incident.do.
    -   Connect with single sign-on, for example, digest authentication or a Security assertion markup language \(SAML\).
    -   Use their credentials to authorize SOAP connections if allowed by strict security.
    -   Use their credentials for other API connections such as WSDL, JSON, XML, or XSD without restriction.
-   **Non-interactive users**

    Non-interactive users can only use their credentials to authorize API connections such as JSON, SOAP, and WSDL. They can’t log in to the ServiceNow UI. The strict security high security setting determines if non-interactive users are subject to [Contextual Security Manager](https://www.servicenow.com/docs/access?context=r_ContextualSecurity&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) requirements.


Distinguishing between interactive and non-interactive users increases instance security by helping to ensure that users abide by the principle of least privilege.

## Installed with Non-Interactive Sessions

**Note:** Non-Interactive Sessions is enabled for all new instances since the Calgary release. If you don’t see it in the list of plugins, request it using the Activate Plugin service catalog item in Now Support.

-   Adds a column titled **Web Service Access Only** \[web\_service\_access\_only\] to the **User** \[sys\_user\] table.
-   Changes all existing users to be interactive users \(web\_service\_access\_only=false\).
-   Updates the User form to display the **Web Service Access Only** \[web\_service\_access\_only\] field by default.

**Parent Topic:**[Monitoring user activity](../../roles/concept/user-admin-tools-landing.md)

## Create a non-interactive user for web services

Non-interactive users can only connect to a ServiceNow instance from an API protocol. Use this feature to set up user accounts for web service authentication purposes.

### Before you begin

Role required: user\_admin or admin

### About this task

Non-interactive users can't log in to an instance or a service portal or connect through single-sign-on. They can be used as a MID Server user if they’re flagged as an Internal Integration User.

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Search for the user to be updated.

    For example, SOAP user.

3.  Select the **Web Service Access Only** check box.

4.  Select **Update**.

    **Note:**

    -   The Web service access only check box is automatically enabled when you select **Machine** in the Identity type field. The Web service access only check box is automatically disabled when you select **Human** or **AI Agent**.
    -   The ServiceNow platform uses any user name and password credentials supplied with a request even if the [High Security Settings](https://www.servicenow.com/docs/access?context=c_HighSecuritySettings&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) don’t require authorization for a given API protocol. For example, if a SOAP request supplies a user name and password, the instance verifies those credentials even if SOAP requests don’t require authorization. To avoid verifying user credentials, the request must not include them.

## Make a non-interactive user record interactive

Manually switch a non-interactive user to an interactive user.

### Before you begin

Role required: user\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Search for the user you want to update.

    For example, **System Administrator**.

3.  Clear the **Web Service Access Only** check box.

4.  Select **Update**.


## Update web service user accounts for strict security

If your instance requires strict security, add the soap role to any user accounts used for web services.

### Before you begin

Role required: user\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select a web service user from the list.

3.  From the **Roles** related list, select **Edit**.

4.  Add soap to the **Roles List**.

5.  Select **Save**.

6.  Select **Update**.


## Require authentication

You can specify whether non-interactive sessions require authentication from the **High Security Settings** module.

### Before you begin

Role required: admin with elevated privileges

### About this task

A non-interactive session bypasses the UI to connect to the instance at an API level. Typically, non-interactive sessions use set protocols such as JSON, SOAP, XSD, or WSDL. By default, all non-interactive sessions require authentication.

### Procedure

1.  Log in with an administrator user with the security\_admin role.

2.  Elevate your privileges to use security\_admin.

3.  Navigate to **All** &gt; **System Security** &gt; **High Security Settings**.

4.  Select the matching **Requires authorization...** option for the protocol you want to set.

    For example, **Requires authorization for incoming SOAP requests**.

5.  Select the check box to require authentication for the non-interactive session method.

    Clear the check box to enable the non-interactive session method to connect without providing any credentials.

    **Note:**

    Activating the Non-Interactive Sessions plugin might restrict existing users who manage SOAP and WSDL-based integrations from logging in, unless they already possess the SOAP role.


