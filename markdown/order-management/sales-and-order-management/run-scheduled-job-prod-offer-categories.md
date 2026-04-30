---
title: Run scheduled job to populate product offering categories
description: After upgrading to the Zurich release and the Now Assist for Sales and Order Management plugin is installed, run a scheduled job that generates the product offering categories for pre-existing product offerings in the product catalog with AI Search.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-12-03"
reading_time_minutes: 1
breadcrumb: [AI Search for product catalog, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Run scheduled job to populate product offering categories

After upgrading to the Zurich release and the Now Assist for Sales and Order Management plugin is installed, run a scheduled job that generates the product offering categories for pre-existing product offerings in the product catalog with AI Search.

## Before you begin

Role required: admin

## About this task

Run the scheduled job called **Scheduled job to populate product\_offering\_categories glide list for product offerings** only if you've upgraded from a release before the Zurich release. This job adds the product offering categories field to the Product Offering table. If you're a new customer using the Zurich release or Zbooted, do not run this job.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.

2.  In the **Search** field, enter **Scheduled job to populate product\_offering\_categories glide list for product offerings**.

3.  Select **Execute Now** to run the scheduled job.


## What to do next

[Run the scheduled job to publish the stop words dictionary, search profiles, and index tables](run-sched-job-index-stopwords-profile.md).

