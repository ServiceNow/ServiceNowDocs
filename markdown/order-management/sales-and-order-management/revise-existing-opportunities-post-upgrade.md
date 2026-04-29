---
title: Revise existing opportunities after an upgrade
description: Run a scheduled job to modify older opportunities so they can support parent-child opportunity line items.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install and configure Opportunity Management, Lead and opportunity management apps, Configure, Sales and Order Management]
---

# Revise existing opportunities after an upgrade

Run a scheduled job to modify older opportunities so they can support parent-child opportunity line items.

## Before you begin

Role required: admin

## About this task

The scheduled job helps update opportunity lines on the opportunities created on or before the Yokohama Q1 release. From Yokohama Q2 release onward, the opportunity lines follow a hierarchical parent-child structure. The hierarchy is achieved by adding new fields on an opportunity line and affects the pricing functionality. For the existing lines to incorporate the updated pricing functionality, the newly added fields must be populated and the hierarchical structure must be in place.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  On the scheduled job menu, search for the **Revise existing Opportunities on upgrade** job.

3.  Open the job and select **Execute Now**.

4.  Navigate to **All** &gt; **System Logs** &gt; **System Log** &gt; **All**.

5.  Confirm that the job has been completed by checking for the `Opportunity Upgrade Job completed` message.

    The log lists the total number of records processed, along with their success and failure count.

    **Note:** If the job is abruptly stopped, the log displays `Opportunity Upgrade Job encountered errors` in addition to the error message.


## Result

The scheduled job updates the open opportunities \(not in any of the closed stages\). The job works differently for opportunities that are synced to Quote than the ones that aren't.

## Example

For open, non-synced opportunities:

1.  The scheduled job updates the newly added **Top Opportunity Line Item** and **Product Specification** fields for all the opportunity lines.
2.  If a complex product offering has a child offering, the job creates child opportunity lines under the parent line. Newly created child lines contain correct values populated for the newly added fields.
3.  A subsequent pricing call is made to populate pricing fields for all the lines in the hierarchy.

For open, synced opportunities:

1.  A scheduled job updates the newly added **Top Opportunity Line Item** field for all the opportunity lines.
2.  The **Product Specification** field, new hierarchy, and pricing fields for this line are updated only if any change is done on the corresponding synced quote line.

**Note:** After upgrading to the Yokohama Q2 release, run the scheduled job before working with Opportunity. Failure to do so results in inconsistent behavior in Opportunity and the related tables.

