---
title: Portal Object widget instance options form
description: Instance options enable you to configure the Portal Object widget on a portal page.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configurable Portal widgets instance options, Configurable Portal Widgets reference, Reference, Customer Service Management]
---

# Portal Object widget instance options form

Instance options enable you to configure the Portal Object widget on a portal page.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table from which the fields of the selected record are shown as cards on the widget. The default table is the Asset \[alm\_asset\] table.

</td></tr><tr><td>

Record

</td><td>

The system identifier \(sys\_id\) of the record from the specified table.The default sys\_id is 00a96c0d3790200044e0bfc8bcbe5dc3.

**Note:** Note:

-   Displays details of the record identified by the sys\_id in the URL. If no sys\_id is found in the URL, displays details of the record identified by the sys\_id in the instance option.
-   If the sys\_id is provided in both the portal web page URL and the **Record** field, the widget displays information based on the portal web page URL.
-   The sys\_id of a record should be taken from the table specified in the **Table** field.

</td></tr></tbody>
</table><table id="table_hpn_kb1_fzb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Card title

</td><td>

Fields of the selected record from the specified table to be displayed as the card title in the widget.**Note:** You can select up to three fields from the defined table. They’ll be combined to form a title for each record displayed on the widget. For example, if you combine the Asset tag, Model category, and Display name fields of a record from the specified table, the card title would be "P1000479 Computer Apple MacBook Pro 15."

</td></tr><tr><td>

Image field

</td><td>

The name of the field of the selected record that contains an image to be displayed as an image on the card.

</td></tr><tr><td>

Image style

</td><td>

The display style for an image inside the widget. The available choices are: -   Thumbnail
-   Avatar

 The default display style is Thumbnail.

</td></tr><tr><td>

Summary view fields \(Desktop\)

</td><td>

Fields from the specified table whose name and value are displayed as field value pairs on the card in the desktop view.

</td></tr><tr><td>

Summary view fields \(Mobile\)

</td><td>

Fields from the specified table whose name and value are displayed as field value pairs on the card in the mobile view.

</td></tr><tr><td>

Details view

</td><td>

Field value pairs and sections from the specified table to be displayed when the **View all** option is selected on the card.

</td></tr><tr><td>

Actions

</td><td>

The actions to appear on the card, which are chosen from a set of predefined actions. The title field from the specified table is used as the display name of the actions.**Note:**

-   If you select multiple actions, the button label displays **Actions**.
-   If one action is selected, the actions button displays the name of that action.
-   If no action is selected, the actions button isn’t displayed on the card.

</td></tr><tr><td>

Enable Service Definitions

</td><td>

Option to display the service definitions associated with the record under **Actions**. For details, see [Service definitions](../concept/csm-service-definitions.md).

</td></tr><tr><td>

Enable Editing Record

</td><td>

When enabled, users with edit permissions see **Edit details** button as one of the Actions. On selecting it users are navigated to a form page with the default view to edit the record details.

</td></tr></tbody>
</table>**Related topics**  


[Add and configure the Portal Object widget](../task/add-conf-port-object-widget.md)

