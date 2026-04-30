---
title: Set up the Microsoft Entra ID integration for new hire onboarding
description: To set up the Microsoft Entra ID integration for new hire onboarding, you must first set up the Microsoft Entra ID spoke, next configure the remote directory sync to fetch the groups into your instance, and last configure the required business roles.
locale: en-US
release: yokohama
product: Employee Journey Management
classification: employee-journey-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Microsoft Entra ID integration for new hire onboarding, Lifecyle events for enterprise integrations, Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Set up the Microsoft Entra ID integration for new hire onboarding

To set up the Microsoft Entra ID integration for new hire onboarding, you must first set up the Microsoft Entra ID spoke, next configure the remote directory sync to fetch the groups into your instance, and last configure the required business roles.

## Before you begin

This integration requires subscriptions to the following:

-   [Microsoft Azure AD spoke](https://www.servicenow.com/docs/access?context=microsoft-azure-ad-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
-   Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin

    **Note:** The Lifecycle Events for new hire onboarding is included as demo data with this plugin.


Role required: admin

## Procedure

1.  Set up the Microsoft Entra ID spoke.

    For instructions on how to set up the spoke, see [Set up Microsoft Azure AD spoke](https://www.servicenow.com/docs/access?context=set-up-azure&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

2.  Configure the remote directory sync to fetch the groups into your instance.

    **Note:** The Remote Directory Sync \[com.snc.remote\_directory\_sync\] plugin is automatically activated with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin. This plugin retrieves data from a remote directory on external systems like Microsoft Azure AD or Okta, and stores a copy of the data locally. This plugin stores data about individual users and groups, and the relationship between them.

    1.  Navigate to **Directory Sync** &gt; **Integrations**.

        The Directory Integrations table appears.

    2.  Select **New**.

    3.  Fill in the fields on the form.

        |Field|Description|
        |-----|-----------|
        |Display name|Display name for the integration.|
        |Connection &amp; Credential|Set the value to `sn_azure_ad_spoke.AzureAD`.|
        |Directory provider|Set the value to `Microsoft Azure AD`.|

    4.  Right-click the form header and select **Submit**.

    5.  Select **Publish** to publish the record.

    Publication triggers the fetching of groups into your instance so that you can assign them to different users. Groups are fetched on a scheduled basis. You can view the fetched groups by navigating to **Directory Sync** &gt; **Groups**.

3.  Configure the required business roles.

    **Note:** The Business Roles \[com.snc.businessroles\] plugin is automatically activated with the Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin.

    For instructions on how to configure the business roles and map them to the relevant groups, see [Configure a business role](configure-business-role.md).


**Parent Topic:**[Microsoft Entra ID integration for new hire onboarding](../concept/azure-active-directory-integration-for-new-hire-onboarding.md)

