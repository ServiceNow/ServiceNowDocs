---
title: Delete a connection
description: Remove an established connection and its data fabric tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/delete-connection-zcc.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Update an established connection, Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Delete a connection

Remove an established connection and its data fabric tables.

## Before you begin

Role required: df\_connection\_admin

## About this task

A connection admin can remove an established connection from the Zero Copy Connector Hub by deleting the connection. To delete the connection, you must delete all the data fabric tables using the connection first.

## Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to delete.

    The current connection information is displayed on the **Connection details** tab.

3.  Delete the connection immediately if it doesn't have any associated tables or delete the associated tables and then delete the connection.

<table id="choicetable_wv5_lmf_w2c"><tbody><tr><td id="d685611e120">

**Delete a connection without any associated tables**

</td><td>

1.  Select the More Actions icon \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions icon\), and select **Delete**.
2.  In the confirmation dialog box, select **Delete**.


</td></tr><tr><td id="d685611e150">

**Delete a connection with associated tables**

</td><td>

1.  Select the More Actions icon \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions icon\), and select **Delete**.
2.  In the message that appears about deleting associated tables, select **View tables**.
3.  In the **Data fabric tables** tab, delete each associated table by selecting the More Actions icon \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions icon\), and selecting **Delete**.
4.  Navigate back to **Established connections**.
5.  Select the connection that you want to delete again.
6.  Select the More Actions icon \(\[Omitted image "more-actions-menu-icon.png"\] Alt text: More actions icon\), and select **Delete**.
7.  In the confirmation dialog box, select **Delete**.


</td></tr></tbody>
</table>
## Result

The connection and any associated tables are deleted from the Zero Copy Connector Hub.

**Parent Topic:**[Update an established connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/configure-connection-details-zcc.md)

