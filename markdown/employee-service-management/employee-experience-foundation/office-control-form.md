---
title: Office Control form
description: The Office Control form helps you create a button, menu, or menu item for the ServiceNow Add-in for Microsoft 365.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow Add-in for Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Office Control form

The Office Control form helps you create a button, menu, or menu item for the ServiceNow Add-in for Microsoft 365.

<table id="table_ijn_b4k_pcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label of the office control that is displayed on the add-in.

</td></tr><tr><td>

Description

</td><td>

Description of the office control displayed on the add-in.

</td></tr><tr><td>

Type

</td><td>

Type of office control that you want to create.

</td></tr><tr><td>

Action

</td><td>

Action taken when the office control is selected.This field is available only when **Button** or **MenuItem** is selected in the **Type** field.

</td></tr><tr><td>

Relative URL

</td><td>

Relative URL that opens when the user selects the office control.This field is available only when **Open URL** is selected in the **Action** field.

</td></tr><tr><td>

Catalog

</td><td>

Catalog that opens when the user selects the office control.This field is available only when **Open Catalog** is selected in the **Action** field.

</td></tr><tr><td>

Table

</td><td>

Table for the new record that is created when the user submits a form.This field is available only when **Open Form** is selected in the **Action** field.

</td></tr><tr><td>

Parent Control

</td><td>

Parent menu that you want to add the item to.This field is available only when **MenuItem** is selected in the **Type** field.

</td></tr><tr><td>

Manifest

</td><td>

Manifest record that the office control is linked to.

</td></tr><tr><td>

Active

</td><td>

Option to activate the record.

</td></tr><tr><td>

Extension Point Type

</td><td>

Extension point for the office control.This field is available only when **Button** or **Menu** is selected in the **Type** field.

**Note:** Menu items will have the same extension point as the parent menu record.

This field has the following options:

-   MessageReadCommandSurface: Adds a button in the mail read view
-   MessageComposeCommandSurface: Adds a button in the mail compose form
-   AppointmentOrganizerCommandSurface: Adds a button on the ribbon for the meeting organizer
-   AppointmentAttendeeCommandSurface: Adds a button on the ribbon for the meeting attendee
-   PrimaryCommandSurface: Adds a tab to the ribbon in the Office app. This option is available only when the manifest is created for Microsoft Word or Microsoft PowerPoint

For more information about extension points, see [ExtensionPoint element](https://learn.microsoft.com/en-us/javascript/api/manifest/extensionpoint?view=common-js-preview) in the Microsoft documentation.

</td></tr><tr><td>

Icons

</td><td>

Section that requires HTTPS or relative URLs for the office control icons.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Add-in for Microsoft 365 reference](sn-addin-for-ms365-reference.md)

