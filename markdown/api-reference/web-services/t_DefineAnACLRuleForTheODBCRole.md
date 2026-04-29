---
title: Define an ACL rule for the odbc role
description: Define an ACL rule for the odbc role to provide read access to the incident table. You can create other ACL rules for the odbc role to provide read access to other tables.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Getting started with ODBC, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Define an ACL rule for the odbc role

Define an ACL rule for the odbc role to provide read access to the incident table. You can create other ACL rules for the odbc role to provide read access to other tables.

## Before you begin

Role required: admin

## Procedure

1.  Elevate the session permissions to security\_admin so you can create ACL rules.

2.  Navigate to **System Security** &gt; **Access Controls \(ACL\)**.

3.  Click **New**.

4.  From the **Operation** choice list, select **read**.

5.  From the **Name** choice list, select **Incident \[incident\]**.

    Leave the second **Name** choice list as **None**.

6.  From the form context menu, select **Save**.

7.  In the **Requires role** related list, click **Edit**.

8.  Use the slushbucket to add the ODBC role, and then click **Save**.

9.  Click **Submit**.


**Parent Topic:**[Getting started with ODBC](../concept/c_GettingStartedWithODBC.md)

**Previous topic:**[Create an ODBC user account and assign the odbc role](t_CreateAnODBCUser.md)

**Next topic:**[Installing the ODBC driver](../concept/c_InstallingTheODBCDriver.md)

