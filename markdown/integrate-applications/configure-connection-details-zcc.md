---
title: Update an established connection
description: Keep connection details current by updating service account information, authentication, or security settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/configure-connection-details-zcc.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
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

If the connection fails, [View the connection log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/view-connection-log-zcc.md). Review the connection details with the data source admin and try again.

If your changes impact data fabric tables, ensure the proper access is configured on the **Access Controls** tab.

-   **[View the connection log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/view-connection-log-zcc.md)**  
Monitor and troubleshoot a connection by viewing the connection log.
-   **[Deactivate a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/deactivate-connnection-zcc.md)**  
Temporarily disable the connection between data fabric tables and their data source by deactivating a connection.
-   **[Reactivate a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/reactivate-connnection-zcc.md)**  
Manage data assets and access control in a deactivated connection by reactivating it.
-   **[Delete a connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/delete-connection-zcc.md)**  
Remove an established connection and its data fabric tables.

**Parent Topic:**[Managing zero copy connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/managing-connections-zcc.md)

