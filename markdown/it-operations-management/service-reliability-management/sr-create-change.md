---
title: Manually create an SRM change task
description: Create a change task to implement a controlled process for modifying approved and supported actions for SRM.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Manually create an SRM change task

Create a change task to implement a controlled process for modifying approved and supported actions for SRM.

## Before you begin

For general information on Change requests, see [Using Change Management](https://www.servicenow.com/docs/access?context=using-change-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

Role required: srm\_manager, srm\_responder, or srm\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  Select **Reliability tasks** \(![Reliability tasks icon](../image/icon-sr-reliability-tasks.png)\).

3.  Select the **Changes** tab.

4.  Select **New** from the **Changes** list header.

5.  In the **Select a change** window, search for a change record or select an SOW change creation page card to select the type of change request.

6.  Select **Next**.

7.  In the form Details tab, fill in the fields on the **Change request**, **Impact**, **Assignment**, **Planning**, **Schedule**, **Notes**, and **Closure information** forms.

    For more information, see [Create change request forms](../reference/sr-create-change-request-form.md).

8.  Select **Assign to me**.

9.  Select **Save**.

    The change request is created and a **Related Records** tab appears for the request.

10. You can take the following steps in **State** workflow.

    If the change request requires approval, you’ll see the **Request approval** button. Select **Request approval** and **State** moves to **Assess**. See [Approve a change request for SRM](sr-approve-change-req.md) for instructions on approving a change request.

    If the change request is pre-approved or doesn’t require approval, you can move the **State** to **Scheduled**.

    Once approved and scheduled, you can select **Implement** to put the change request into action.

    Once implemented, you only after reviewing the details on the change request, select Review. The change request is moved to the **Review** state.

    **Note:** All open change tasks are set to **Canceled**.

    For more information on **State** in Change requests, see, [SRM change request states](../concept/sr-change-request-states.md)


**Parent Topic:**[Working with SRM reliability tasks](sr-work-reliability-tasks.md)

