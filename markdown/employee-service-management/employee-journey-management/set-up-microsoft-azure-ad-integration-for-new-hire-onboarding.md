---
title: Set up the Microsoft Entra ID integration for new hire onboarding
description: To set up the Microsoft Entra ID integration for new hire onboarding, you must first set up the Microsoft Entra ID spoke, next configure the remote directory sync to fetch the groups into your instance, and last configure the required business roles.
locale: en-US
release: australia
product: Employee Journey Management
classification: employee-journey-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Entra ID integration for new hire onboarding, Lifecyle events for enterprise integrations, Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Set up the Microsoft Entra ID integration for new hire onboarding

To set up the Microsoft Entra ID integration for new hire onboarding, you must first set up the Microsoft Entra ID spoke, next configure the remote directory sync to fetch the groups into your instance, and last configure the required business roles.

## Before you begin

This integration requires subscriptions to the following:

-   [Microsoft Azure AD spoke](https://www.servicenow.com/docs/access?context=microsoft-azure-ad-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin

    **Note:** The lifecycle event for new hire onboarding is included as demo data with this plugin.


Role required: admin

## Procedure

1.  Set up the Microsoft Entra ID spoke.

    For instructions on how to set up the spoke, see [Set up Microsoft Azure AD spoke](https://www.servicenow.com/docs/access?context=set-up-azure&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

2.  Configure the remote directory sync to fetch the groups into your instance.

    **Note:** The Remote Directory Sync \[com.snc.remote\_directory\_sync\] plugin is automatically activated with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

    1.  Navigate to **Directory Sync** &gt; **Integrations**.

    2.  Click **New**.

    3.  Fill in the fields on the form.

        |Field|Description|
        |-----|-----------|
        |Display name|Display name for the integration.|
        |Connection &amp; Credential|Set the value to `sn_azure_ad_spoke.AzureAD`.|
        |Directory provider|Set the value to `Microsoft Azure AD`.|

    4.  Right-click the form header and click **Submit**.

    5.  Click **Publish** to publish the record.

    Publication triggers the fetching of groups into your instance so that you can assign them to different users. Groups are fetched on a scheduled basis. You can view the fetched groups by navigating to **Directory Sync** &gt; **Groups**.

3.  Configure the required business roles.

    **Note:** The Business Roles \[com.snc.businessroles\] plugin is automatically activated with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

    For instructions on how to configure the business roles and map them to the relevant groups, see [Configure a business role](configure-business-role.md).


**Parent Topic:**[Microsoft Entra ID integration for new hire onboarding](../concept/azure-active-directory-integration-for-new-hire-onboarding.md)

