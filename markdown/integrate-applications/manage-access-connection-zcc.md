---
title: Manage access to an established connection using roles
description: Manage which data stewards can access an established connection and create data fabric tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Manage access to an established connection using roles

Manage which data stewards can access an established connection and create data fabric tables.

## Before you begin

Role required: df\_connection\_admin

## About this task

Access to a zero copy connection in Zero Copy Connector Hub is controlled by the connection admin. The connection admin grants access using custom roles that identify the data stewards responsible for managing the quality and integrity of the data provided by the connection.

For example, an instance admin can create a custom role for an application and assign it to each of the data stewards who manage the data for that application. Once the role and the data stewards are defined, a connection admin can add the custom role to an established connection. When a custom role is added to the connection, it inherits the df\_data\_steward role, which grants access to the data stewards who have the custom role.

**Note:** Data stewards can access an established connection if they have a role that inherits the df\_data\_steward role. Users who are granted the df\_data\_steward role directly can view the Zero Copy Connector Hub but can't access any established connections.

## Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
2.  Select the connection that you want to configure.

3.  Select the **Access Control** tab.

4.  Grant data steward access by adding one or more roles.

    1.  Select **Manage Access**.

    2.  Browse or search for the role that you want to configure.

    3.  Select the check box next to the role.

    4.  Search and add additional roles as needed.

    5.  Select **Save changes**.

5.  Remove data steward access from one or more roles.

    1.  Select **Manage Access**.

    2.  Browse or search for the role that you want to update.

    3.  Clear the check box next to the role that you want to remove.

    4.  Search and remove additional roles as needed.

    5.  Select **Save changes**.


## Result

The df\_data\_steward role is granted to or removed from the selected roles. Each data steward with a role that contains the df\_data\_steward role can access the connection to create data fabric tables.

## Assigning data steward access to separate connections

1.  The connection admin creates separate connections for accessing external ITSM and finance data in Zero Copy Connector Hub.
2.  The instance admin creates the following custom roles in the ServiceNow AI Platform:
    -   df\_ITSM\_data\_steward
    -   df\_FINANCE\_data\_steward
3.  The instance admin identifies the users who are responsible for creating and maintaining data fabric tables for the ITSM and finance applications.
4.  The instance admin assigns the ITSM users to the df\_ITSM\_data\_steward role and the finance users to the df\_FINANCE\_data\_steward role.
5.  The connection admin grants the df\_data\_steward role to ITSM data stewards by adding to the df\_ITSM\_data\_steward role to the ITSM connection in Zero Copy Connector Hub.
6.  The connection admin grants the df\_data\_steward role to finance data stewards by adding the df\_FINANCE\_data\_steward role to the finance connection in Zero Copy Connector Hub.

After access is granted, ITSM data stewards can only access and manage external ITSM data, while finance data stewards can only access and manage external finance data.

**Parent Topic:**[Managing zero copy connections](../concept/managing-connections-zcc.md)

