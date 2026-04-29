---
title: Configure update set scanning properties
description: The Scan Engine provides several options to further configure update set scanning and enhance the governance over update set management. Update set scanning occurs during scheduled instance scans. The settings on this tab define which update sets will be scanned, and the parameters those update sets have to meet in order to be marked complete.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Scan Engine properties, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure update set scanning properties

The Scan Engine provides several options to further configure update set scanning and enhance the governance over update set management. Update set scanning occurs during scheduled instance scans. The settings on this tab define which update sets will be scanned, and the parameters those update sets have to meet in order to be marked complete.

## Before you begin

Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\).

Update sets are scanned in two scenarios:

-   During scheduled instance scans, based on the scanning condition
-   When a user attempts to mark an update set as Complete \(if enforcement is enabled\)

## Procedure

1.  Select whether to **Enable update set summary scan synchronization**.

    This allows update set summary scans to be synced between instances.

    **Note:** Data synchronization is exclusively for explicitly defined instances within the multi-instance communication API integration.

2.  **Table for update set scanning condition** specifies which table the scan condition builder references. By default, this is `sys_update_set`, and is typically not changed.

3.  Configure the **Update set scanning condition** properties using the condition builder.

    The Scan Engine uses these defined conditions to determine which update sets to scan for findings.

    By default, two conditions are already set to filter out both non-active and default update sets. `State is in progress` and `Name matches regex ^(?!Default).*`. The `regex ^(?!Default).*` condition filters out update sets named 'Default'. You can add and configure additional filter conditions by selecting **Add filter condition**. You can also add and configure OR clauses by selecting **Add OR clause**.

    **Note:** You can append filter conditions and OR clauses to existing conditions by selecting the AND or OR options next to them.

4.  Select whether to **Enforce update set validation**.

    Requires that update sets meet the conditions specified in step 5, **Conditions for completing an update set**, in order to be marked complete by a developer.

    **Important:** If the specified conditions are not met, a business rule validates the conditions before allowing the status to change to Complete. The update set cannot be marked complete until the set conditions are met.

5.  Configure the **Conditions for completing an update set** \(`table_for_update_set_completing`\) using the condition builder.

    The Scan Engine automatically scans update sets during a save when the status changes to **Complete**. It then uses these defined conditions to determine whether to allow that change or not.

6.  Select whether to **Override Environment Check for Update Set Scans**.

    When enabled, all active definitions run during update set scans regardless of instance-specific settings. This is useful for validating update sets before promoting them to production.


