---
title: Create an ODBC user account and assign the odbc role
description: The ODBC driver communicates with your ServiceNow instance as a specific user. Create an ODBC user account and assign the odbc role to enable the user to communicate via ODBC.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Getting started with ODBC, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create an ODBC user account and assign the odbc role

The ODBC driver communicates with your ServiceNow instance as a specific user. Create an ODBC user account and assign the odbc role to enable the user to communicate via ODBC.

## Before you begin

Role required: admin

## About this task

The odbc role contains various additional roles, including the soap\_query role required to make ODBC requests and the itil role required to access core tables such as the incident table. You can modify the odbc role to allow access to other tables as needed by adding additional child roles.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Click **New**.

3.  In the **User ID** field, enter `odbc.user`.

4.  Enter a **Password** for this user.

5.  From the form context menu, select **Save**.

6.  In the **Roles** related list, click **Edit**.

7.  Use the slushbucket to add the odbc role, and then click **Save**.

8.  Click **Submit**.


## What to do next

In a separate browser session, confirm that the odbc.user is able to log in to your ServiceNow instance.

**Parent Topic:**[Getting started with ODBC](../concept/c_GettingStartedWithODBC.md)

**Previous topic:**[Getting started with ODBC](../concept/c_GettingStartedWithODBC.md)

**Next topic:**[Define an ACL rule for the odbc role](t_DefineAnACLRuleForTheODBCRole.md)

