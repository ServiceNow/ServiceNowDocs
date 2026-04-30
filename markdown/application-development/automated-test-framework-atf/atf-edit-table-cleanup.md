---
title: Modify data retention policy for ATF test results
description: Modify the Auto Flush data retention policy, which designates how long the system retains data, and referencing data, for test and test suite results. You can change the frequency of flushing for the sys\_atf\_test\_result or sys\_atf\_test\_suite\_result base tables. This setting controls how far back in time test result data is available.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Administering the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Modify data retention policy for ATF test results

Modify the Auto Flush data retention policy, which designates how long the system retains data, and referencing data, for test and test suite results. You can change the frequency of flushing for the sys\_atf\_test\_result or sys\_atf\_test\_suite\_result base tables. This setting controls how far back in time test result data is available.

## Before you begin

Role required: atf\_test\_admin

## About this task

The system regularly flushes data in the sys\_atf\_test\_result and sys\_atf\_test\_suite\_result base tables, \(and optionally, referencing data\). By default, the system deletes test and test suite results data 30 days after creation. This task enables you to modify the Auto Flush retention policy for data stored in a specific base table \(sys\_atf\_test\_result or sys\_atf\_test\_suite\_result\).

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework** &gt; **Administration** &gt; **Table Cleanup**.

    The system displays a list of the retention policies \(Auto Flushes\) it maintains for automated testing results tables.

2.  Select the retention policy \(sys\_atf\_test\_result or sys\_atf\_test\_suite\_result\) to modify.

    The system displays the record for this retention policy.

    **Note:** The **Tablename** field displays the name of the table to which the selected Auto Flush retention policy applies. Selecting another tablename in this field compromises the integrity of the Auto Flush record. Leave the tablename on existing ATF policies at the base system \(default\) value so it does not adversely affect ATF data retention behavior.

3.  Specify how the system should determine the length of time for retention of data, and referencing data.

    1.  In the **Matchfield** field, enter the field you want the system to use to monitor duration.

        For example, to specify that you want to delete data x amount of time after the system created it, leave **Matchfield** set to its default value of **sys\_created\_on**.

    2.  In the **Age in seconds** field, enter the amount of time \(in seconds\) the system must wait before deleting the associated data and referencing data.

4.  If you want to apply the policy to the specified data \(for example, sys\_atf\_test\_result\), and to any data that references it, select **Cascade delete** \(default value\).

    Affected referencing data is stored the following tables: sys\_atf\_test\_result\_item, sys\_atf\_test\_result\_step, and sys\_attachment \(when table\_name = sys\_atf\_test\_result\). If you want the policy to simply flush data in the selected table \(for example, sys\_atf\_test\_result\), and skip flushing of the referencing data, then clear **Cascade delete**.

5.  In the **Conditions** field, specify the filter conditions to use for selection of data \(and optionally, referencing data\) for this Auto Flush retention policy.

    The default is **Retain indefinitely is false**, because the [Test results record](../reference/atf-test-results-record.md) also contains a **Retain indefinitely** check box that allows opting out of the auto flushes for specific test results.

6.  Click **Update**.


**Parent Topic:**[Administering the Automated Test Framework](../concept/atf-admin-overview.md)

