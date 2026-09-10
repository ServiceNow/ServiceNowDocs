---
title: Set up the Multi-Instance Framework for value calculations
description: Connect a subproduction instance to a production instance through the Multi-Instance Framework \(MIF\) so that the AI Control Tower can run value calculations across instances.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Set up the Multi-Instance Framework for value calculations

Connect a subproduction instance to a production instance through the Multi-Instance Framework \(MIF\) so that the AI Control Tower can run value calculations across instances.

## Before you begin

Before you begin:

-   You must have access to both the subproduction and the production instances.
-   Role required: `sn_ai_governance_ai_steward`

## About this task

Use the Multi-Instance Framework to register a subproduction instance under a production instance so that value calculations run against the correct managed instances.

## Procedure

1.  In the subproduction instance, create a record that defines the production instance in the Manager Instances \[`sn_mif_managed_by_instance`\] table with the following values.

    -   **Application**: AI Control Tower Core
    -   **Manager Instance**: select your production instance
2.  Wait a few minutes until the **Approval** field of the record updates to **Auto-Approved**.

3.  In the production instance, open the **AI Control Tower** workspace.

4.  Go to **Configurations**.

5.  On the **Multi-instance setup** tab, select **Add instances**, choose your subproduction instance, and then select **Save**.


## Result

The subproduction instance is registered with the production instance, and the AI Control Tower can run value calculations across the connected instances.

