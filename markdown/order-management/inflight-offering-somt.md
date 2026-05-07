---
title: Managing inflight order for site projects
description: Manage how your organization receives changes for customer orders, service orders or individual line items that are still being orchestrated and fulfilled.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Managing inflight order for site projects

Manage how your organization receives changes for customer orders, service orders or individual line items that are still being orchestrated and fulfilled.

When you create an inflight order with a new site and new product offering, it creates new site project and new sub-projects for the offerings using the same program.

When you create an inflight order with new product offering for existing site project using the same program, it creates new sub-project for the new product offering. An existing site project is reused and it will not create new site project. The site project tasks and templates may be updated to reflect newly added products.

## Cancel order for site project

When a product offering on an inflight customer order is canceled, the corresponding sub-project and all associated tasks must be automatically closed.

If all product offerings \(or all related sub-projects\) under a parent project are closed, the main parent project must also be automatically transitioned to a terminal state. In such cases, its status much be updated to **Closed Skipped**.

If the parent site project is canceled, all linked child projects and associated product offerings under that site project are closed automatically.

All records moved to a terminal state are set to **Closed Skipped**.

Does not delete any records as part of this process.

