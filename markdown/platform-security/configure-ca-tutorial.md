---
title: Tutorial: Configure Continuous Authentication for a Data Class
description: Procedure that describes end to end configuration of continuous authentication policy for a data class and the impacts to the users due to the configuration changes.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring CA, Continuous Authentication \(CA\), Zero Trust Access, Access Management]
---

# Tutorial: Configure Continuous Authentication for a Data Class

Procedure that describes end to end configuration of continuous authentication policy for a data class and the impacts to the users due to the configuration changes.

## Before you begin

-   Role required: ca\_admin

    **Note:** You must elevate your role to **ca\_admin**.

-   You must install the **Zero Trust - Continuous Authentication** \(`com.snc.zero_trust_continuous_authentication`\) for opting CA which requires a license.
-   Enable the Continuous Authentication \(**glide.zta.continuous\_authentication.enabled**\) system property. For more information, see [System properties](../concept/ca-system-properties.md).
-   Activate the Integration - Multiple Provider Single Sign-On Installer \(**com.snc.integration.sso.multi.installer**\) plugin.
-   Understand the pre-work that is required before configuring CA for the instance. For more information, see [Pre-work for Continuous Authentication](../concept/pre-work-ca.md).

## Procedure

1.  Navigate to **All** &gt; **Continuous Authentication**.

2.  Select **Policies** tab.

3.  Select **New**.

4.  On the form, fill the fields:

<table id="table_cvy_xnw_ycc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy Name

</td><td>

Name of the policy

</td></tr><tr><td>

Description

</td><td>

Generic description to the policy

</td></tr><tr><td>

Select the resources

</td><td>

Select the **Data Class**. You can create data class and use it for CA policy configuration.**Note:** To know more about how to create data class, see [Data Classification](../../../administer/security/concept/data-classification.md).

</td></tr></tbody>
</table>    ![CA Policy for a Data Class](../images/ca-policy-dataclass.png)

    **Note:** You can use either of the login methods for the CA policy:

    -   **SSO based login**: Specify the fields in the **Continuous Authentication** tab within the Identity Provider record and the set the Identity Provider record as **Active**. ![Continuous Authentication - tab information](../images/ca-tab.png)

        To know more about Identity Providers configuration, see [OIDC](../../single-sign-on/task/create-OIDC-configuration-SSO.md) and [SAML](../../single-sign-on/task/t_CreateASAML2Upd1SSOConfigMultiSSO.md).

    -   **Non-SSO based login**: By default, if there are no Identity Provider with Continuous Authentication configuration, Multi-factor Authentication \(MFA\) is used as a login method. Make sure the MFA properties are Active and configured based on your requirement. To know more about MFA properties, see [Multi-factor Authentication system properties](../reference/mfa-properties.md).
5.  Select **Save &amp; Activate**.


## Result

Based on the details provided for the configuration, CA policy is created with Access Control List \(ACLs\) for the selected table or data class. You can view the details of the ACLs that are created by selecting the **View ACLs** on the policy page.

![ACL Details for Data Class CA policy](../images/ca-acl-details-dataclass.png)

The CA policy created, prompts the user for authentication to data class \(in this case data class set for the table **Account Recovery**\) that you've protected using the policy. The users can select **Authenticate** option.

![CA Policy enforced for data class](../images/ca-policy-data-class.png)

Perform the authentication based on the following:

-   User who had performed local login to log in to the instance, is displayed with platform MFA for step-up authentication.

    ![MFA-SMS](../images/mobile-screen-mfa.png)

-   User who had performed SSO login \(OIDC or SAML\) to log in to the instance is displayed with the SSO for re-authentication.

    ![SSO - Screen](../images/ca-sso-screen.png)


After successful authentication the table with the data class is displayed.

![ACR table after successful login](../images/ca-acr-table-after-login.png)

An high assurance session is now established for the user. High assurance session is limited to the High Assurance session length \(**glide.zta.high\_assurance.session.timeout**\) system property. If the high assurance session time exceeds the property length, the user is prompted for re-authentication or step up authentication.

**Related topics**  


[Configuring Continuous Authentication](configure-ca.md)

[High Assurance session with Continuous Authentication](../concept/high-assurance-ca.md)

[Exploring Continuous Authentication](../concept/explore-continuous-auth.md)

