---
title: State flow dictionary overrides
description: A dictionary override in a state flow defines the starting state for all new records in a specific table. You set an override in tables that extend a base table only, so that your customizations are applied only to the extended table.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [State flow customization, Service management states, Service Management]
---

# State flow dictionary overrides

A dictionary override in a state flow defines the starting state for all new records in a specific table. You set an override in tables that extend a base table only, so that your customizations are applied only to the extended table.

## Before you begin

Role required: admin

## Procedure

1.  In a state flow record, select an **Ending state**.

    This is the override value which becomes the starting state for all new records in the table named.

2.  Click **Create Default Value**.

    The system populates the **Dictionary override** field with a value of state, which is the field in the task table affected by the override. The Dictionary override field is read-only. After the override is created, the system hides the **Create Default Value** button on all subsequent state flow forms for that table.


**Parent Topic:**[State flow customization](../concept/c_StateFlowCustomization.md)

