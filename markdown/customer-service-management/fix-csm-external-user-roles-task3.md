---
title: Fix roles for external users with intentional internal role assignments
description: Review and fix roles for external users that have intentional internal role assignments.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Fix external user role assignments, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Fix roles for external users with intentional internal role assignments

Review and fix roles for external users that have intentional internal role assignments.

## Before you begin

Role required: admin

## About this task

It is recommended that you do not assign internal roles to external users. Use this procedure to review and fix the contacts and consumers that have the following role assignments:

snc\_internal role that is contained by another role.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup** and click **Get Started**.

2.  In the Fix External User Role Assignment category, click **Get Started** and then click **External users with intentional internal role assignments**.

3.  Run the scheduled job to tag users that have intentional user role assignments.

    Users are tagged with the **Ext-user-contained-role** tag.

4.  Review the list of tagged users.

5.  Manually fix the role assignments for the desired users.


