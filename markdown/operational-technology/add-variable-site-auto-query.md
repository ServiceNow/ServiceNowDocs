---
title: Create a Site-specific Variable set to use with Auto Query
description: Create a Site-specific Variable set for use in Auto Queries.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Variables page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Create a Site-specific Variable set to use with Auto Query

Create a Site-specific Variable set for use in Auto Queries.

## Before you begin

Role required: admin

## About this task

Create a Site-specific Variable set to define query Variable values for use in Auto Queries. You can use the Variable set as a credential for your Site.

**Note:** A Site can be associated to only one Variable.

## Procedure

1.  Navigate to the Variable page in the Console.

2.  Create a Variable as described in [Create a Variable set](create-variable-set.md).

3.  When you create the variable, select a Site to associate it.

4.  Create an Auto Query as described in [Create an Auto Query](add-auto-query-console.md).

5.  In the Filter section of the query, select the Sites filter.

6.  From the list of sites, select the site to associate to your variable.

7.  Complete creating the query.

8.  Run the Auto Query that you created.


## Result

Your Site is queried and associated to the Variable.

