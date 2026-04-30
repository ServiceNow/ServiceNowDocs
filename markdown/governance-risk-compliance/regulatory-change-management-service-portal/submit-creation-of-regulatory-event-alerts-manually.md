---
title: Create regulatory event alerts manually
description: Create a manual entry of the regulatory changes or updates so that they can be routed to the correct subject matter experts for further analysis.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Create regulatory event alerts manually

Create a manual entry of the regulatory changes or updates so that they can be routed to the correct subject matter experts for further analysis.

## Before you begin

Role required: sn\_grc\_reg\_change.manager

## About this task

Users with the sn\_grc\_reg\_change.manager role can create the regulatory alerts manually. Creating the regulatory alerts manually provides the following benefits:

-   Recognize and fix human instinctive errors accurately.
-   Assign an ad-hoc or the submitted regulatory event alert to the subject matter experts for further review and analysis, thus ensuring accountability.
-   Ensure that the data entered manually in the system has high quality and a high level of integrity.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **Compliance Workspace** &gt; **Regulatory alerts** &gt; **Unassigned Alerts**.

    The Regulatory Change Management application in the Compliance Workspace is displayed.

2.  Select **New**.

    The Create New Regulatory alert form is displayed.

3.  On the **Details** tab, fill in the form.

<table id="table_ahp_f3p_11c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

A short summary title of the regulatory alert.

</td></tr><tr><td>

Source

</td><td>

Displays the data source type identified for creating a regulatory event record. The default option for the input source type is Manual.

 **Note:** This field is locked for editing for the purpose of internal reporting and business configuration management.

</td></tr><tr><td>

Type

</td><td>

Type of regulatory alert.

</td></tr><tr><td>

Description

</td><td>

Description and a summary of the event.

</td></tr><tr><td>

Provider

</td><td>

Name of the alert provider.**Note:** This field is locked for editing for the purpose of internal reporting and business configuration management.

</td></tr><tr><td>

Provider URL

</td><td>

URL of the alert that is received from the provider.

</td></tr><tr><td>

Regulatory body URL

</td><td>

URL of the regulatory body that is associated with the alert.

</td></tr><tr><td>

Coordinator

</td><td>

User that the alert is assigned to.

</td></tr><tr><td>

Overall impact

</td><td>

Overall impact of the alert.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Dates

</td></tr><tr><td>

Source publication date

</td><td>

Date when the regulatory event is published by the regulatory body.

</td></tr><tr><td>

Comments date

</td><td>

Date until when the comments can be provided for the regulatory event.

</td></tr><tr><td>

Effective date

</td><td>

Date when the regulatory event is going to be applicable.

</td></tr><tr><td>

Compliance date

</td><td>

Date by which the regulatory event is going to be compliant.

</td></tr><tr><td>

Expiration date

</td><td>

Expiry date for the regulatory event.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Additional comments

</td><td>

Additional comments related to the alert.

</td></tr></tbody>
</table>    **Note:** Beginning with the Yokohama release, the taxonomy section in the form is not available for the new installations.

4.  In the **Coordinator** field, assign the regulatory event alert to a coordinator with the sn\_grc\_reg\_change.user role and select **Save**.


## Result

The regulatory event alert is assigned to the selected coordinator.

## What to do next

[Import the regulatory event alerts in bulk](import-regulatory-event-alerts-in-bulk.md) and [Assess the impact of a regulatory event alert](assess-impact-of-reg-change-using-ws.md).

