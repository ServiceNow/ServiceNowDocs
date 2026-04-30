---
title: Configuring Service Observability
description: After you install Service Observability, you must register services, connect external application performance management \(APM\) instances, and map that APM data to those services.
locale: en-US
release: yokohama
product: Service Observability
classification: service-observability
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Observability, ITOM AIOps, IT Operations Management]
---

# Configuring Service Observability

After you install Service Observability, you must register services, connect external application performance management \(APM\) instances, and map that APM data to those services.

## Configuration overview

-   **[Install Service Observability](../task/install-service-observability.md)**  
If you have the system admin role, you can install the Service Observability application \(`sn_sow_svcobs`\). The application installs related ServiceNow® Store applications and plug-ins if they aren't already installed.
-   **[Activate teams and services](activate-teams-and-services.md)**  
Follow this step only if you are on version 1.5.0 of Service Observability. Assign existing teams to Service Observability so they can view the data returned by the Configuration Management Database \(CMDB\) on those pages. Activate the services in the CMDB for use in Service Observability.
-   **[Connect a Service Observability data source](../task/connect-an-observability-data-source.md)**  
Connect Service Observability to an external application performance management \(APM\) instance. Service Observability displays metrics in the Service Operations Workspace \(SOW\) from that APM instance.
-   **[Create and manage data mappings](../task/create-and-manage-observability-data-mappings.md)**  
Map your services to the data from a connected external application performance management \(APM\) instance, and view it in charts for the service.
-   **[Customize Service Observability dashboard templates](../task/customize-service-observability-dashboard-templates.md)**  
You can customize the Service Observability dashboards on both the Overview and Observability tabs of the Service Details page. You can change or add metrics and related data to fit your business needs.
-   **[Use synthetic monitoring with Service Observability](use-synthetic-monitoring-with-service-observability.md)**  
Create a synthetic monitor to test your service's endpoints. Then display the results by customizing a Service Observability dashboard.

**Parent Topic:**[Service Observability](service-observability.md)

