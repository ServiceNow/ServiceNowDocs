---
title: Confirm a vaccine exemption request for a user
description: As a Vaccination Status admin or manager, use the Employee Readiness Core Approval Portal to approve or deny a user's vaccine exemption request.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Confirm a vaccine exemption request for a user

As a Vaccination Status adminor manager, use the Employee Readiness Core Approval Portal to approve or deny a user's vaccine exemption request.

## Before you begin

Your organization must install both Health and Safety Testing and Vaccination Status to use the Approval Portal.

-   For more information on installing Health and Safety Testing, see [Install Health and Safety Testing](../../health-safety-testing/task/install-health-testing.md#).
-   For more information on installing Vaccination Status, see [Install Vaccination Status](install-vaccination-status.md#).

Activate the **sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_exemption\_records** property to enable all managers to approve or deny vaccine exemption requests for their direct reports. This property assigns the sn\_imt\_core.approval\_portal\_manager role to managers and grants access to the Approval Portal for vaccine exemption requests.

Your organization must enable vaccine exemptions. Exemptions do not affect a user's **Covid 19 Vaccine Complete** status in their vaccine profile. For more information, see [Set up Vaccination Status properties](config-vaccination-properties.md).

Role required: sn\_imt\_vaccine.admin, sn\_imt\_core.approval\_portal\_manager, or sn\_imt\_core.health\_and\_safety\_approver

## About this task

Managers can only approve or deny the vaccine exemption requests of their direct reports. Vaccine admins and health and safety approvers can approve or deny the requests of all users.

## Procedure

1.  Navigate to **Employee Health and Safety Status** &gt; **Approval Portal**.

    The default view displays all health test, vaccine dose, and exemption request records that require review.

2.  Filter the results.

    -   Change which record types are displayed by selecting a record type from the **Record** field list.
    -   Change how the records are sorted by selecting a value from the **Sort** field list.
3.  Search for the user whose exemption request you want to approve or deny.

4.  Select the user's attachments to review any submitted documentation.

5.  Select the record you want to review in the Vaccine exemption modal.

<table id="table_zkh_kmc_wrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Exemption type

</td><td>

Type of exemption being requested.

</td></tr><tr><td>

Status

</td><td>

Status of the exemption. The default status of an open exemption is **Submitted**.

</td></tr><tr><td>

Status updated by

</td><td>

Name of the admin or manager who updated the status of the user's request.

</td></tr><tr><td>

Expiration date

</td><td>

The date the exemption expires. If this field is blank, the exemption does not expire.

 **Note:** If no expiration date is set manually or by your organization's configuration, the exemption does not expire.

 You can update this field in the modal or Vaccine Exemption Request record. If you need to update this field in the modal, manually enter an expiration date or pick from the calendar.

</td></tr><tr><td>

Details

</td><td>

Details related to the exemption request.

</td></tr><tr><td>

Work notes

</td><td>

A log of work notes included for tracking purposes.

</td></tr></tbody>
</table>6.  Add additional information to the record in the work notes and click **Save**.

    The ability to add work notes is unavailable to managers.

7.  Approve or deny the user's submitted exemption request.

    -   To approve the user's exemption request, click **Approve**.
    -   To reject the user's exemption request, click **Deny**

## Result

The record is moved to the **Approved** or **Denied** tab based on your decision.The user's vaccine profile is updated to show who approved the vaccination exemption \(if approved\) and when it expires \(if applicable\).

**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

