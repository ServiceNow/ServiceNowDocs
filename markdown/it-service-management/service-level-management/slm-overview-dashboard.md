---
title: Service level management overview dashboard
description: The Service Level Management Overview Dashboard provides insight into Service Level Agreement \(SLA\) information relevant to the logged-in user. By default, the Overview dashboard is available to users who possess the itil role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-level-management/slm-overview-dashboard.html
release: australia
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# Service level management overview dashboard

The Service Level Management Overview Dashboard provides insight into Service Level Agreement \(SLA\) information relevant to the logged-in user. By default, the Overview dashboard is available to users who possess the itil role.

The Overview Dashboard is enabled by default for new customers. Customers upgrading from a prior release have to enable the Service Level Management Dashboard plugin \(com.snc.sla.overview\) to activate this feature.

You can navigate to the dashboard in the following ways:

-   **Service Level Management** &gt; **Overview**
-   **Self – Service** &gt; **Dashboard** &gt; **SLA Overview**

\[Omitted image "sla-overview-dashboard.png"\] Alt text: sla overview dashboard

|UI component|Description|
|------------|-----------|
|My at Risk SLAs|Number of active task SLAs for tasks assigned to the logged in user that have not yet breached but have elapsed 75% of the duration of the SLA.|
|My Active Breached SLAs|Number of active task SLAs for tasks assigned to the logged in user that have breached.|
|My Active SLAs \(count\)|Number of active task SLAs for tasks assigned to the logged in user.|
|My Groups Active SLAs \(count\)|Number of active task SLAs for tasks assigned to groups that the logged in user is a member of.|
|My Active SLAs \(bar chart\)|Displays a bar chart of active task SLAs for tasks assigned to the logged in user. The data can be grouped and/or stacked on some of the fields available in the task SLA records.|
|My Groups Active SLAs \(bar chart\)|Displays a bar chart of active Task SLAs for Tasks assigned to groups that the logged in user is a member of. The data can be grouped and/or stacked on some of the fields available in the task SLA records.|
|My Active SLAs \(list\)|Displays a list of active task SLAs for tasks assigned to the logged in user. The data can be grouped on some of the fields available in the task SLA records.|

**Parent Topic:**[Service Level Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/service-level-management-reference.md)

