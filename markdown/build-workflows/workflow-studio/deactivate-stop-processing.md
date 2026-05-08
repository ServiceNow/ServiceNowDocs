---
title: Allow multiple triggers to process an inbound email
description: Configure Workflow Studio to allow an inbound email to be processed by multiple inbound email triggers in a specific order.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [With inbound email trigger, Create a flow, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Allow multiple triggers to process an inbound email

Configure Workflow Studio to allow an inbound email to be processed by multiple inbound email triggers in a specific order.

## Before you begin

Role required: admin

## About this task

Although you can process an inbound email with multiple inbound email actions, you can't process an inbound email with multiple flows by default. You can add a system property to let process owners use multiple triggers to process an inbound email.

**Warning:** Allowing multiple triggers to process an inbound email may increase maintenance and decrease system performance.

## Procedure

1.  Add a property with the following settings:

    -   Name: **glide.hub.flow.inbound\_email\_trigger.show\_advanced**
    -   Type: true \| false
    -   Value: true
    After you activate the system property, the **Order** and **Stop processing** fields appear on the inbound email trigger.

2.  Create multiple flows with an inbound email trigger.

    For more information, see [Create a flow with an inbound email trigger](../../flow-designer/task/create-inbound-email-flow.md).

3.  Specify the processing order for each of the inbound email flows:

    1.  Open each flow and enter a value in the **Order** field.

        To give the flow higher priority over other flows, enter a lower number.

    2.  Enable or disable stop processing for each flow in your sequence.

        To allow an inbound email to be processed by the next flow in your sequence, clear the **Stop processing** option.

        To end the sequence on a particular flow, leave the option selected in that flow.


**Parent Topic:**[Create a flow with an inbound email trigger](../../flow-designer/task/create-inbound-email-flow.md)

