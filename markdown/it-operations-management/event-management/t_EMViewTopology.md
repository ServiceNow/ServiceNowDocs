---
title: View an alert impact on CIs in a service map
description: You can view service maps to see active alerts for CIs and the relationship between CIs. By viewing this information, you can better understand the source of alerts and take remediation steps. The service map is available for all application services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/t\_EMViewTopology.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# View an alert impact on CIs in a service map

You can view service maps to see active alerts for CIs and the relationship between CIs. By viewing this information, you can better understand the source of alerts and take remediation steps. The service map is available for all application services.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

You can open a service map from these places:

-   From the Application services list, you can view service maps for application services.
-   From the Monitored services list, you can view service maps for monitored services.

## Procedure

1.  Open an application service map:

    1.  Navigate to **Event Management** &gt; **Services** &gt; **Application Services**.
    2.  Next to the service, click **View Map**.
2.  Do one or more of the following.

<table><thead><tr><th align="left" id="d668896e126">

Option

</th><th align="left" id="d668896e129">

action

</th></tr></thead><tbody><tr><td id="d668896e135">

**View alerts for a CI by type and severity**

</td><td>

In the service map:1.  Click a CI tile.
2.  Below the map, click the **Alerts** tab and review the listed alerts.


</td></tr><tr><td id="d668896e156">

**View changes to a CI in a discovered service**

</td><td>

In the service map:1.  Click a CI tile.
2.  Below the map, click the **Changes** tab.


</td></tr><tr><td id="d668896e177">

**Show alert bindings to CIs**

</td><td>

In the service map:1.  Click a CI tile.
2.  Click the additional actions menu icon\[Omitted image "context-menu-icon.png"\] Alt text: Additional actions menu option. to view the **Affected CIs** indicator.
3.  Below the map, click the **Affected CIs** tab.


</td></tr><tr><td id="d668896e210">

**View CI properties**

</td><td>

In the service map:1.  Click a CI tile.
2.  In the side pane, click the **Properties** tab and review information about the CI.
3.  If you want to view more detailed information, scroll to the end of the pane and click **Detailed Properties**.


</td></tr><tr><td id="d668896e238">

**Show the impact rules for a CI**

</td><td>

In the service map:1.  Click a CI that has a severity.
2.  Below the service map, click the **Impact** tab and review the listed impact rules.


</td></tr><tr><td id="d668896e259">

**Show alert details for networks or storage for a service**

</td><td>

In the service map: 1.  Right-click a path between CIs.
2.  Select **Show network path**or **Show storage path**.


</td></tr><tr><td id="d668896e283">

**Display additional information for CIs**

</td><td>

In the service map header: 1.  Click the additional actions menu icon \[Omitted image "context-menu-icon.png"\] Alt text: Additional actions menu option.
2.  You can select the **Map Indicators** for additional information that you want to view.


</td></tr><tr><td id="d668896e309">

**Remediate a CI**

</td><td>

In the topology, right-click the CI, and then select **Remediation options**.

</td></tr></tbody>
</table>
**Related topics**  


[Alert impact calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/c_EMImpactCalculation.md)

[Understand Service Maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/Understand-Service-Maps.md)

