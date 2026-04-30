---
title: Configure HTTP response headers
description: Configure standard name-value pairs for HTTP response headers. You designate if the configuration applies to all pages, or to specific types \(Service Portal, UI Page, or UX application record\).The HTTP response header table \(sys\_response\_header\) in the List view contains two additional columns - Add by and Order.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [HTTP Response Headers, Extend ServiceNow AI Platform capabilities]
---

# Configure HTTP response headers

Configure standard name-value pairs for HTTP response headers. You designate if the configuration applies to all pages, or to specific types \(Service Portal, UI Page, or UX application record\).

## Before you begin

Role required: An elevated access security\_admin role is required to configure an **All Pages** type header. An admin role is required to configure a **Specific Type** header.

## Procedure

1.  In the Navigator pane, type `sys_response_header.list`.

2.  Click **New**.

3.  Fill in the fields on the form.

<table id="table_osc_lwk_snb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Check box that designates that this HTTP response header configuration is active.

</td></tr><tr><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

Applies to

</td><td>

Type of record the HTTP response header configuration applies to.-   **Specific Type**

HTTP response header configuration is for the specific type and record you select in the **Type** and **Record** fields.

-   **All Pages**

HTTP response header configuration is for all pages and record types.

**Note:** Only users with an elevated access privilege security\_admin role can configure HTTP response headers for the All Pages type header.

</td></tr><tr><td>

Type

</td><td>

Type of record the HTTP response header configuration applies to. -   **Service Portal \[sp\_portal\]**

Records related to the Service Portal.

-   **UI Page \[sys\_ui\_page\]**

Standard UI pages in the ServiceNow AI Platform.

-   **UX Application \[sys\_ux\_page\_registry\]**

Standard UX applications in the ServiceNow AI Platform.

</td></tr><tr><td>

Record

</td><td>

Specific record the HTTP response header configuration applies to. To select a record:1.  Click the Search \(![Search icon](../../../common/image/List_SearchIcon.png)\) icon to access the Select the document form.
2.  In the **Table name** field, the default is the type you selected in the **Type** field. Do not change it.
3.  In the **Document** field, select the record from the table.

For example, if you selected **Service Portal \[sp\_portal\]**, you select a specific Service Portal-related record in that table.

4.  Click **OK**.
 You can only access this field if you selected **Specific Type** in the **Applies to** field.

</td></tr><tr><td>

Name

</td><td>

Name you want to assign to the name-value pair for the HTTP response header.

</td></tr><tr><td>

Value

</td><td>

Value you want to assign to the name-value pair for the HTTP response header.

</td></tr><tr><td>

Description

</td><td>

Detailed description for the HTTP response header.

</td></tr></tbody>
</table>4.  Click **Submit**.


## HTTP header configuration for advanced users

The HTTP response header table \(sys\_response\_header\) in the List view contains two additional columns - **Add by** and **Order**.

<table id="table_wqj_wlf_14b"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Order

</td><td>

Adds a default integer order value to a header configuration regardless of the type of header \(**All Pages** or a **Specific page**\). -   When a specific page request takes place, both of the header types are interleaved based on the **Order**.
-   The net headers, regardless of the type, are sorted first, based on the **Order** and added to the response based on the ordered header list.

</td></tr><tr><td>

Add By

</td><td>

Contains the following values:-   **Append**

\(Default value\) This option is relevant when multiple headers with the same name are configured. In this case, they are both added to the HTTP response header.

-   **Overwrite**

This option is relevant when the same header \(a header with the same name\) is attempting to add twice in the ordered header list \(see **Order** description\). The header with the higher order and with an **Overwrite** selection in **Add By** overwrites the same header trying to be set with a lower order.


</td></tr></tbody>
</table>You may have situations where a couple of similar **All Pages** type header configurations could overwrite a **Specific Type** type header configuration. An example of a **Specific Type** configuration would be one for a specific UI page. You can remedy this situation by adjusting the **Add by** and **Order** columns, as in the following examples.

### Append example

The ServiceNow AI Platform is trying to set headers in the following order, and **Append** is the default value for each in the **Add By** column. ![Append example - sys_response_header.list](../image/headers-all-append-list-view.jpg)

In this example, the second \(Header 2\) and third \(Header 3\) response header configurations have the same name \(Content-Security-Policy\). In this case, Header 3 is appended to Header 2. If a request is made for a specific page you configured with a Header 3 response, the net HTTP response headers are both Header 2 and Header 3.

![Append example - resulting HTTP response header](../image/headers-all-append-page-response.png)

### Overwrite

The ServiceNow AI Platform is trying to set headers in the following order, and you've selected **Overwrite** in the **Add By** column for the third header. ![Overwrite example - sys_response_header.list](../image/headers-one-overwrite-list-view.jpg)

In this example, the second \(Header 2\) and third \(Header 3\) response header configurations have the same name \(Content-Security-Policy\). In this case, Header 3 overwrites Header 2. If a request is made for a specific page you configured with a Header 3 response, the net HTTP response header is only Header 3.

![Overwrite example - resulting HTTP response header](../image/headers-one-overwrite-page-response.png)

