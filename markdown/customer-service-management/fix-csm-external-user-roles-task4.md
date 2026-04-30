---
title: Prevent future internal role assignments for external users
description: Enable a property to prevent external users from being assigned the snc\_internal role.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Fix external user role assignments, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Prevent future internal role assignments for external users

Enable a property to prevent external users from being assigned the snc\_internal role.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup** and click **Get Started**.

2.  In the Fix External User Role Assignment category, click **Get Started** and then click **Avoid such role assignments in future**.

3.  Set the **glide.security.explicit\_roles.enable\_internal\_user\_blacklist** property to true.


