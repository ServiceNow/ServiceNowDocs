---
title: Unauthorized change properties
description: Use the Unauthorized Change Properties page to enable or disable the unauthorized change capability, and to configure the criteria for additional unauthorized change properties.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Unauthorized change request, Create a change request, Using Change Management, Change Management, IT Service Management]
---

# Unauthorized change properties

Use the Unauthorized Change Properties page to enable or disable the unauthorized change capability, and to configure the criteria for additional unauthorized change properties.

From this properties page, you can control the capabilities, such as:

-   Enabling or disabling the creation of unauthorized change requests when receiving the **ci.change.unplanned** event.
-   Configuring the type of change requests, which are valid, and fall into the unauthorized change category.
-   Configuring a quiet time, whereby, if there is a repeated change to a CI that has been flagged previously, another unauthorized change is not created within that time period.
-   Configuring the interval frequency for detection.
-   Including a CI class for the change request that must be monitored.

    **Note:** Monitored CIs must be part of an application service.


Navigate to **Change** &gt; **Administration** &gt; **Unauthorized Change Properties** to view and edit the properties.

<table id="table_yrv_pqf_b4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable event processing

</td><td>

Enable the property to create unauthorized change events when an unplanned CI change \(**ci.change.unplanned**\) event is triggered.Default value: False

</td></tr><tr><td>

Notification ignores period

</td><td>

Enter the time duration until which you want to disable sending notifications or creating unauthorized changes for the same CI.Default value: 1 day

</td></tr><tr><td>

Change request query

</td><td>

Add the query conditions to define what change requests are valid and belong to the unauthorized change category. For example, you can add a condition to view all active change requests that are in the implement or review state for the given CI. If the conditions given are not met, then the change becomes an unauthorized change.

</td></tr><tr><td>

CI class inclusion

</td><td>

Choose the CI classes that you want to include and monitor for an unauthorized change to be created.

</td></tr></tbody>
</table>**Parent Topic:**[Unauthorized change request](../concept/unauthorized-change-request.md)

**Related topics**  


[Disable the creation of an unauthorized change request](../task/disable-unauth-notification.md)

