---
title: Fix roles for external users with possible intentional internal role assignments
description: Review and fix roles for external users that might have intentional internal role assignments.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Fix external user role assignments, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Fix roles for external users with possible intentional internal role assignments

Review and fix roles for external users that might have intentional internal role assignments.

## Before you begin

Role required: admin

## About this task

It is recommended that you don’t assign internal roles to external users. Use this procedure to review and fix the contacts and consumers that may have the following role assignments:

-   snc\_internal role and one or more additional internal roles
-   snc\_internal role and one or more additional internal and external roles

**Note:** This guided setup task uses scheduled jobs to identify and fix role assignments. When fixing role assignments, the scheduled job fixes 3000 users at a time. If there are more than 3000 users in this group, change the configuration of the job so that it runs periodically.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup** and select **Get Started**.

2.  In the Fix External User Role Assignment category, select **Get Started** and then select **External users with possible intentional internal role assignments**.

3.  Run the scheduled job to tag users that may have intentional user role assignments.

    Users are tagged with the **Ext-user-intentional** tag.

4.  Review the list of tagged users and remove the tag from any users for which you don’t need to fix role assignments.

    If necessary, configure the list to display the Tag column.

5.  Run the scheduled job to fix the role assignments for the users with the **Ext-user-intentional** tag.

    This scheduled job makes the following changes:

    -   For users with the snc\_internal role and one or more additional internal roles, it removes the snc\_internal role and all other internal roles, and adds the snc\_external role.
    -   For users with the snc\_internal role and one or more additional internal and external roles, it removes the snc\_internal role and all other internal roles.
    This scheduled job runs all of the delete business rules on the User Role \[sys\_user\_has\_role\] table.


