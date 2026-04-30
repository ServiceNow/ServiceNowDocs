---
title: Manage and assign regulatory event alerts
description: Assign regulatory event alerts that are received from the regulatory intelligence provider to an appropriate user. You can review other properties of the regulatory event alert.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Regulatory alerts, Regulatory Change Management Core UI, Use, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Manage and assign regulatory event alerts

Assign regulatory event alerts that are received from the regulatory intelligence provider to an appropriate user. You can review other properties of the regulatory event alert.

## Before you begin

Role required: sn\_grc\_reg\_change.manager

## About this task

Regulatory alerts are displayed under the Regulatory Alerts module in the Regulatory Change Management application.

As a manager, you can view and assign the regulatory event alerts to users with the sn\_grc\_reg\_change.user role. The user can then perform actions on the regulatory event alerts.

## Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Regulatory Change Management** &gt; **Regulatory Alerts** &gt; **Unassigned Alerts**.

    All the regulatory alerts in your instance are displayed. You can view the unassigned alerts and assign them to a specific user. An incoming alert is automatically assigned to the New state.

2.  In the regulatory alert list, select a regulatory event alert by using the Type column.

    The alert record for the regulatory event alert is displayed.

3.  To assign the alert, set the **Coordinator** field to the appropriate user.

    You can review the other properties of the alert to help you determine the appropriate user to assign to.

<table id="table_qk5_sx2_rmb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of the alert as received from the provider.

</td></tr><tr><td>

Source

</td><td>

Source of the regulatory alert.

</td></tr><tr><td>

Description

</td><td>

Description and a brief summary of the event.

</td></tr><tr><td>

Provider

</td><td>

Name of the regulatory alert provider.

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

List of regulatory managers to whom you can assign the alert.

</td></tr><tr><td>

Overall impact

</td><td>

Overall impact of the field.-   No impact
-   Low
-   Medium
-   High
-   Critical


</td></tr><tr><td>

Type

</td><td>

Type of regulatory alert.-   Regulatory event
-   Source document


</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Dates

</td></tr><tr><td>

Source publication date

</td><td>

Date when the particular regulatory event is actually published by the regulatory body.

</td></tr><tr><td>

Comments date

</td><td>

Date until when the comments can be provided for the regulatory event.

</td></tr><tr><td>

Effective date

</td><td>

Date when the particular regulatory event will be applicable.

</td></tr><tr><td>

Compliance date

</td><td>

Date by which the regulatory event will be compliant.

</td></tr><tr><td>

Expiration date

</td><td>

Date when the particular regulatory event will expire.

</td></tr><tr><td class="sub-head" colspan="2">

Series data

</td></tr><tr><td>

Series name

</td><td>

Name of the series related to the regulatory alert.

</td></tr><tr><td>

Sequence number

</td><td>

Sequence number related to the regulatory alert.

</td></tr><tr><td class="sub-head" colspan="2">

Activity Journal

</td></tr><tr><td>

Additional comments

</td><td>

Additional comments related to the alert.

</td></tr><tr><td class="sub-head" colspan="2">

Related lists

</td></tr><tr><td>

Regulatory Tasks

</td><td>

Related tasks for the alert. This field is available only when a alert is assigned to a coordinator and it is in In Progress state.

</td></tr><tr><td>

Related Documents

</td><td>

Details of the documents related to the alert, such as a citation, title, or type.

</td></tr><tr><td>

Impact Assessments

</td><td>

Impact assessment details that are associated with the regulatory event alert.

</td></tr></tbody>
</table>4.  Select **Update**.


## Result

The regulatory event alert is assigned to the selected user and it is listed under the **All Assigned Alerts** module in the application.

**Parent Topic:**[Regulatory alerts](../concept/regulatory-feeds.md)

**Related topics**  


[Perform actions on regulatory alerts](perform-actions-reg-event-feeds.md)

[Add an AI-recommended citation to a regulatory alert](add-recommended-citations-to-a-regulatory-alert.md)

[Train and use the similarity solution to recommend citations on regulatory alerts](retrain-ml-reg-compliance-mapping.md)

[Manage and assign source document alerts](manage-source-document-feeds.md)

