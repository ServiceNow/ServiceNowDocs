---
title: Binding process flow
description: Learn the process of binding Configuration Items \(CIs\) to alerts. This includes handling event arrival, binding alerts using available fields when no node is present, and searching the CMDB for matching hosts. It also explains linking alerts to CIs based on host and CI type detection.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Binding process flow

Learn the process of binding Configuration Items \(CIs\) to alerts. This includes handling event arrival, binding alerts using available fields when no node is present, and searching the CMDB for matching hosts. It also explains linking alerts to CIs based on host and CI type detection.

## CI binding to alerts: Flow diagram

![How alerts bind to CIs](../image/EMEventBinding.png)

## Process of linking CIs to alerts

1.  Event Arrival: When an event is received, Event Management checks for node or CI identifiers.
2.  Is Node Value Present?
    -   Yes: If a node value is provided, Event Management searches the CMDB for a matching host.
    -   No: If no node is found, the system attempts to bind the alert using other available details, such as:
        -   Alert Type
        -   Additional Information
        -   CI Identifier
3.  Host and CI Type Detection:
    -   Both Found: If both a host and CI type are identified, the alert is linked to the corresponding device CI.
    -   Host Only Found: If only a host is identified, the system links the alert to an application CI.

## Additional Considerations

-   Event Processing Notes: The event can include the binding process flow in its **Processing Notes** field, providing insights into the binding actions.
-   Binding to Retired CIs: By default, events do not bind to CIs with a Retired status. To enable binding to these CIs, set the **evt\_mgmt.ignore\_retired\_cis\_in\_binding** property to false.
-   Specifying CI Statuses for Binding: You can configure the **evt\_mgmt.install\_status\_list\_to\_ignore\_in\_binding** property by specifying CI status numbers to control which CIs are considered for binding. For example:

    |Status Number|Status|
    |-------------|------|
    |1|Installed|
    |2|OnOrder|
    |3|InMaintenance|
    |4|PendingInstall|
    |5|PendingRepair|
    |6|InStock|
    |7|Retired|
    |8|Stolen|
    |100|Absent|


**Note:** To specify multiple statuses, separate each status number with a comma.

