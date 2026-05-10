---
title: Bind alerts to CIs using CI identification
description: Bind alerts to specific applications on hosts using event rules to ensure accurate tracking and to improve issue resolution speed—leading to efficient remediation and better alignment of alerts with the right resources.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Overriding default binding, Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Bind alerts to CIs using CI identification

Bind alerts to specific applications on hosts using event rules to ensure accurate tracking and to improve issue resolution speed—leading to efficient remediation and better alignment of alerts with the right resources.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Before going through the procedure, let’s first understand how this binding works with an example. Suppose an out-of-the-box event rule, SCOM Metrics – IIS WebServer, generates an alert for a Microsoft IIS Web Server running on a host. Instead of binding the alert to just the host machine, you want it to be associated with the specific application \(IIS Web Server\) where the issue occurred. Here’s how the system ensures accurate binding.

Let's say in the **Binding** tab, the **Class** and **Container Level 1** are defined along with their respective attributes, as shown in the image.

![The Binding tab where Class and Container is defined.](../image/em-ms-iis-webserver-binding.png "Binding tab")

The binding procedure follows these steps:

1.  Identifying the Host \(Container Level 1\)

    Since the Microsoft IIS Web Server runs on a host \(in this case Hardware\), the system first locates the host, which is defined as **Container Level 1**. The name field is used to identify the host, and its value is taken from the **Node** field of the event. Using this name, the system searches the CMDB to find a matching host CI.

2.  Identifying the Microsoft IIS Web Server CI on the Host

    Once the host is identified, the system looks for a Microsoft IIS Web Server CI under that host with the following attributes:

    -   name = ci\_name
    -   sys\_class\_name = cmdb\_ci\_microsoft\_iis\_web\_server
    Here, ci\_name is derived from the key-value pair defined in the **Transform and Compose Alert Output** tab of the event rule. Assume that in the **Transform and Compose Alert Output** tab of the event rule, the **Manual attributes** check box is selected and the following key-value pair is already added:

    -   **Field Name**: `ci_name`
    -   **Field Value**: `Microsoft IIS Server@${node}`
    This ensures that `ci_name` appears in the **Additional information** field of the alert and is used when configuring the attribute field of the CI class.

    ![Manual attribute for an alert.](../image/em-ms-iis-webserver-attribute.png "Transform and Compose Alert Output tab")


If a matching Microsoft IIS Web Server CI is found on the identified host, the alert is bound to the correct application CI rather than just the host. This ensures more precise incident tracking and resolution, linking the alert to the actual service affected instead of only the machine it runs on.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New** and complete the required fields of the event rule.

3.  Select the **Binding** tab.

4.  Select the **Override default binding** check box.

5.  In the **Binding type** field, select **CI Identification**.

6.  In the **Class** field, select a CI class.

7.  In the **Select an identifier** field, select an identifier for the class.

    An identifier for a class is a set of rules that helps the system recognize and match CIs correctly. Think of it like a fingerprint for each type of CI \(such as a server, router, or application\). The identifier uses key attributes—like a serial number, hostname, or IP address—to make sure that when new data comes in, it gets linked to the right CI instead of creating duplicates. For more information on CI identification rule, see [Create a CI identification rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_CreateCIIdentificationRule.md).

8.  In the **Add value** field, add the exact value or specify the source field from which the value for the field must be populated.

    Add or remove fields using the add \(![Add icon](../image/em-add-icon.png)\) and the delete \(![Delete icon](../image/em-delete-icon.png)\) icons.

    **Note:** While filling in the CI Class attributes, if you do not find the attribute you need, you can use the **Transform and Compose Alert Output** tab of the event rule to add the necessary key-value pair. For more information, see [Configure an event rule to customize alert content](t_EMComposeOuput.md).

    The event rule transformation and composition is useful when relevant information exists in a different field but needs to be extracted or reassigned for proper alert processing. This is especially important when the required attribute is not directly available and must be manually defined.

    For example, suppose the **Additional information** field of an alert contains the alert name under the **Node** field. However, for correct processing, we need this value to appear under the **Name** field instead. Since there is no existing name attribute in the event, we can manually create one using the **Transform and Compose Alert Output** tab in the event rule. Here’s how:

    1.  Select the **Transform and Compose Alert Output** tab.
    2.  Select the **Manual attributes** check box.
    3.  Add the following key-value pair:
        -   **Field**: Name
        -   **Field Value**: Node
    This configuration ensures that the system extracts the **Node** value and maps it to the name field, making it available for CI binding and alert correlation.

9.  In the **Container level 1** area, specify the host.

10. In the **Select an identifier** field, select an identifier for the container.

11. In the **Add value** field, add the exact value or the field that is the source for the **Select an identifier** field of the container.

    Add or remove fields using the add \(![Add icon](../image/em-add-icon.png)\) and the delete \(![Delete icon](../image/em-delete-icon.png)\) icons.

12. Select **Save**.


