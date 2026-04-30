---
title: Enable connecting to meetings from Microsoft Teams
description: Create the OIDC provider configuration record that enables users to connect to meetings in the Microsoft Teams application.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Enable connecting to meetings from Microsoft Teams

Create the OIDC provider configuration record that enables users to connect to meetings in the Microsoft Teams application.

## Before you begin

Role required: admin

Ensure that you install the Azure apps in your environment.

## About this task

This step is only required if the upn is different from the email ID.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select the OIDC record in the format **Azure AD – sso -**&lt;tenantname&gt; where &lt;tenantname&gt; is the name of your tenant.

3.  Review the **OAuth OIDC Provider Configuration** entry.

    **Note:** This field is applicable for records of the type **External OIDC Provider**.

    ![Preview OIDC provider configuration](../images/preview-oauth-oidc.png)

4.  Select **Open Record**.

5.  In the **User Claim** field, enter `email`.

6.  Select **Update**.


**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_tnt.md)

