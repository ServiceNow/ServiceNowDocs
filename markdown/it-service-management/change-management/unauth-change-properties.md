---
title: Unauthorized change properties
description: Use the Unauthorized Change Properties page to enable or disable the unauthorized change capability, and to configure the criteria for additional unauthorized change properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-service-management/change-management/unauth-change-properties.html
release: yokohama
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
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


This topic uses these terms consistently:

-   Unplanned CI change- A change detected directly on a configuration item, which raises the **ci.change.unplanned** event.
-   Unauthorized change request- The change request record created in response to an unplanned CI change that does not match an existing valid change request. For more information, see [Unauthorized change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/unauthorized-change-request.md)

Navigate to **Change** &gt; **Administration** &gt; **Unauthorized Change Properties** to view and edit the properties.

<table id="table_yrv_pqf_b4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable event processing

</td><td>

Enable this property to create an unauthorized change request when an unplanned configuration item \(CI\) change raises a **ci.change.unplanned** event. The unplanned CI change is the detected activity; the unauthorized change request is the record created in response.Default value: False

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
</table>**Parent Topic:**[Unauthorized change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-service-management/change-management/unauthorized-change-request.md)

**Related topics**  


[Disable the creation of an unauthorized change request]()

