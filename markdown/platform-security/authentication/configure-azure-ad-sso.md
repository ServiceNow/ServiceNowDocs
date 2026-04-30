---
title: Configure Azure AD SSO
description: Configure Azure AD SSO in the Azure portal.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Azure AD Integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Configure Azure AD SSO

Configure Azure AD SSO in the Azure portal.

## Before you begin

Role required: Azure admin

## Procedure

1.  In the Azure portal, on the ServiceNow application integration page, find the Manage section.

2.  Select single sign-on.

    On the Select a single sign-on method page, select SAML.

3.  On the Set up single sign-on with SAML page, select the pen icon for Basic SAML Configuration to edit the settings.

    ![SAML Configuration.](../image/configure-azure-ad-sso.png)

4.  In the Basic SAML Configuration section, perform the following:

    1.  In **Sign on URL**, enter one of the following URL patterns:

        ```
        https://<instancename>.service-now.com/navpage.do
        https://<instance-name>.service-now.com/login_with_sso.do?glide_sso_id=<sys_id of the sso configuration>
        ```

        **Note:** You need to provide the sys\_id within this URL.

    2.  In Identifier \(Entity ID\), enter a URL with the pattern: `https://<instance-name>.service-now.com`.

    3.  For **Reply URL**, enter one of the following URL patterns:

        ```
        https://<instancename>.service-now.com/navpage.do
        https://<instancename>.service-now.com/customer.do
        ```

    4.  In Logout URL, enter a URL with the pattern: `https://<instancename>.service-now.com/navpage.do`

        **Note:** You must update the actual sign-on URL, Reply URL, Logout URL and identifier. the values shown in these URLs are for demo purpose.

5.  On the Set up single sign-on with SAML page, in the SAML Signing Certificate section, find **Certificate \(Base64\)**.

    ![Signing Certificate.](../image/certificate-sso.png)

    1.  Select the copy button to copy **App Federation Metadata Url**, and paste it into Notepad.

        This URL is required for further configuration.

    2.  Select **Download** to download Certificate\(Base64\).

6.  In the Set up ServiceNow section, copy the appropriate URLs, based on your requirement.

    ![Setup SAML.](../image/set-up-saml.png)


