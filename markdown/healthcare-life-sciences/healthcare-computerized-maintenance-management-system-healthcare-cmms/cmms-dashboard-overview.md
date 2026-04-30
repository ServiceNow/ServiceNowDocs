---
title: CMMS Dashboard
description: The CMMS Dashboard is a central place for CMMS users to monitor ongoing operations. The dashboard includes reports that query the database and display the results.
locale: en-US
release: yokohama
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Healthcare CMMS, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# CMMS Dashboard

The CMMS Dashboard is a central place for CMMS users to monitor ongoing operations. The dashboard includes reports that query the database and display the results.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

To access the CMMS Dashboard, install the Performance Analytics Content Pack for Healthcare CDM application. For more information, see [Components installed with Healthcare Computerized Maintenance Management System](../reference/cmms-components-installed.md).

To display the CMMS Dashboard, navigate to **Platform Analytics Workspace** &gt; **Dashboards** &gt; **CMMS Dashboard**.

Dashboards are the home pages for products on the instance. The CMMS Dashboard provides metrics of all the medical devices. It also displays the status of all medical devices. The widgets can be filtered by selecting the duration.

![Landing page of CMMS Dashboard. For text description, refer to steps that follows.](../image/cmms-dashboard.png "Dashboard")

-   **High risk PM% in the selected duration** shows the percentage of the planned work orders that were completed within the due date for high risk medical devices.
-   **Non-high risk PM% in the selected duration** shows the percentage of the planned work orders that were completed within the due date for non-high risk medical devices.
-   **Medical devices in-service in the selected duration** shows number of the medical devices in-service in the selected duration. Click the widget to view the list of all medical devices in-service. You can export the list of all medical devices in-service.
-   **Closed work orders due in the selected duration** shows number of the closed work orders who's requested due date is in the selected duration. Click the widget to view the list of all closed work orders. You can export the list of all the closed work orders.
-   **Open work orders due in the selected duration** shows number of the open work orders who's requested due date is in the selected duration. Click the widget to view the list of all open work orders. You can export the list of all the open work orders.
-   **Status of all work orders due in the selected duration** shows the status of all work orders. Click the widget to view the list of all work orders. You can export the status list of all the work orders.

