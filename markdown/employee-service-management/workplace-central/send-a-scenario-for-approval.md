---
title: Send a scenario for approval
description: After publishing the scenario, send your scenario for approval to workplace managers of your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/send-a-scenario-for-approval.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 5
breadcrumb: [Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Send a scenario for approval

After publishing the scenario, send your scenario for approval to workplace managers of your organization.

## Before you begin

Ensure the following:

1.  [Create a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)
2.  [Publish a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/publish-a-scenario.md)

Role required: sn\_wsd\_spcmgmt.space\_planner

## About this task

After you publish a scenario, send the scenario for approval. The scenario will be sent for approval to the workplace managers for approval. If there are multiple approvers for a scenario, the approval or rejection received from the workplace manager who performs it at first, is considered. You can view your approval-related details in the **Approver** tab. When a scenario is sent for an approval, the state of the scenario changes from Published to Awaiting approval and you cannot edit the scenario.

## Procedure

1.  Navigate to any one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  On the left pane, select **Space Optimization** icon \(\[Omitted image "space-optimization-icon.png"\] Alt text: Space optimization icon.\).

    The Space optimization dashboard opens.

3.  Open the scenario that you want to send for approval.

    Follow any one of the following paths.

<table id="choicetable_vtv_5nj_3vb"><thead><tr><th align="left" id="d388385e159">

Path

</th><th align="left" id="d388385e162">

Action

</th></tr></thead><tbody><tr><td id="d388385e168">

**From the Scenarios list section**

</td><td>

1.  At the end of the scenarios list, click **View all**.

A list of all the scenarios created in the application are displayed.

2.  Select the scenario that you want to send for approval.

You can use the search and filter options on the list.

</td></tr><tr><td id="d388385e193">

**From the Buildings list section**

</td><td>

1.  Select the building of which you want to send a scenario for approval.

The stack plan view of the building opens.

2.  Select **Related scenarios**.
3.  Select the scenario that you want to send for approval.


</td></tr></tbody>
</table>    The stack plan of the selected scenario opens.

4.  Review the scenario.

    Refer to [Review a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/review-a-scenario.md).

5.  If the scenario is not published, then publish the scenario.

    Refer to [Publish a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/publish-a-scenario.md).

6.  After publishing, click **Send for approval** to send the scenario for approval.

7.  Open the **Approver** tab to view your approver-related details.

8.  Depending on the state of the scenario after sending for approval, do the following:

    -   Rejected: If the scenario is rejected by the approver, then the state of the scenario changes to Rejected.

        To view the rejection details, do the following:

        1.  Select the **Approver** tab.
        2.  Search for **Rejected** state.

            Use the filter option to view Rejected state.

        3.  In the **Comments**, view the comments given by the approver.
        4.  Select the **Stack plan** tab to implement the changes suggested by the approver.
        5.  After making the changes, click **Save**.
        6.  After saving the scenario, to send the scenario for approval again, click **Send for approval.**

            The state of the scenario is again changed to Awaiting approval and you can no longer edit the scenario.

            If the scenario is rejected, you can send a scenario for approval multiple times until it is approved.

    -   Approved: If the scenario is approved, then the state of the scenario changes to Approved. You can no longer edit the scenario after it is approved.
9.  After the scenario is approved, deploy the scenario.

    Refer to [Deploy a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).


## Result

The scenario approval process is completed.

## What to do next

[Deploy a scenario](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

**Parent Topic:**[Working with Space Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/working-with-space-optimization.md)

**Related topics**  


[Create a scenario]()

[Viewing or editing a scenario]()

[Review a scenario]()

[Publish a scenario]()

[Change owner of a scenario]()

[Deploy a scenario]()

[View scenario change details]()

[Create a copy of an existing scenario]()

[View or edit space allocations of a building]()

[Work on a space assist request]()

[Map based space administration]()

