---
title: Disable Quote Management application objects
description: Disable the business rules, client scripts, UI policies, and navigation items from the Quote Management application, which cannot run concurrently with ServiceNow Quote Experience on the same instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/disable-quote-management-fix-script.html
release: brazil
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 1
breadcrumb: [Without guided setup, Set up CPQ, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Disable Quote Management application objects

Disable the business rules, client scripts, UI policies, and navigation items from the Quote Management application, which cannot run concurrently with ServiceNow Quote Experience on the same instance.

## Before you begin

Role required: admin

**Note:** Review and document any customizations that you plan to re-implement before you disable the Quote Management objects.

## About this task

ServiceNow Quote Experience and the Quote Management application are not compatible and cannot run concurrently on the same instance. If Quote Management is installed, disable its objects before you use ServiceNow Quote Experience.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix scripts**.

2.  Search for `Disable objects for quote adv` in the **Name** field, then copy the script.

3.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

4.  Paste the script that you copied.

5.  Uncomment the `disableObjects();` line.

6.  Run the script.


## Result

Verify that the script disabled the Quote Management objects:

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.
2.  Filter the list to the **Quote** and **Quote Line Item** tables.
3.  Verify that all rules are disabled. Manually set **Active** to false for any rule that is still active.

