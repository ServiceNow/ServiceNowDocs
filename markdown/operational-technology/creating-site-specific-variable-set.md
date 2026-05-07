---
title: Create a Site-specific Variable set
description: Create a Site-specific Variable for use in Auto Queries. You can use the Variable as a credential for your Site.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sites page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Create a Site-specific Variable set

Create a Site-specific Variable for use in Auto Queries. You can use the **Variable** as a credential for your **Site**.

## Before you begin

Role required: admin

## About this task

**Note:** A Site can be associated to only one Variable.

## Procedure

1.  Navigate to the Variable page in the Console.

2.  Create a Variable as described in [Create a Variable set](create-variable-set.md).

3.  Select a Site to associate to the Variable.

4.  Create an Auto Query as described in [Create an Auto Query](add-auto-query-console.md).

5.  In the Filter section of the query, select the Sites filter.

6.  From the list of sites, select the site associated to your variable.

7.  Complete creating the query.

8.  Run the Auto Query that you created.


## Result

Your Site is associated with the Variable and queried.

