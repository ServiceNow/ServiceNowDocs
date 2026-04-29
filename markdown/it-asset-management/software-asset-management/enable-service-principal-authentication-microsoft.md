---
title: Enable service principal authentication for Power BI read-only APIs
description: Grant your application access to Power BI service content and APIs by enabling service principal authentication for Power BI read-only APIs. Power BI service content and APIs help optimize your Microsoft 365 subscriptions, such as by downgrading subscriptions from Office 365 E5 to Office 365 E3.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Enable service principal authentication for Power BI read-only APIs

Grant your application access to Power BI service content and APIs by enabling service principal authentication for Power BI read-only APIs. Power BI service content and APIs help optimize your Microsoft 365 subscriptions, such as by downgrading subscriptions from Office 365 E5 to Office 365 E3.

## Before you begin

Microsoft Entra ID Role required: global administrator

Power BI Role required: Power platform administrator

**Note:** This configuration enables the ServiceNow Software Asset Management application to get the usage information \(Last usage time\) for all Power BI Pro deployments across the Web and Desktop. The Software Asset Management application pulls the last activity date for Power BI deployments that are part of Microsoft 365 subscriptions.

## About this task

Service principal is an authentication method that enables your application to access secure Microsoft Entra ID resources, such as Power BI service content and APIs.

## Procedure

1.  Create a security group for service principal authentication.

    Security groups enable you to manage which users, devices, groups, and service principals can access shared resources. If you want to use an existing security group for service principal authentication, skip to [step 2](enable-service-principal-authentication-microsoft.md#add-app-security-group).

    1.  On the page header of the Microsoft Azure portal, use the search bar to search for and select the **Microsoft Entra ID** service.

        The Overview page for the Microsoft Entra ID service opens.

    2.  From the side navigation menu of the Microsoft Entra ID service, navigate to **Manage** &gt; **Groups**.

        The **Groups** &gt; **All groups** page opens.

    3.  On the All groups page, select **New group**.

    4.  On the form, fill in the fields.

<table id="table_rj1_j5y_pqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group type

</td><td>

Group type.Set this field to **Security**.

</td></tr><tr><td>

Group name

</td><td>

Name of the group.

</td></tr><tr><td>

Group email address

</td><td>

Email address that is shared between all group members.

</td></tr><tr><td>

Group description

</td><td>

Description of the group.

</td></tr><tr><td>

Membership type

</td><td>

Method in which members can be added to or removed from the group.Set this field to **Assigned**.

</td></tr></tbody>
</table>    5.  Select **Create**.

    The security group is created and then you’re redirected to the Overview page for the new group.

2.  Add the application that you created in [Register a Microsoft Entra ID application](register-microsoft-app.md) as a member of your security group.

    1.  If you didn’t create a security group in [step 1](enable-service-principal-authentication-microsoft.md#create-security-group) and are using an existing security group instead, open your existing security group.

        If you created a security group in [step 1](enable-service-principal-authentication-microsoft.md#create-security-group), skip to [step b](enable-service-principal-authentication-microsoft.md#step-b).

        1.  On the page header of the Microsoft Azure portal, use the search bar to search for and select the **Microsoft Entra ID** service.

            The Overview page for the Microsoft Entra ID service opens.

        2.  From the side navigation menu of the Microsoft Entra ID service, navigate to **Manage** &gt; **Groups**.

            The **Groups** &gt; **All groups** page opens.

        3.  From the list of available groups, locate and select your existing security group.

            The Overview page for the security group opens.

    2.  From the side navigation menu of your security group, navigate to **Manage** &gt; **Members**.

        The Members page opens.

    3.  On the Members page, select **Add members**.

        The Add members dialog box opens.

    4.  In the dialog box, search for and select the application that you created in [Register a Microsoft Entra ID application](register-microsoft-app.md).

        **Important:** The application must not have any Power BI admin permissions set from the Microsoft Azure portal. You can verify your application permissions using the following steps:

        1.  Log in to the Microsoft Azure portal using either your global administrator, application administrator, or cloud application administrator credentials.
        2.  On the page header of the Microsoft Azure portal, use the search bar to search for and select the **Microsoft Entra ID** service.

            The Overview page for the Microsoft Entra ID service opens.

        3.  From the side navigation menu of the Microsoft Entra ID service, navigate to **Manage** &gt; **Enterprise applications**.

            The Enterprise applications page opens.

        4.  From the list of available enterprise applications, locate and select your application.
        5.  Select **Permissions**.
        6.  Verify that no Power BI admin-consent-required permissions are set on the application.
    5.  Select **Select**.

        The application is added as a member of your security group.

3.  Enable your security group to access read-only Power BI admin APIs.

    1.  In a new tab or web browser, open [Power BI](https://app.powerbi.com/).

    2.  Log in using either your global administrator or Power BI administrator credentials.

        The Power BI portal opens.

    3.  On the page header of the Power BI portal, select the Settings icon ![Personalize list icon.](../image/gear-icon.png) and then select **Admin portal**.

        The Power BI Admin portal opens.

    4.  From the side navigation menu of the Admin portal, select **Tenant settings**.

    5.  In the Admin API settings section, expand the **Allow service principals to use read-only Power BI admin APIs** setting.

    6.  Select the toggle button to enable the setting.

    7.  When prompted, select the option to apply the setting to **Specific security groups**.

    8.  In the corresponding text box, enter the name of your security group.

    9.  Select **Apply**.

    After you enable this setting through the Power BI Admin portal, any application permissions that you set from the Microsoft Azure portal are no longer effective. All application permissions must subsequently be set and managed through the Power BI Admin portal.


