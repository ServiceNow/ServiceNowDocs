---
title: Example: Binding alerts to non-host CIs
description: Bind alerts to an application service \(a non-host CI\) using event rules and event field mapping. This example demonstrates how to achieve this by leveraging the IP address associated with the service.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Example: Binding alerts to non-host CIs

Bind alerts to an application service \(a non-host CI\) using event rules and event field mapping. This example demonstrates how to achieve this by leveraging the IP address associated with the service.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When an event is generated, it may not always include the exact name of the Application Service it affects. Instead, it might provide details such as an IP address. In this example, suppose application services are identified by IP addresses. Since the goal is to bind the alert to an Application Service, you need to determine which service name corresponds to the given IP address.

To achieve this, follow these steps:

1.  Match the correct Application Service: Override the default binding and select **Binding Type** as **CI field matching**. The binding process needs to associate the alert with an Application Service, not a host. In the event rule, set the **CI Type** to **Application Service** so that the system searches for the service in the Application Service table \(cmdb\_ci\_service\_auto\).
2.  Extract the IP address from the event description: The event might contain a message like `Service is down. IP address is: 196.1.1.24`. You need to extract the IP address from this description for further processing.

    ![Extract IP address from the Description field.](../image/em-example-event-msg.png)

3.  Translate the IP address into a service name using Event Field Mapping: Use Event Field Mapping to look up the extracted IP address in the CMDB and find the associated application service. Once a matching service is found, its name is stored in the **Name** field of the event.
4.  Bind the alert to the correct Application Service: If the service name is identified, the alert's CI is populated with that service.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Events**.

2.  Open the specific event for which you want to create an event rule.

3.  Select **Create Event Rule**.

    The new event rule page opens. Some fields in the event rule are populated based on the event record data, such as the Source field value.

4.  In the **Event Rule Info** tab, in the **Name** field, enter `application service binding`.

5.  Select the **Binding** tab.

    In this tab, you select the CI type as a service \(non-host\) instead of a host because the goal is to bind alerts to an Application Service, not to a physical or virtual machine.

6.  Perform the following steps:

    1.  Select the **Override default binding** check box.
    2.  In the **Binding type** field, select **CI field matching**.
    3.  From the **CI type** list, select **Application Service**.
    ![In the Binding tab, the CI type is selected as Application Service.](../image/em-example-binding-ci-type.png)

7.  Select the **Transform and Compose Alert Output** tab.

    In this tab, you extract the IP address of the application service into a manually created field. Extracting the IP allows the system to look up the corresponding service in the Application Service table \(cmdb\_ci\_service\_auto\). Without extracting the IP, the system wouldn’t be able to determine which Application Service the event belongs to, making it difficult to bind the alert correctly.

8.  Perform the following steps:

    1.  Clear the **Node** field.

        When an event is processed, it often comes with multiple fields of information. The **Node** field typically contains the host or device name. However, since the goal is to bind the alert to an Application Service rather than a host, clearing the **Node** field ensures that the system focuses on identifying the correct service instead of mistakenly associating the alert with a host CI.

        ![Clear the Node field.](../image/em-example-clear-node.png)

    2.  Under **Event Input** &gt; **Event Raw Info**, select **Description**.

        The Edit Regex Expressions window opens.

    3.  In the Mark Expressions section, select the IP address, manually enter a field name \(e.g., service\_ip\_address\), and press Enter to save it.

        ![A field is created manually to store the IP address.](../image/em-example-regex-field.png)

    4.  Select **Done**.

        The IP address is extracted into the newly created **service\_ip\_address** field, which is added to the **Additional info** field of the alert. This allows it to be used later to identify the corresponding Application Service.

9.  Select **Submit** in the event rule to save your changes.

10. Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Field Mapping**.

    In Event Field Mapping, configure the extracted IP address to map it to the corresponding service name. The event provides only an IP address, but alerts need to be associated with a service name \(not just an IP\). The system needs to map this IP to its corresponding Application Service so that teams can easily identify the impacted service.

11. Select **New**.

    The Event Field Mapping window opens.

12. Perform the following:

    ![Configure the extracted IP address to map it to the corresponding service name.](../image/em-example-event-field-mapping.png)

<table id="table_ljx_hw1_q2c"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name of the mapping.Example: mapping from ip\_address to service name.

</td></tr><tr><td>

Source

</td><td>

Enter `AWS`.**Note:** The source is the same as the one in the Events record.

</td></tr><tr><td>

Mapping type

</td><td>

Select **Map field and transform value \(Single field\)**

</td></tr><tr><td>

Source field

</td><td>

Enter `service_ip_address`.

</td></tr><tr><td>

Target field

</td><td>

Enter `name`.The target field value is the column name in the Application Service table \(cmdb\_ci\_service\_auto\) where the source field value is searched.

</td></tr><tr><td class="sub-head" colspan="2">

Transform value pairs

</td></tr><tr><td>

From value

</td><td>

196.1.1.24

</td></tr><tr><td>

To value

</td><td>

Corp E-mail

</td></tr></tbody>
</table>13. Select **Submit**.

    The system extracts the IP address of the service from the event and stores it in the **service\_ip\_address** field. Since the Application Service table \(cmdb\_ci\_service\_auto\) does not have a column for searching by IP address, the Transform value pairs feature is used to map the IP address to a name—in this case, Corp E-mail and and saves it in the **name** field within the **Additional info** field of the alert. The **Target field** specifies where to search for the Corp E-mail in the Application Service table. The system looks for Corp E-mail in the **name** column of the Application Service table \(cmdb\_ci\_service\_auto\). If a match is found, the alert is bound to the corresponding Application Service.

    ![Binds alerts to service.](../image/em-example-result.png)


