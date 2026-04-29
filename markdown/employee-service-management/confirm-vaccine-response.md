---
title: Confirm the reported vaccination status for a user
description: As a Vaccination Status admin or manager, use the Employee Readiness Core Approval Portal to confirm a user's reported COVID-19 vaccination status.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Confirm the reported vaccination status for a user

As a Vaccination Status adminor manager, use the Employee Readiness Core Approval Portal toconfirm a user's reported COVID-19 vaccination status.

## Before you begin

Your organization must install both Health and Safety Testing and Vaccination Status to use the Approval Portal.

-   For more information on installing Health and Safety Testing, see [Install Health and Safety Testing](../../health-safety-testing/task/install-health-testing.md#).
-   For more information on installing Vaccination Status, see [Install Vaccination Status](install-vaccination-status.md#).

Activate the **sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_response\_records** property to enable all managers to confirm the reported vaccination status of their direct reports. This property assigns the sn\_imt\_core.approval\_portal\_manager role to managers and grants access to the Approval Portal for vaccine responses.

Role required: sn\_imt\_vaccine.admin, sn\_imt\_core.approval\_portal\_manager, or sn\_imt\_core.health\_and\_safety\_approver

## About this task

In the Approval Portal, you can review the results of user-reported vaccinations and approve or reject the responses. Approvals can be based on a user's proof of vaccination, such as their attachments submitted with their vaccine response. If the **Reset Covid 19 Vaccine Complete to false if Vaccine Review Outcome is Rejected** property is enabled, a user's COVID-19 vaccine completed status depends on the responses being approved.

**Note:** Managers can only confirm the vaccine responses only of their direct reports. Vaccine admins and health and safety approvers can confirm the responses of all users.

For more information, see [Set up Vaccination Status properties](config-vaccination-properties.md).

Organizations that want to automatically review vaccine responses must configure Vaccination Status to support the functionality. For more information, see [Automate reviews of vaccine responses](enable-automated-vaccine-response-reviews.md).

## Procedure

1.  Navigate to **Employee Health and Safety Status** &gt; **Approval Portal**.

    The default view displays all health test, vaccine dose, and exemption request records that require review.

2.  Filter the results.

    -   Change which record types are displayed by selecting a record type from the **Record** field list.
    -   Change how the records are sorted by selecting a value from the **Sort** field list.
3.  Search for the user whose vaccination status you want to confirm.

    The search behavior for the Approval Portal is a starts with search.

4.  Select the record to review the information included in the Vaccine response modal and any attachments.

    |Field|Description|
    |-----|-----------|
    |Manufacturer|The manufacturer of the vaccine or booster dose.|
    |Date administered|Date the vaccine or booster was administered.|
    |Vaccine reviewed date|Date the vaccine response was reviewed.|
    |Verified by|Who verified the vaccine response.|
    |Vaccine review outcome|The result of the vaccine review, such as whether it was approved or denied.|
    |Validator state|If your organization enables the ability for Vaccination Status to automatically validate vaccinations with validator services, such as CommonTrust Network, this field populates based on the review. A status of **Complete** indicates that the validator was able to successfully run. The results of the validation are included in the work notes.|
    |Work notes|A log of work notes included for tracking purposes.|

5.  Add additional information to the record in the work notes and click **Save**.

    The ability to add work notes is unavailable to managers.

6.  Approve or reject the user's submitted vaccination status.

    -   To approve the user's vaccination status, click **Approve**.
    -   To reject the user's vaccination status, click **Deny**.

## Result

The record is moved to the **Approved** or **Denied** tab based on your decision and the **Verified by** field in the user's vaccine response record is updated with your name. Based on your organization's configurations, your review might affect the user's COVID-19 vaccine complete status.

For more information on configuring Vaccination Status, see [Set up Vaccination Status properties](config-vaccination-properties.md).

**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

