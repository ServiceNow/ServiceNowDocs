---
title: Run scheduled job to populate product offering categories
description: After upgrading to the Zurich release and the Now Assist for Sales Force Automation \(SFA\) plugin is installed, run a scheduled job that generates the product offering categories for pre-existing product offerings in the product catalog with AI Search.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI Search for product catalog, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Run scheduled job to populate product offering categories

After upgrading to the Zurich release and the Now Assist for Sales Force Automation \(SFA\) plugin is installed, run a scheduled job that generates the product offering categories for pre-existing product offerings in the product catalog with AI Search.

## Before you begin

Role required: admin

## About this task

Run the scheduled job called **Scheduled job to populate product\_offering\_categories glide list for product offerings** only if you've upgraded from a release before the Australia release. This job adds the product offering categories field to the Product Offering table. If you're a new customer using the Australia release or Zbooted, do not run this job.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

2.  In the **Search** field, enter **Scheduled job to populate product\_offering\_categories glide list for product offerings**.

3.  Select **Execute Now** to run the scheduled job.


## What to do next

Run the scheduled job to index the tables, publish the stop word dictionary, and publish search profiles.

