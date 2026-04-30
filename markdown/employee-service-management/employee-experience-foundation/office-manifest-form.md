---
title: Office Manifest form
description: The Office Manifest form helps you configure a manifest file for the ServiceNow Add-in for Microsoft 365.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow Add-in for Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Office Manifest form

The Office Manifest form helps you configure a manifest file for the ServiceNow Add-in for Microsoft 365.

<table id="table_yqv_5kk_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add-In Name

</td><td>

Name of the add-in that you want to create the manifest for.

</td></tr><tr><td>

Description

</td><td>

Description of the add-in that you want to create.

</td></tr><tr><td>

Plugin ID

</td><td>

Auto-generated identifier for the add-in.

</td></tr><tr><td>

Office Application

</td><td>

Microsoft Application that you want to create the add-in for.

</td></tr><tr><td>

Active

</td><td>

Option to activate the add-in.

</td></tr><tr><td>

Permission

</td><td>

API permissions for the add-in.

</td></tr><tr><td>

Icon URL

</td><td>

HTTPS or relative URL for the add-in icon.

</td></tr><tr><td>

Version

</td><td>

Version number of the add-in file.

</td></tr><tr><td>

Login Page not Required

</td><td>

Option to disable the login page for the add-in.If you select this option, you must add a list of domains that are allowed to access the add-in.

</td></tr><tr><td>

Auto Open Add-in

</td><td>

Option to automatically open the add-in when the app is launched.This field is available only when **Word** or **PowerPoint** is selected in the **Office Application** field.

</td></tr><tr><td>

Allowed Domains

</td><td>

List of domains that are allowed to access the add-in.This field is available only when the **Login Page not Required** field is selected.

</td></tr></tbody>
</table>**Note:** You can configure single sign-on \(SSO\) for your add-in by selecting the **Login Page not Required** field and providing the SSO domain in the **Allowed Domains** field.

**Parent Topic:**[ServiceNow Add-in for Microsoft 365 reference](sn-addin-for-ms365-reference.md)

