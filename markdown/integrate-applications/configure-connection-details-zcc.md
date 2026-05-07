---
title: Update an established connection
description: Keep connection details current by updating service account information, authentication, or security settings.Monitor and troubleshoot a connection by viewing the connection log.Temporarily disable the connection between data fabric tables and their data source by deactivating a connection.Manage data assets and access control in a deactivated connection by reactivating it.Remove an established connection and its data fabric tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Update an established connection

Keep connection details current by updating service account information, authentication, or security settings.

## Before you begin

Role required: df\_connection\_admin

## Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to configure.

3.  Update the connection details.

    **Important:** Changing connection details can affect data mapping in the data fabric tables created using this connection. If you need to preserve the current data mapping, consult the data source administrator before updating the connection to ensure the data mapping isn't affected.

    1.  Select **Edit**.

    2.  Update the connection identification.

        For example, update the connection description if data stewards can't find the connection or if the data source admin adds new data assets.

    3.  Update the connection attributes.

        For example, you might update the connection attributes if the connection URL or service account information changes.

    4.  Update the authentication method or private key information.

        For example, update the private key and pass phrase when the private key changes or is no longer valid.

    5.  In the confirmation dialog box, confirm that you want to make the changes by selecting **Edit**.

4.  Select **Save and connect**.


## Result

The system tests the connection. If connection succeeds, the changes are saved.

## What to do next

If the connection fails, [View the connection log](configure-connection-details-zcc.md#). Review the connection details with the data source admin and try again.

If your changes impact data fabric tables, ensure the proper access is configured on the **Access Controls** tab.

**Parent Topic:**[Managing zero copy connections](../concept/managing-connections-zcc.md)

## View the connection log

Monitor and troubleshoot a connection by viewing the connection log.

### Before you begin

Role required: df\_connection\_admin

### Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to monitor.

3.  Select the More Actions icon \(![More actions icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), and select **View Connection Logs**.


### Result

The Data Fabric Logs \[df\_log\] table appears, displaying log entries for the current day related to this connection.

### What to do next

Review the log entries and consult your data source administrator if necessary. Update the connection details if any connection attributes are incorrect. See [Update an established connection](configure-connection-details-zcc.md#).

## Deactivate a connection

Temporarily disable the connection between data fabric tables and their data source by deactivating a connection.

### Before you begin

Role required: df\_connection\_admin

### About this task

A connection admin can stop queries to an external data source or prevent changes to data mapping by deactivating a connection. When a connection is deactivated, external data isn't available from any data fabric tables using the connection.

### Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to deactivate.

3.  Select the More Actions icon \(![More actions icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), and select **Deactivate**.

4.  Confirm that you want to deactivate the connection by selecting **Deactivate**.


### Result

The connection is deactivated.

-   External data is no longer pulled by any data fabric table using the connection.
-   The **Data Assets** tab and **Access Control** tabs aren't accessible in the connection.

### What to do next

To update the connection information or access the **Data Assets** or **Access Control** tabs again, you must reactivate the connection. See [Reactivate a connection](configure-connection-details-zcc.md#).

## Reactivate a connection

Manage data assets and access control in a deactivated connection by reactivating it.

### Before you begin

Role required: df\_connection\_admin

### About this task

A connection admin can reactivate a connection that's been temporarily deactivated.

### Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to reactivate.

    **Note:** View all deactivated connections by selecting **Deactivated** in the **Status** list.

3.  Select **Reactivate**.

4.  Review and update connection details as needed.

5.  Select **Save and connect**.


### Result

The connection is activated.

-   External data is pulled by any data fabric table using the connection.
-   The **Data Assets** tab and **Access Control** tabs are accessible in the connection.

## Delete a connection

Remove an established connection and its data fabric tables.

### Before you begin

Role required: df\_connection\_admin

### About this task

A connection admin can remove an established connection from the Zero Copy Connector Hub by deleting the connection. To delete the connection, you must delete all the data fabric tables using the connection first.

### Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to delete.

    The current connection information is displayed on the **Connection details** tab.

3.  Delete the connection immediately if it doesn't have any associated tables or delete the associated tables and then delete the connection.

<table id="choicetable_wv5_lmf_w2c"><tbody><tr><td id="d531286e780">

**Delete a connection without any associated tables**

</td><td>

1.  Select the More Actions icon \(![More actions icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), and select **Delete**.
2.  In the confirmation dialog box, select **Delete**.


</td></tr><tr><td id="d531286e810">

**Delete a connection with associated tables**

</td><td>

1.  Select the More Actions icon \(![More actions icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), and select **Delete**.
2.  In the message that appears about deleting associated tables, select **View tables**.
3.  In the **Data fabric tables** tab, delete each associated table by selecting the More Actions icon \(![More actions icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), and selecting **Delete**.
4.  Navigate back to **Established connections**.
5.  Select the connection that you want to delete again.
6.  Select the More Actions icon \(![More actions icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), and select **Delete**.
7.  In the confirmation dialog box, select **Delete**.


</td></tr></tbody>
</table>
### Result

The connection and any associated tables are deleted from the Zero Copy Connector Hub.

