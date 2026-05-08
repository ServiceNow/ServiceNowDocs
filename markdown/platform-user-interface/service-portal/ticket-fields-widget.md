---
title: Ticket Fields widget
description: The Ticket Fields widget displays information about a request that a user has made. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Ticket Fields widget

The Ticket Fields widget displays information about a request that a user has made. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

## Using the widget

After a user submits a request, they can track their request on a ticket page in Service Portal. The user can consult the Ticket Fields widget to review the details of their request and check its resolution status.

![Ticket Fields widget](../image/ticket-fields-widget.png)

Fields for the Ticket Fields widget are defined by the HTML template and the server.

If a user entered variables when submitting the request, they can view those variables in the Options section.

![Options section of the Ticket Fields widget](../image/ticket-fields-options.png)

**Note:** The values that appear in the Options section are not field values from the ticket. They are Service Catalog variables that are associated with the ticket. For more information, see [Service catalog variables](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Instance options

Use the instance options to configure the Ticket Fields widget for a portal page.

<table id="table_jr1_5zy_jkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pickup message

</td><td>

Text to communicate the expected resolution time of the ticket. This text is displayed below the ticket fields.

 The default is `${Tickets are picked up within <br/> 4 hours (M-F 9-5)}`. Ensure that any changes you make are within the curly braces.

</td></tr></tbody>
</table>**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

