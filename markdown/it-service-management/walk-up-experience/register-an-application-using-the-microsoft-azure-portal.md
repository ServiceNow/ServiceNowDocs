---
title: Register an application using the Microsoft Azure portal
description: Grant authorization to the ServiceNow instance by registering an application with Azure AD.
locale: en-US
release: yokohama
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Microsoft Office 365 integration for Walk-up Experience, Integrate Microsoft Office 365 calendar with Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Register an application using the Microsoft Azure portal

Grant authorization to the ServiceNow instance by registering an application with Azure AD.

## Before you begin

Role required: Azure Active Directory admin

## About this task

Complete these steps from the Microsoft Azure portal. For instructions on registering an application, see the [Microsoft Azure documentation](https://docs.microsoft.com/en-gb/).

## Procedure

1.  In the Microsoft Azure portal, add the **Redirect URIs** in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`

2.  For the **Required Permissions**, select **Microsoft Graph**.

    ![Microsoft graph permissions](../image/ms-exchange-online-spoke-permissions.png)

3.  Record the **Client Secret** for use in later configurations.


## Result

The ServiceNow application is created with Microsoft Azure AD.

**Parent Topic:**[Set up Microsoft Office 365 integration for Walk-up Experience](setup-walkup-msoffice365-cal-integ.md)

