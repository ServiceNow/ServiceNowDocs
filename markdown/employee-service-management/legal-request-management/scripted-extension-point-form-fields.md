---
title: Scripted Extension Point form fields
description: List of fields in the Scripted Extension Point.
locale: en-US
release: xanadu
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create implementation in Scripted Extension Point, Configure an external storage system for legal requests and legal matters, Setting up Legal Request Management, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Scripted Extension Point form fields

List of fields in the Scripted Extension Point.

<table id="table_aqz_g35_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the extension point. The name can be up to 100 alphanumeric characters, including special characters.

</td></tr><tr><td>

API Name

</td><td>

Name of the extension point API that is pre-pended with the application scope to which it applies. This is a system-assigned name and can’t be changed.

</td></tr><tr><td>

Application

</td><td>

Application to which the extension point is assigned. This is system-assigned and can’t be changed.

</td></tr><tr><td>

Accessible from

</td><td>

Application scope that defines the applications that can access this scripted extension point. The available values are:-   All application scopes — Can be accessed from any application scope.
-   This application scope — Can be accessed from the current application scope.

</td></tr><tr><td>

Active

</td><td>

Option to enable the scripted extension point.

</td></tr><tr><td>

Description

</td><td>

Descriptive content regarding the scripted extension point.

</td></tr><tr><td>

Script

</td><td>

The server-side script to run when called from other scripts. The script must define a single JavaScript class or a global function. The class or function name must match the **Name** field.

</td></tr><tr><td>

Client callable

</td><td>

Options to make the scripted extension point available to client scripts, list/report filters, reference qualifiers, or, if specified, as part of the URL.

</td></tr></tbody>
</table>**Parent Topic:**[Create implementation in Scripted Extension Point](../task/create-scripted-extension-point.md)

