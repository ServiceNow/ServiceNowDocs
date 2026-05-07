---
title: Review overridden records
description: You can view information about specific overridden records and mark them reviewed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [View upgraded processes or records in the global domain, Setup and administration, Domain separation for service providers, Access Management]
---

# Review overridden records

You can view information about specific overridden records and mark them reviewed.

## Before you begin

Role required: domain\_admin or admin

**Note:** Advanced features require read access to all process tables. Using the Admin role is recommended.

## Procedure

1.  Select a file name on the Upgraded **Overridden Domain Records** tab to review its associated overridden record.

    This lets you view the overridden record's relationship to the original global record.

2.  From **Related Links**, select **Show Related Record** to directly open the affected global record that was overridden as a result of the upgrade.

    **Note:** You will need the Admin role to use this feature.

3.  You can select **Preview Overrides** to view all records that override the associated global record across different domains. This will display all overrides related to that global record.

    **Note:** You will need the Admin role to use this feature.

4.  Under the **Related Links** is the **Override Processes** table, which shows:

    | | |
    |---|---|
    |Process Name|Name of the process \(for example, Business Rule, UI Action, or Deactivate Audit\) that is overriding the upgraded global record.|
    |Domain Name|Name of the domain in which the record is overriding the upgraded global record.|

5.  You can check a process name then select **Compare**. This allows users to view a side-by-side comparison of the overridden version \(version in global domain\) and the updated override version \(version in a specific domain\).

    **Note:** You will need the Admin role to use this feature.


## What to do next

Once you've reviewed the record's information, you can return to the overridden record and finish your review. Enter comments in the **Review Notes** field on the main page, then select **Confirm Review** to indicate you've reviewed it.

**Note:** This marks the overridden record as **Reviewed**, and the dashboard will now indicate this status for the record.

