---
title: Report an operational vulnerability from the module
description: Report an operational vulnerability from the Operational vulnerability module in the Operational Resilience Workspace.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reporting Operational vulnerability, Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Report an operational vulnerability from the module

Report an operational vulnerability from the Operational vulnerability module in the Operational Resilience Workspace.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

When an operational vulnerability is reported, it is opened in the **New** state, marking the beginning of its initial review.

Users of the operational vulnerability are listed in the Assignment section on the form and can find their tasks if their names are listed on any of the following fields:

-   The Operational vulnerability record is assigned to the person who reports the vulnerability. The name of the person is listed in the **Requester** and **Analyst** fields. The analyst receives a notification when the vulnerability is assigned to them.
-   Typically, Operational Resilience administrators and Operational Resilience managers are part of the assignment group. The names of the groups are listed in the **Assignment group** field.
-   The requester can report the vulnerability on behalf of someone by selecting the person in the **Requested on behalf of** field.
-   The requester can add one or more approvers of the vulnerability in the **Approvers** field. The approvers receive a notification when the vulnerability is moved to the **Pending approval** state.
-   The requester can add one or more persons on the watchlist of the vulnerability in the **Watchlist** field.
-   The requester of the vulnerability and persons on the Watchlist and Requested on behalf of fields do not receive any notifications when a vulnerability is assigned to them.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities**.

2.  Select **New**.

3.  Enter the name and description of the Operational vulnerability record.

4.  On the Vulnerability New record form, fill in the fields.

    To view more information on the fields, see the [Create New Operational vulnerability form](../reference/create-new-op-vul-form.md).

5.  Select the treatment decision for the vulnerability.

    To make decisions for the treatment, you can use one of the following choices:

    -   **Accept**
    -   **Avoid**
    -   **Mitigate**
    -   **Transfer**
    -   **None**
6.  Select **Submit**.

    The Operational vulnerability record is assigned to the requester and analyst by default. The requester is a person who reports the vulnerability. An Analyst is a person who analyzes and works on the vulnerability.

7.  To update the state of the vulnerability, select **Update state**.

8.  To save the vulnerability, select **Save**.

9.  To view the relationship data for the vulnerability, select **360-degree view**.

10. To start a sidebar discussion, select **Discuss**.

    |Field|Description|
    |-----|-----------|
    |**Add participants**|Add the participants to the discussion about the vulnerability. You can add the users that have access to the record.|
    |**Include a brief message for participants**|Type a message for the participants.|
    |**Select __Start Discussion__.**|Start a sidebar discussion about the vulnerability with the participants.|

    The sidebar discussion is displayed as shown in the example.

    ![Sidebar.](../image/op-vul-sidebar.png)

    The New discussion created is also displayed in the Activity panel of the record.

11. To export the details of the vulnerability in PDF format, select **Export PDF**, select the template to be exported such as Operational Vulnerability Template, and select **Export**.

    The PDF report is generated and it is displayed in the Attachments section of the Activity panel in the record.

12. To create an email draft of the vulnerability record, select **Compose Email**, enter the details, and select **Save**.

    You can enter the details of the email draft in the record. You can save and view the email details, email draft recipients, and email draft attachments in the respective related lists.

13. To delete the vulnerability record, select **Delete**.


