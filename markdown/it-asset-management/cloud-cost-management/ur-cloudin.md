---
title: Unassigned resources
description: Unassigned resources policies help you to identify the resources that aren’t associated with a change group and to assign them appropriately. When a resource is assigned to the correct group, the resource can be appropriately governed even as it goes through stages such as patching, upgrading, and reconfiguring.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Unassigned resources

Unassigned resources policies help you to identify the resources that aren’t associated with a change group and to assign them appropriately. When a resource is assigned to the correct group, the resource can be appropriately governed even as it goes through stages such as patching, upgrading, and reconfiguring.

The Cloud Cost Management application can generate compute and database recommendations for AWS, Azure, and GCP. The latest data is fetched every day at midnight.

## How Unassigned resources processes work

For cloud billing information to be accurate, it must include all resources in your managed cloud infrastructure. An Unassigned resources policy analyzes all resources to identify resources that aren’t assigned to a change group. The policy can then auto-assign the appropriate change group to the resources. Unassigned resources jobs follow this process:![Process flow for Unassigned Resources](../image/ur-process-flow-diagram.png)

## Requirements and limitations

-   The Discovery process triggers Unassigned Resources analysis and updates recommendations in reports.
-   For AWS, the Unassigned Resources feature supports AWS EC2 instances only.
-   Terminated, retired, or canceled resources aren’t considered.
-   Data appears on reports only when at least one policy is active.

