---
title: Configure a content type
description: Users with the content\_admin role can create a content type.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Content types, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure a content type

Users with the content\_admin role can create a content type.

## Before you begin

Role required: content\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Content Types**.

2.  Click **New**.

3.  Complete the Content Type form.

<table id="table_p5m_s3k_np"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select the table whose content will be rendered in Content Management.

</td></tr><tr><td>

Content site

</td><td>

Select the site that will use this content type.

</td></tr><tr><td>

Media type

</td><td>

Enter one of the following media types to use with this content type.-   `m`: Smartphone interface only \(not for CMS use\)
-   `tablet`: Tablet interface only \(not for CMS use\)


</td></tr><tr><td>

Default detail page

</td><td>

Select which page loads after a user clicks a link.

</td></tr><tr><td>

Gauge page

</td><td>

Select which page is the drill-through target for any gauge. If you display a gauge on a CMS page, then clicking the links loads the page specified here.

</td></tr><tr><td>

Summary Template

</td><td>

Write an XML script that determines how the list is displayed in the list block, if the link is displayed in a list block.

</td></tr><tr><td>

Detail Template

</td><td>

Write an XML script that determines how to display the associated information after a user clicks the link.

</td></tr></tbody>
</table>
**Parent Topic:**[Content types](../concept/c_ContentTypes.md)

