---
title: HR Service Delivery with Ultimate Kronos Group
description: With the HR Service Delivery with Ultimate Kronos Group application, provide employee assistance through conversations in the Virtual Agent conversational \(client\) interface. Enable employees to view their accrual leave balances, schedules, and upcoming shifts from the Ultimate Kronos Group application in ServiceNow Employee Center.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# HR Service Delivery with Ultimate Kronos Group

With the HR Service Delivery with Ultimate Kronos Group application, provide employee assistance through conversations in the Virtual Agent conversational \(client\) interface. Enable employees to view their accrual leave balances, schedules, and upcoming shifts from the Ultimate Kronos Group application in ServiceNow Employee Center.

Key features include:

-   Build conversations that are based on keywords that an employee enters.
-   Apply Natural Language Understanding \(NLU\) models, which enable the Virtual Agent to pick utterances for understanding, processing, and responding to what employees are saying during a conversation.

## Application setup

First, you must activate the HR Service Delivery Integration with the Ultimate Kronos Group \[sn\_hr\_ukg\] application from the ServiceNow Store. Next, you must set up [HR Service Delivery Integration with Ultimate Kronos Group application](../task/set-up-ukg.md).

## HR Service Delivery with Ultimate Kronos Group overview

After the activation and setup of HR Service Delivery Integration with Ultimate Kronos Group is complete, the HR Service Delivery with Ultimate Kronos Group responds to what employees or managers are saying during a conversation, and allows employees to view the following details from the Ultimate Kronos Group application in the Employee Center Employee Service Center.

## Topics accessible to employees

As an employee, you can view your accrual balances, work hours, list of punches, schedules, time-off requests, and upcoming shifts using the Virtual Agent.

-   **Retrieve My Accrual Balance**

    You can view the aggregate of accrual leaves balance \(by type\) by selecting the **Retrieve My Accrual Balance \(Template\)**. If the [NLU model](../task/nlu-ukg-model.md) is trained, you can ask a question in the chat \(for example, show my sick leaves\) and view the balance of a single type of leave.

-   **Retrieve My Hours Worked**

    You can view the number of hours worked for a given period by selecting the **Retrieve My Hours Worked \(Template\)** and choosing a symbolic period.

-   **Retrieve My List of Punches**

    You can view the list of punches by selecting the **Retrieve My List of Punches \(Template\)** and choosing a symbolic period.

-   **Retrieve My Schedule**

    You can view the work schedule for a given period by selecting the **Retrieve My Employee Schedule \(Template\)** and choosing a symbolic period. If the [NLU model](../task/nlu-ukg-model.md) is trained, you can ask a question in the chat \(for example, my work schedules of the previous pay period\) and view the work schedules for that symbolic period.

    You can also view your schedule location for three days from the current day.

-   **Retrieve My Time Off Requests**

    You can view the status of the time off requests by selecting the **Retrieve My Time off Requests \(Template\)** and specifying an end date.

    **Note:** Ensure that the selected time-off period ranges for 15 days from the start date \(current day\).

-   **Retrieve My Upcoming Shift**

    You can view the next upcoming shift by selecting the **Retrieve My Upcoming Shift \(Template\)**. If the [NLU model](../task/nlu-ukg-model.md) is trained, you can ask a question in chat \(for example, show my shifts\) and directly view the next upcoming shift.

    You can also view your location along with the shift date and time.


## Topics accessible to managers

As a manager, you can access and view the locations, schedules, and time-off requests of your team using the Virtual Agent.

**Note:** The templates are visible only to a user with the manager role.

-   **Reportee's Location Today**

    You can view the location of a reportee in the team \(for today\) by selecting the **Reportee’s Location Today \(Template\)**.

-   **Reportee's Schedule Changes**

    You can view the schedule change requests such as shift cover, shift swap, availability change, open shift, and self-schedule. Follow the onscreen instructions for more information on the schedule changes.

    **Note:** You can view the change requests in offered, invalidated, or pending state.

-   **Reportee's Time Off Requests**

    You can view the pending time off requests from your team for a specified time period. You can check the requests from the individual team members or the entire team.


## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Configure ![Plan and configure your implementation.](../../../common/image/icon-set-up.png) Plan and configure your integration.](../task/set-up-ukg.md)

</td><td>

[Reference ![Get details about components like fields, tables, and properties.](../../../common/image/icon-reference.png) Get details about components like fields, tables, and properties.](../reference/ref-hrsd-ukg.md)

</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>