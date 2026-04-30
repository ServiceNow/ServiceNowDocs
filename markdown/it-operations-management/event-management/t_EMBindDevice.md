---
title: Bind alerts to a specific host CI
description: Create an event rule to bind alerts to the correct device CI. An incoming event from a device CI can bind to an alert based on event rule transform information. However, first identify the host CI that the device is running on.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Alert binding to CIs with event rules, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Bind alerts to a specific host CI

Create an event rule to bind alerts to the correct device CI. An incoming event from a device CI can bind to an alert based on event rule transform information. However, first identify the host CI that the device is running on.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

In the binding process, after the host is found, the algorithm matches all **additional\_info** attributes that have the same name as CI fields for that event type. If the match is successful, the event is bound to the CI. If more than one matching device is found on the host, the alert is bound to the host and not the application. Use the following steps to bind alerts to a specific device:

-   When binding alerts to a host, such as a computer, switch, or router CI:
    -   Populate the **Node** field in the event with the **CI name**, **FQDN**, **IP**, or **MAC** address value. The bind is successful even if host has more than one IP address or MAC address.
    -   If you want to use a unique identifier that is not one of the four mentioned in the preceding point, populate the event rule **CI Identifier** \(ci\_identifier\) field with one or more unique identifiers of the CI. This field should be in JSON format. For example, to use a unique identifier that is not one of the four mentioned above, add a **CI Identifier** \(ci\_identifier\) filter field with one or more unique identifiers of the CI. If the host CI is **VMWare VM**, and it has a field called **MOID**, use the JSON format and specify: `{"moid":"<CI moid>"}`

        **Note:**

        The node field must be either empty or non-resolvable. If the node field is resolvable, the ci\_identifier is ignored.

-   Create an event rule with a filter that captures events on the device type you want. In the event rule, select the **Transform** check box and select the appropriate **CI Type**:

    |Device to bind|CI Type|
    |--------------|-------|
    |File System|cmdb\_ci\_file\_system|
    |Port|cmdb\_ci\_network\_adapter|
    |Storage Device|cmdb\_ci\_storage\_device|
    |Volume|cmdb\_ci\_storage\_volume|


## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New** and fill in the appropriate fields of the event rule.

3.  Select the **Binding** tab.

4.  Select **Active**.

5.  From the **CI type** list, select the device that is used in the filter condition.

    For example, if you build a filter condition for a port, select **Port**.

    |Device to bind|CI type|
    |--------------|-------|
    |File System|cmdb\_ci\_file\_system|
    |Port|cmdb\_ci\_network\_adapter|
    |Storage Device|cmdb\_ci\_storage\_device|
    |Volume|cmdb\_ci\_storage\_volume|

6.  In the Event Match Fields section, specify any **Additional information** mappings.

7.  Select **Submit**.

8.  To bind to custom device types, configure the alert binding to a process and add the custom device type to the Process to CI Type Mapping \[em\_binding\_process\_map\] table.


## Example

Example showing binding to a specific device using CI field matching to bind to the following string values in the **Additional information** field of an event: "file\_system":"ext2", "mount\_point":"mp1".

![Event rule binding toCI example additional-info](../image/event-rule-binding-to-ci-example-additional-info.png)

1.  Navigate to **Event Management** &gt; **Rules** &gt; **Event Rules**.
2.  Select **New**, and in **Event Rule Info**, fill in the appropriate fields of the event rule.

    ![Event rule binding to CI example](../image/event-rule-binding-to-ci-example.png)

3.  Select the **Binding** tab.

    1.  Select **Override default binding**.
    2.  In the **Binding type** field, select `CI field matching`.
    3.  In the **CI type** field, select `File System`.
    ![Binding rule example](../image/binding-rule-example.png)

4.  Select **Save**.

In the Binding Device Maps \[em\_binding\_device\_map\] table, ensure that File System is mapped to cmdb\_ci\_file\_system.

![Event rule binding to CI example device map](../image/event-rule-binding-to-ci-example-device-map.png)

In the File Systems \[cmdb\_ci\_file\_system\] table, ensure that the required values exist, for example, name1 and name2, as depicted in the following image.

![Event rule binding to CI example file system](../image/event-rule-binding-to-ci-example-file-system.png)

The result of the binding performed by the "test binding" event rule is shown in the **Processing Notes** field of the event.

![Event rule binding to CI example-processing notes](../image/event-rule-binding-to-ci-example-processing-notes.png)

**Parent Topic:**[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

**Related topics**  


[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

