---
title: Filter equipment model entities by operational status
description: Filter how equipment model entities appear in the Equipment Model Manager on the Industrial Workspace using a system property. Filtering equipment model entities can help you organize the data shown on the Industrial Workspace.
locale: en-US
release: zurich
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Review and update the equipment model details, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Filter equipment model entities by operational status

Filter how equipment model entities appear in the Equipment Model Manager on the Industrial Workspace using a system property. Filtering equipment model entities can help you organize the data shown on the Industrial Workspace.

## Before you begin

Role required: cmdb\_ot\_isa\_viewer and cmdb\_ot\_isa\_admin

## Procedure

1.  Navigate to **All** &gt; **Equipment Model - ISA** &gt; **System Properties**.

2.  Under **List of equipment model operational statuses that need to be filtered out from the equipment model page**, list the equipment model entities by**Operational Status** that you want removed from view in the Industrial Workspace.

    You can choose from the following options.

    -   Operational = 1
    -   Non-Operational = 2
    -   Repair in Progress = 3
    -   DR Standby = 4
    -   Ready = 5
    -   Retired = 6
    -   Pipeline = 7
    -   Catalog = 8
    -   Not in Use = 9
    For example, if you want to remove equipment model entities with **Operational Status** field values of **Retired** and**Not in Use**, list `6, 9`.


**Parent Topic:**[Review and update the equipment model details](equipment-model-workspace.md)

