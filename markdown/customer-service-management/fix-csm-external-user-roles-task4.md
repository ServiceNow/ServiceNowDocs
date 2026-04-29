---
title: Avoid future internal role assignments for external users
description: Enable a property to avoid external users from being assigned the snc\_internal role.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Fix external user role assignments, User management, Set up your environment, Configure, Customer Service Management]
---

# Avoid future internal role assignments for external users

Enable a property to avoid external users from being assigned the snc\_internal role.

## Before you begin

Role required: csm\_guided\_setup\_user and security\_admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup** and select **Get Started**.

2.  In the Fix External User Role Assignment category, select **Get Started** and then select **Avoid such role assignments in future**.

3.  Set the **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** property to true.


