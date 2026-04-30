---
title: Test an LDAP connection
description: The instance tests the connection automatically every time a user opens the LDAP Server form. Alternatively, you can manually test the connection to the LDAP server from the LDAP server form.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Test an LDAP connection

The instance tests the connection automatically every time a user opens the LDAP Server form. Alternatively, you can manually test the connection to the LDAP server from the LDAP server form.

## Before you begin

Role required: admin

## About this task

By default, error messages appear on the LDAP server form if there are any issues connecting to the LDAP server.

**Note:** Employees can also verify connectivity between the instance and the LDAP server. Contact Technical Support for assistance verifying LDAP connectivity.

To manually test a connection:

## Procedure

1.  Navigate to **All** &gt; **System LDAP** &gt; **LDAP Servers**.

2.  Select the LDAP server to test.

3.  Under **Related Links**, click **Test connection**.

4.  Under **Related Links**, click **Browse** to verify that the appropriate LDAP directory structure is visible to the system.

5.  If the connection was successful, click **Browse** to view the source LDAP directory structure that is visible to the instance.

    **Note:** The **Filter** and **RDN** fields on the left of the Browse window are ignored when you use the search field on the right.


## Result

The instance changes the operational status of LDAP servers depending on the result of the connection test.

-   If your instance establishes a connection to a server that has a **Operational Status** value of **down**, the **Operational Status** value is automatically changed to **up**. This functionality is supported for both automatic and manual connection tests.
-   If a connection cannot be established to a server that has a **Operational Status** value of **up**, the **Operational Status** value is automatically changed to **down**. This functionality is supported for automatic connection tests only, not manual tests.

