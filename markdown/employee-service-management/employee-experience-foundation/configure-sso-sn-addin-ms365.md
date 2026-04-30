---
title: Configure single sign-on for ServiceNow Add-in for Microsoft 365
description: Configure single sign-on \(SSO\) for your add-in so users don't have to sign-in to Employee Center.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Add-in for Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure single sign-on for ServiceNow Add-in for Microsoft 365

Configure single sign-on \(SSO\) for your add-in so users don't have to sign-in to Employee Center.

## Before you begin

Role required: sn\_outlook\_addin.outlook\_addin\_setup, sn\_hr\_sp.admin, sn\_hr\_sp.esc\_admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In Manifests**.

2.  From the Office Manifests list, select the manifest that you want to configure.

3.  On the Office Manifest form, select **Login Page not Required**.

4.  In the **Allowed Domains** field, enter the SSO domain for your add-in.

    ![Office Manifest form with the Login Page not Required field selected and an SSO domain URL added to the Allowed Domains field.](../images/sn-addin-ms365-sso.png)


**Parent Topic:**[Configuring ServiceNow Add-in for Microsoft 365](../concept/configuring-sn-addin-for-ms365.md)

