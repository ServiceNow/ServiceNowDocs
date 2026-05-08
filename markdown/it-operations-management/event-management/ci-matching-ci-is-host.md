---
title: Bind host CIs using CI field matching
description: When CI Field Matching is used and the CI is a host, the Node value from the alert is used for binding. The system compares the Node with attributes like Name, FQDN, IP, or MAC Address in the CMDB to find a match. This ensures that alerts are correctly linked to the corresponding host CI.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Bind host CIs using CI field matching

When CI Field Matching is used and the CI is a host, the Node value from the alert is used for binding. The system compares the Node with attributes like Name, FQDN, IP, or MAC Address in the CMDB to find a match. This ensures that alerts are correctly linked to the corresponding host CI.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When an event enters the system, key field like **Node** is available on the event record. The **Node** field generally represents the name of the server. In CI there is no field like **Node**. However, the value of **Node** from the event is compared with different values in the host CI such as Name, Fully qualified domain name \(FQDN\), IP, or MAC Address. If a match is found, the alert is linked to the corresponding CI. This is the default binding of alerts to CIs. In this binding, the CI must be a host. Host CIs include Computers, OS, Switches, Routers—essentially any CI type or class that extends the \[cmdb\_ci\_hardware\] table.

There may be cases where no match is found because the column names in the event record and the table differ for the same item. In such cases, you can manually create an additional key-value pair with a name matching the table column, ensuring the matching process continues successfully. For information on how to create a manual field, see [Bind CIs using CI field matching and handling column name differences](ci-matching-manual-field.md).

**Note:** Even if the node successfully binds the alert with the CI, event rules further determine how the binding occurs.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New** and complete the required fields of the event rule.

3.  Select the **Binding** tab.

4.  Select the **Override default binding** check box.

5.  In the **Binding type** field, select **CI field matching**.

    ![Binding type is CI field matching](../image/em-ci-field-matching-host.png)

6.  In the **CI type** field, select the appropriate type of hardware component \(such as a server, router, or storage device\) that the CI type represents.

    The **CI type** determines the specific CMDB table where the system searches for the matching CI. For example, if the **CI type** is **Network Adapter**, the system searches in the \[cmdb\_ci\_network\_adapter\] table.

7.  Select **Submit**.

    **Note:** You can also use the Service Operations Workspace to define binding rules. For more information, see [Create Enrich automation](../../service-operations-workspace-itom/task/enrich-alert-sow-itom.md).


**Related topics**  


[Bind non-host CIs using CI field matching](ci-matching-ci-non-host.md)

