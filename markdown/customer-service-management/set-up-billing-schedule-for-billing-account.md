---
title: Set up a billing schedule for a billing account
description: Set up a billing schedule for a billing account to define when billing occurs. A billing schedule uses the platform schedule and schedule entry records and is linked to the billing account through the billing schedule field.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/set-up-billing-schedule-for-billing-account.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Set up a billing schedule for a billing account

Set up a billing schedule for a billing account to define when billing occurs. A billing schedule uses the platform schedule and schedule entry records and is linked to the billing account through the billing schedule field.

## Before you begin

Role required: sn\_billing\_account.schedule\_writer, or a billing account role that contains it, such as sn\_billing\_account.crm\_b2b\_writer, sn\_billing\_account.writer, sn\_billing\_account.data\_manager, or sn\_billing\_account.admin.

**Note:** Users with sn\_billing\_account.schedule\_viewer role have read-only access to the schedule.

## About this task

A billing schedule is a schedule \(cmn\_schedule\) record made up of one or more schedule entry \(cmn\_schedule\_span\) records that define the billing periods. When you create a schedule from a billing account, the schedule **Type** is automatically set to **Billing Account**.

Each billing account uses a single billing schedule. You can reuse the same schedule for more than one billing account. However, if a schedule is shared, an information message appears on both the billing account and the schedule.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select a billing account from the list.

    For more information on how to create a billing account record, see [Install billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/install-billing-account.md).

3.  In the **Billing schedule** field, create a schedule or select an existing one.

    For more information about the fields on the schedule form, see [Schedule fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_ScheduleFields.md).

<table id="table_ba_bill_sched"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Billing Schedule

</td><td>

Schedule \(cmn\_schedule\) record that defines the billing periods for the billing account.**Note:** The **Billing schedule** field lists only schedules whose **Type** is Billing Account. Because the Schedule \(cmn\_schedule\) table is shared across the platform, the **Type** field identifies which schedules belong to billing accounts.

If you select a schedule that another billing account already uses, an information message indicates that the schedule is shared.

</td></tr></tbody>
</table>4.  Add schedule entry \(cmn\_schedule\_span\) records to the schedule to define the individual billing periods.

5.  Save the billing account to associate the billing schedule with the record.


