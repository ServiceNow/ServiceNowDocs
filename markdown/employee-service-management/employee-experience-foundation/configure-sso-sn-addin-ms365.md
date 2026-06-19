---
title: Configure single sign-on for ServiceNow Add-in for Microsoft 365
description: Configure single sign-on \(SSO\) for your add-in so users don't have to sign-in to Employee Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/configure-sso-sn-addin-ms365.html
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

    \[Omitted image "sn-addin-ms365-sso.png"\] Alt text: Office Manifest form with the Login Page not Required field selected and an SSO domain URL added to the Allowed Domains field.


**Parent Topic:**[Configuring ServiceNow Add-in for Microsoft 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/configuring-sn-addin-for-ms365.md)

