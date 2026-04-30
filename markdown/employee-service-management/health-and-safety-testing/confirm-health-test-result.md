---
title: Confirm COVID-19 test results for a user
description: Confirm a user's reported COVID-19 test results through the Employee Readiness Core Approval Portal.
locale: en-US
release: xanadu
product: Health and Safety Testing
classification: health-and-safety-testing
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Health and Safety Testing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Confirm COVID-19 test results for a user

Confirm a user's reported COVID-19 test results through the Employee Readiness Core Approval Portal.

## Before you begin

Your organization must install both Health and Safety Testing and Vaccination Status to use the Approval Portal.

-   For information on installing Health and Safety Testing, see [Install Health and Safety Testing](install-health-testing.md#).
-   For information on installing Vaccination Status, see [Install Vaccination Status](../../vaccination-status/task/install-vaccination-status.md#).

Activate the **sn\_imt\_health\_test.allow\_managers\_ability\_to\_update\_test\_result\_records** property to enable all managers to review and verify COVID-19 tests of their direct reports. This property assigns the sn\_imt\_core.approval\_portal\_manager role to managers and grants access to the Approval Portal for test results.

For more information, see [Set up Health and Safety Testing properties](configure-health-safety-testing.md#).

Role required: sn\_imt\_vaccine.admin, sn\_imt\_core.approval\_portal\_manager, or sn\_imt\_core.health\_and\_safety\_approver

Role required: sn\_imt\_vaccine.admin

## About this task

Managers can only confirm the COVID-19 test results of their direct reports. Vaccine admins and health and safety approvers can confirm the test results of all users.

## Procedure

1.  Navigate to **Employee Health and Safety Status** &gt; **Approval Portal**.

    The default view displays all health test, vaccine dose, and exemption request records that require review.

2.  Filter the results.

    -   Change which record types are displayed by selecting a record type from the **Record** field list.
    -   Change how the records are sorted by selecting a value from the **Sort** field list.
3.  Search for the user whose health test you want to approve or deny.

    The search behavior for the Approval Portal is a starts with search.

4.  Select the record to review the information included in the health test modal and any attachments.

    |Field|Description|
    |-----|-----------|
    |Test review outcome|The status of the health test review.|
    |Related test request|The test request record the health test is related to.|
    |Test result|The results of the test, such as positive or negative.|
    |Date you received the result|The date test results were received.|
    |COVID test result verified by|The person who verified the COVID-19 test result.|
    |Work notes|A log of work notes included for tracking purposes.|

5.  Add additional information to the record through work notes and click **Save**.

    The ability to add work notes is unavailable to managers.

6.  Approve or reject the user's health test results.

    -   To approve the user's health test results, select **Approve**.
    -   To reject the user's health test results, select **Deny**.
7.  Click **Verify** to verify the user's test results.


## Result

-   The record is moved to the **Approved** or **Denied** tab.
-   The **COVID test result verified by** field in the user's test result record is updated with your name to confirm you verified the result.
-   In the user's vaccine profile, the **Most recent COVID test result verified** option is selected.

**Parent Topic:**[Health and Safety Testing](../concept/health-safety-testing.md)

