---
title: Use an SLA map
description: View open work order tasks and their SLA status.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SLA for work orders, Manage work orders, Prepare work orders, Use, Field Service Management]
---

# Use an SLA map

View open work order tasks and their SLA status.

The SLA map view allows users with the wm\_admin, wm\_dispatcher, or dispatcher combination role to quickly see open work order tasks that are in danger of breaching their SLAs.

When the SLA map appears, the view is centered on the logged in user's location, from the **Location** field on the user record. Each task's icon color indicates the level of the SLA's **Business elapsed percentage**. This is the percentage of the SLA duration that has expired on the applicable business calendar, if one exists.

For example, a work order with an SLA of 5 business days starts on a Friday. On Tuesday the actual elapsed percentage for the SLA reaches 100%. However, the business elapsed percentage does not reach 100% until Thursday, because the business calendar shows that a business day runs from 8am to 5pm on weekdays. If the SLA breaches on Thursday, the business elapsed percentage continues upward from 100% until the task is completed. If no business calendar is in use, the business elapsed percentage equals the actual elapsed percentage.

