---
title: SRM alert states
description: Alert can be in a few different states depending on how they are acted on.If changing states starts to do something then use this topic. Otherwise it's not necessary.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Reliability Management reference, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# SRM alert states

Alert can be in a few different states depending on how they are acted on.

An alert is created in SRM when a third-party monitoring tool has an event. Alerts are manually assigned. An alert is one of four states. You can edit actions from either the Alerts list or the Alert form. Use the **Save** button in the form to keep any changes you've made. Changes to Alerts in the list view are automatically saved.

**Note:** You can acknowledge and assign an alert in any state.

<table id="table_hsr_mfq_hbrr"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open

</td><td>

State on alert creation. From this state you can acknowledge and set to:-   **Flapping**

Flapping occurs when the event source continues to generate events even after its associated alert has been closed. See [Configure alert flapping](../../event-management/task/t_EMConfigAlertStateFlapDetect.md) for more information on event flapping.

-   **Closed**

Closes the alert.


</td></tr><tr><td>

Reopen

</td><td>

From this state you can acknowledge and set to:-   **Open**

Sets the alert to the **Open** state.

-   **Flapping**

Flapping occurs when the event source continues to generate events even after its associated alert has been closed.

-   **Closed**

Closes the alert.


</td></tr><tr><td>

Flapping

</td><td>

Flapping occurs when the event source continues to generate events even after its associated alert has been closed. From this state you can set to:-   **Open**

Sets the alert to the **Open** state.

-   **Reopen**

Reopens the alert.

-   **Closed**

Closes the alert.


</td></tr><tr><td>

Closed

</td><td>

From this state you can set to:-   **Open**

Sets the alert to the **Open** state.

-   **Reopen**

Reopens the alert.

-   **Flapping**

Flapping occurs when the event source continues to generate events even after its associated alert has been closed.


</td></tr></tbody>
</table>**Parent Topic:**[Service Reliability Management reference](service-reliability-management-reference.md)

