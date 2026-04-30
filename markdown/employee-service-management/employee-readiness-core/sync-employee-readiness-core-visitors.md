---
title: Synchronize Employee Readiness Core visitors with Workplace Visitor Management
description: As an administrator, synchronize the visitor tables in the Employee Readiness Core and Workplace Visitor Management applications.
locale: en-US
release: zurich
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Employee Health and Safety Status, Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Synchronize Employee Readiness Core visitors with Workplace Visitor Management

As an administrator, synchronize the visitor tables in the Employee Readiness Core and Workplace Visitor Management applications.

## Before you begin

To successfully enable visitor synchronization between Employee Readiness Core and the Workplace Visitor Management application in Workplace Service Delivery, note the following requirements:

-   The Workplace Visitor Management application must be installed. For more information, see [Install Workplace Visitor Management](../../workplace-visitor-mgmt/task/install-workplace-visitor-mgmt.md).
-   Ensure your organization has a data backup before running the `Sync Visitors` fix script. Otherwise, syncing is not reversible.

Role required: admin or sn\_imt\_core.admin

## About this task

To maintain consistent data on visitors, organizations may synchronize data between the Employee Readiness Core sn\_imt\_core\_visitor table and the sn\_wsd\_visitor\_visitor table in Workplace Visitor Management.

An initial synchronization using the `Sync Visitors` fix script is required before updates are synced automatically. Newly added fields to either visitor table are ignored by the fix script while existing fields are left as-is. Administrators with the script\_include\_admin role may customize the `VisitorSyncing` and `WSDVisitorSyncing` script includes called by the fix script to meet their organization’s needs, for example, to accommodate new fields added to the visitor tables. Administrators must run the fix script after performing any customizations to the script includes.

Any data conflicts are resolved by using the most recent changes to a table. After the tables are synchronized, updates to one table automatically are reflected on the other.

**Important:** Do not delete visitors from the Employee Readiness Core sn\_imt\_core\_visitor table because they do not sync back to Workplace Visitor Management. Deletions from the sn\_wsd\_visitor\_visitor table are performed when you anonymize a visitor. Anonymized data does sync to the sn\_imt\_core\_visitor table. For more information on anonymizing visitors or deleting visitor data in Workplace Visitor Management, see [Anonymize a visitor](../../workplace-visitor-mgmt/task/anonymize-visitor.md).

Synchronization can be disabled; however, the initial sync is irreversible without a backup.

## Procedure

1.  Unless the **sn\_imt\_core.visitor\_syncing** property is already enabled and the initial fix script run was completed, enable this property.

    This property controls visitor syncing between visitors in Employee Readiness Core and Workplace Visitor Management. It is disabled by default.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Properties**.

    2.  Set the **sn\_imt\_core.visitor\_syncing** property to **Yes**.

    3.  Click **Save**.

2.  Navigate to **System Definition** &gt; **Fix Scripts**.

3.  Open the `Sync Visitors` fix script from the list.

4.  If the **Active** check box for **Sync Visitors** is not selected, select it and click **Update**.

5.  Click **Run Fix Script**.


## Result

Visitor records synchronize between the Employee Readiness Core visitor table and the sn\_wsd\_visitor\_visitor table in Workplace Visitor Management.

If your organization wants to disable synchronization, navigate to **Employee Health and Safety Status** &gt; **Properties**, clear the **sn\_imt\_core.visitor\_syncing** check box, and click **Save**.

**Parent Topic:**[Employee Health and Safety Status](../concept/employee-health-safety-status.md)

