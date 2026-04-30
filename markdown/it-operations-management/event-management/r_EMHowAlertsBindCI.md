---
title: Alert binding to CIs with event rules
description: When alerts are associated with CIs, the task of remediation is simplified. During alert generation, Event Management uses event rules and other mechanisms to automatically bind alerts to a CI information from the CMDB. For tracking purposes and remediation, the alert shows information about the CI that caused the event.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Alert binding to CIs with event rules

When alerts are associated with CIs, the task of remediation is simplified. During alert generation, Event Management uses event rules and other mechanisms to automatically bind alerts to a CI information from the CMDB. For tracking purposes and remediation, the alert shows information about the CI that caused the event.

## Alert binding process flow

Alerts bind to CIs based on the following process flow:

1.  When an event arrives, Event Management checks the node or CI identifiers.
2.  If no node exists, the generated alert can bind to the CI using the alert **Type**, **Additional information**, or **Configuration item** identifier fields.
3.  If the event has a node value, search for a valid host.
4.  If the event has a host and a CI type, try to bind to a device CI.
5.  If the event has a host, try to bind to the application CI.

![How alerts bind to CIs](../image/EMEventBinding.png "How alerts bind to CIs")

The event can contain the binding process flow in its **Processing Notes** field.

By default, events do not bind to CIs with a specified status, such as Retired. To enable binding events to these CIs, set the **evt\_mgmt.ignore\_retired\_cis\_in\_binding** property to **false**.

To specify the CI statuses to be included in the **evt\_mgmt.ignore\_retired\_cis\_in\_binding** property, add the relevant status numbers to the **evt\_mgmt.install\_status\_list\_to\_ignore\_in\_binding** property, as per the following table:

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

**Note:** When adding more than one status, separate each status number with a comma.

## Tracking and remediation

Alerts can be bound to CIs from the CMDB for tracking purposes and remediation. Event Management uses event rules and various mechanisms to automatically bind CIs to alerts. When information from an event populates a field with a value, the value either originates from the event source or from event rules. This enhances remediation, functionality, and integration with other ITOM products.

## Binding to an application running on a specific host

If the event is specific to an application type, use the following steps to bind alerts to a specific application:

1.  Use the procedures in the [Bind alerts to a CI running on a host using CI identifiers](../task/t_EMBindHost.md) topic.
2.  Create an event rule with a filter that captures events on the application type you want.
3.  In the event rule, select **Binding**. ![Event Management binding](../image/event-rule-binding-active.png)
4.  Click **Override default binding**.
5.  In the Binding Type field, select either **CI's Identification** or **CI field matching**.
    1.  For **CI's Identification**, specify the **Class**. ![Event Management binding](../image/event-rule-binding-ci.png)
    2.  In the Criterion attributes field, specify `name and sys_class_name`.

        ![Event Management binding](../image/event-rule-binding-class-id.png)

    3.  In the **Name Add Value** field, specify the required name.
    4.  In the **Container level 1** area, specify the required values.
    5.  If further container level fields appear, specify the required values.

-   For **CI field matching**, specify the required **CI Type**.
-   In the binding process, after the host is found, the algorithm matches all **additional\_info** attributes that have the same name as CI fields for that CI type. If the match is successful, the event is bound to the CI.
-   If more than one matching application is found on the host, the alert is bound to the host and not to the application.

Where there is no **CI Type**, for example, when binding alerts to an SQL server application when the CPU on sqlServer.exe is over 90%, do the following:

-   Populate the **Node** field in the event with the **CI name**, **FQDN**, **IP**, or **MAC** address value. The bind is successful even if the host has more than one IP address or MAC address.
-   If you want to use a unique identifier that is not one of those previously mentioned, populate the event rule **CI Identifier** \(ci\_identifier\) field with one or more unique identifiers of the CI. This field should be in JSON format. For example, to use a unique identifier that is not one of those previously mentioned, add a **CI Identifier** \(ci\_identifier\) filter field with one or more unique identifiers of the CI. If the host CI is **VMWare VM**, and it has a field called **MOID**, use the JSON format and specify: `{"moid":"<CI moid>"}`
-   Create an event rule with an event match field which maps the process name to the mapping variable *sa\_process\_name*. In this case, do not use the **CI type**.

## Binding procedures

Use the procedures in these topics to bind alerts.

-   **[Bind alerts to a CI running on a host using CI identifiers](../task/t_EMBindHost.md)**  
Create an event rule to bind alerts to a CI running on a host.
-   **[Bind alerts to a specific host CI](../task/t_EMBindDevice.md)**  
Create an event rule to bind alerts to the correct device CI. An incoming event from a device CI can bind to an alert based on event rule transform information. However, first identify the host CI that the device is running on.
-   **[Bind alerts to non-host CIs](../task/t_EMBindServiceCI.md)**  
Bind an incoming event from a discovered application services or alert group to an alert, based on an event rule and the corresponding event field mapping. The event field mapping requires a URL or the port number and corresponding IP address for each service or alert group.
-   **[Bind alerts to application CIs](../task/t_EMBindApplication.md)**  
Create an event rule to bind alerts to the host CI and also to the application CI. An incoming event from an application CI can bind to an alert based on event rule transform information.
-   **[Bind alerts to CIs using event field mapping](../task/bind-ci-event-mapping.md)**  
Instead of creating separate event rules for each CI you want to bind to an alert, you can use event field mapping to bind an alert to multiple event CIs.
-   **[Trigger alert binding to a CI](../task/t_EMManuallyBindAlertCI.md)**  
Trigger a new alert to manually bind an alert to a CI.

**Parent Topic:**[Event rules](../concept/create-event-rules.md)

**Related topics**  


[Event field format for event collection](../concept/c_EMIntegrateRequirementEvent.md)

