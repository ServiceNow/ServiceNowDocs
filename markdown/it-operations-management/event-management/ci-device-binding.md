---
title: Bind alerts to a specific device
description: Bind each alert directly to the originating device to establish a clear source of impact. This ensures accurate troubleshooting, reduces noise from unrelated alerts, and helps teams focus on resolving the right issue faster.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Bind host CIs using CI field matching, Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Bind alerts to a specific device

Bind each alert directly to the originating device to establish a clear source of impact. This ensures accurate troubleshooting, reduces noise from unrelated alerts, and helps teams focus on resolving the right issue faster.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

In IT environments, multiple devices like switches have many smaller components, such as ports. When something goes wrong, it's not enough to just say the switch has an issue—the system needs to pinpoint exactly which port is causing it. Binding alerts to the specific port that triggered the issue allows teams to act faster and fix the real issue without wasting time checking the entire switch or unrelated components.

The following example procedure shows the alert binding configuration for a switch named IP-Switch-1, ensuring alerts target the correct port. The event rule setup starts by enabling the **Override default binding** option and selecting **CI field matching** as the **Binding type**. Choosing **Switchport** as the **CI type** instructs the system to bind alerts to individual ports. The Binding Device Map defines how the system links the switch \(cmdb\_ci\_ip\_switch\) to its ports \(dscy\_switchport\) using the cmdb\_ci reference field. This map guides the binding logic. Under **Configuration** &gt; **Network** &gt; **Switches**, selecting **IP-Switch-1** reveals its switchports and interface names. When an incoming event includes a matching interface name in the **Additional information** field, the system binds the alert directly to the correct port—ensuring precise and meaningful alert context.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New**.

    ![List of event rules](../image/ci-device-map-event-rule.png)

3.  Select the **Binding** tab.

4.  Select the **Override default binding** check box.

5.  In the **Binding type** field, select **CI field matching**.

6.  In the **CI type** field, select **Switchport**.

    The **CI type** determines the specific CMDB table where the system searches for the matching CI.

    ![Binding and CI type](../image/ci-device-map-binding-type.png)

7.  Navigate to **All** and search `em_binding_device_map.list`.

    The Binding Device Maps page opens. Here the column values **From ci type** is mapped to **To ci type** using the **Mapped column**. For example,**cmdb\_ci\_ip\_switch** is mapped to the Switchport \[dscy\_switchport\] table using the reference field **cmdb\_ci**.

    ![Binding device maps](../image/ci-device-binding-map.png)

8.  Navigate to **All** and search `switches` and select **Configuration** &gt; **Network** &gt; **Switches**.

    The IP Switches page opens.

    ![IP switches page](../image/ci-device-map-ip-switches.png)

9.  Select **IP-Switch-1** to view the details page.

10. Select the **Switchports** tab.

11. Navigate to **All** &gt; **Event Management** &gt; **All Events**.

12. Select the event with **Node** value as **IP-Switch-1**.

    ![Additional information field of the event](../image/ci-device-map-addi-info.png)

    In the following image, you can see the processing notes indicating that the binding has occurred between the alert and the matching device.

    ![Processing Notes of the event](../image/ci-device-map-processing-notes.png)


