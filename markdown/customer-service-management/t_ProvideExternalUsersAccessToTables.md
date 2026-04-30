---
title: Provide external users access to a table
description: To enable users with only the snc\_external role to access the list view of a table, you must create a series of ACLs.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Roles installed with Customer Service Management, Components installed with Customer Service Management, Customer Service Management reference, Customer Service Management]
---

# Provide external users access to a table

To enable users with only the snc\_external role to access the list view of a table, you must create a series of ACLs.

## Before you begin

Role required: security\_admin

## Procedure

1.  [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

2.  [Create an ACL rule](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) with the following settings:

    -   **Type**: ui\_page
    -   **Operation**: read
    -   **Name**: \{table\_name\}\_list
    -   **Required role**: snc\_external
3.  On the default **read** ACL for the table, add **snc\_external** in the Required role list.

    Create the ACL if it does not already exist.

4.  Use these settings to create another ACL:

    -   **Type**: ui\_page
    -   **Operation**: read
    -   **Name**: \{table\_name\}
    -   **Required role**: snc\_external
5.  Use these settings to create another ACL to give the user write access to a field in the table:

    -   **Type**: record
    -   **Operation**: create
    -   **Name**: \{table\_name\} \{column\_name\}
    -   **Required role**: snc\_external
    Repeat this step for every field that you want to give the user write access to. Use an asterisk **\*** instead of the column name to provide access to all fields at once.


**Parent Topic:**[Roles installed with Customer Service Management](../../../product/customer-service-management/reference/r_RolesInstalledWithCustomerService.md)

