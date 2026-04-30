---
title: Bind alerts to a CI running on a host using CI identifiers
description: Create an event rule to bind alerts to a CI running on a host.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Alert binding to CIs with event rules, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Bind alerts to a CI running on a host using CI identifiers

Create an event rule to bind alerts to a CI running on a host.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

By default, an incoming event from a CI running on a host can bind to an alert based on the event **Node** field value. If the value resides in a different event field, you can use an event rule transform to copy the data to the **Node** field on the alert. The **Description** field with a name the same as a field of the selected CI can be used as an identifier. The Transform and compose screen can be used to add such fields. All the identifier fields must be matched to bind to the CI. Then the system can locate the CI that matches the alert.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Select the server in the configuration item column of the desired alert.

    Leave this screen open so that you can copy any necessary values to use in the binding.

3.  Navigate to **All** &gt; **Event Management** &gt; **All Events**.

4.  Select **New** and fill in the appropriate fields of the event rule.

    See [View events](t_EMManageEvent.md) for a description of the fields.

    1.  In the **Severity** field, enter a Severity value.

    2.  In the **Description** field, enter a description that includes the server name or IP address for enabling the binding to an appropriate CI.

5.  Right-click the top of the form and select **Save** to save the form.

6.  Right-click the **State** field and select **Ready**.

7.  Right-click the top of the form and select **Insert and Stay** to insert the changes and keep the form.

8.  Right-click the top of the form and select **Reload form** to refresh the form.

    Repeat the step until the **State** changes to **Processed**. You can view the results in the **Processing Notes** field. Binding does not take place, since at this step you haven't defined any event rules.

9.  Select **Create Event Rule**.

    Open this Event Rule Designer in a new tab so that you can easily go back to the Event screen.

10. In the **Event Rule Info**, fill in the appropriate fields of the event rule.

11. Select **Event Filter** to build the condition.

    1.  In the **Event Filter** screen, select **Description** that **contains** the description of the desired condition.

    2.  In the **Event Input** table, copy the **Description** text and paste it in the condition.

        The **Event Input** table can be used as a reference to the available event fields and in this case the **Description** field.

12. Select **Transform and Compose Alert Output**.

13. In the **Event Input** table, select the **Description field**.

    1.  In the **Edit Regex Expressions** dialog box, mark a field, such as the IP address, and select **Node.**.

        The field becomes a regex expression for the **Node**.

    2.  Select **Done**.

14. Select **Binding** to bind the alert to the CI using CI identifiers.

15. Select **Override default binding** to override the default binding.

    The default binding uses the value of the **Node** field to try to match the CI name: CI name, FQDN, IP, or MAC address.

16. In the **Binding type** field, select **CI field matching**.

17. In the **CI type** field, select **Configuration Item**.

18. Select **Submit**.

    The **Event Rules** screen opens listing the new event rule.

19. To test the rule.

    1.  Navigate to **All** &gt; **Event Management** &gt; **All Events**.

    2.  Select the recent event that you created.

        You can also go back to the Event in the open tab.

    3.  In the **Node** field, type the server name.

    4.  Select the **State** field and select **Ready**

    5.  In the **Message key** field, type a new message key.

    6.  Right-click the top of the form and select **Insert and Stay** to insert the changes and keep the form.

    7.  Right-click the top of the form and select **Reload form** to refresh the form.

        Repeat the step until the **State** changes to **Processed**. You can view the binding results in the **Processing Notes** field.


**Parent Topic:**[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

**Related topics**  


[Bind alerts to a specific host CI](t_EMBindDevice.md)

[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

