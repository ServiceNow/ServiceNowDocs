---
title: Form widget
description: The form widget is a platform form within the Service Portal UI with a few differences. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Form widget

The form widget is a platform form within the Service Portal UI with a few differences. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

![Form widget in the shape of the portal form](../image/WidgetForm.png "Form widget")

## URL Parameters

The form widget accepts the following parameters within the URL. Add these parameters to the page URL to display a specified record with the form widget.

<table id="table_nb5_zr4_ndb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sys\_id** or **sl\_sys\_id**

</td><td>

Sys\_id for the record to be displayed.

</td></tr><tr><td>

**table**, **sl\_table**, or **t**

</td><td>

Table for the record to be displayed.The form widget validates access to the table by checking for the necessary cross-scope privileges when fetching data from the table. To turn off validating cross-scope privileges, you can set the **glide.service\_portal.enforce\_cross\_scope\_check\_in\_form** system property to false. For more information, see [Service Portal properties](properties-service-portal.md).

</td></tr><tr><td>

**view** or **v**

</td><td>

View used to display the record.

</td></tr></tbody>
</table>In the following example, the URL would display an incident with a sys\_id of 1c741bd70b2322007518478d83673af3 in the portal view:

`https://example.service-now.com/sp?id=form&table=incident&sys_id=1c741bd70b2322007518478d83673af3&view=portal`

**Note:** Timer fields, such as Time Worked, don’t display correctly in Service Portal. For more information and a workaround, see the [Timer fields do not display the correct data in Service Portal \[KB0752404\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0752404) article in the Now Support Knowledge Base.

## Scripting

Not all client scripts are supported in the Service Portal. To understand how client scripts interact with forms in the Service Portal, see [Service Portal and client scripts](unsupported_client_scripts.md) and [Supported client script types and APIs](../reference/client-script-reference.md).

**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

