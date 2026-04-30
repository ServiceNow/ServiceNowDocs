---
title: Add custom business rules to Service Level Agreement \(SLA\) considerations
description: Prior to adding custom business rules to the task SLA table, you must consider a few points regarding the processing and calculation of the task SLA based on your organization’s needs.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Service Level Management, IT Service Management]
---

# Add custom business rules to Service Level Agreement \(SLA\) considerations

Prior to adding custom business rules to the task SLA table, you must consider a few points regarding the processing and calculation of the task SLA based on your organization’s needs.

## Add custom fields to the task SLA table

You can add custom fields to the task SLA table and write business rules to populate them. This does not impact the SLA engine. However, you must consider performance implications, if any, of these business rules since task SLAs are updated frequently during their lifecycle.

## Points to consider

-   Business rule that directly updates the parent task when an SLA is updated.

    Avoid writing a business rule on the task SLA table that updates the parent task directly. Doing so causes recursive processing of the business rules. This is represented in the diagram.

    ![Diagram of a recursive business rule](../image/SLARecursive.png "Recursive business rule")

-   Business rule that updates the default fields on a task SLA.

    Avoid writing a business rule on the task SLA table that updates the default fields. These default fields are managed and updated by the SLA engine and any updates made to them might result in the following.

    -   Fields being ignored, overwritten, or both the next time the SLA is calculated.
    -   Incorrect calculations of other values on the task SLA.

**Parent Topic:**[Using Service Level Management](../concept/using-service-level-management.md)

