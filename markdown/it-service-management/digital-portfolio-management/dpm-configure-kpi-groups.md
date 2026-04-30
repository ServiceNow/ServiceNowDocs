---
title: Configure KPI groups in Digital Portfolio Management
description: Configure key performance indicator \(KPI\) groups in Digital Portfolio Management \(DPM\) to surface performance information in the context of your organization's solutions.
locale: en-US
release: yokohama
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Configure KPI groups in Digital Portfolio Management

Configure key performance indicator \(KPI\) groups in Digital Portfolio Management \(DPM\) to surface performance information in the context of your organization's solutions.

Configure KPI groups. 

With a DPM admin role \[sn\_dpm.dpm\_admin\], you can define and configure the key performance indicator \(KPI\) groups in DPM. With KPI groups, your organization can analyze the performance of services, offerings, business services, and application services in a centralized area.

**Important:** KPI data in DPM comes from portfolios in the Service Portfolio Management application. The Service Offering Metric Data \[service\_offering\_metric\_data\] table along with the following four indicators have been deprecated in the Utah release:

-   Average SLA Achievement \[ServiceOffering.MetricData.SLA.Daily\]
-   Average Customer Satisfaction \[ServiceOffering.MetricData.CSAT.Daily\]
-   Average Availability \[ServiceOffering.MetricData.Availability.Daily\]
-   Average Request Activity \[ServiceOffering.MetricData.Activity.Daily\]

Therefore, if you have the Service Portfolio Management standard portfolio \(the most recent version\), then the metric data from the legacy indicators are no longer available. For more information, see [Service Portfolio Management portfolios](../../service-portfolio-management2/concept/SPM2-service-portfolios.md).

-   **[Create KPI groups and mappings in Digital Portfolio Management](../task/dpm-create-kpi-groups.md)**  
Create key performance indicator \(KPI\) groups and mappings in Digital Portfolio Management \(DPM\) to monitor the overall health and progress of all your services and offerings.
-   **[Configure KPIs in Digital Portfolio Management with service availability example](../task/dpm-configure-kpi-availability.md)**  
Configure key performance indicators \(KPIs\) in Digital Portfolio Management \(DPM\) to surface performance information in the context of your solutions. This procedure uses the example of configuring service availability to display the availability score in the Run life-cycle phase.
-   **[Copy a KPI group to create a new KPI group in Digital Portfolio Management](../task/dpm-copy-kpi-group.md)**  
Create a new key performance indicator \(KPI\) group by copying an existing KPI group in Digital Portfolio Management \(DPM\). All the KPI records, supporting KPIs, and mappings of the KPI group are copied as well. After you copy the KPI group, you can modify all aspects of it so the new group best fits your needs.
-   **[Update KPIs in Digital Portfolio Management](../task/dpm-kpi-descriptions.md)**  
You can update the key performance indicator \(KPI\) fields in Digital Portfolio Management \(DPM\). The KPI displays in KPI groups in the DPM Workspace.

**Parent Topic:**[Configuring Digital Portfolio Management](dpm-configure-cfw.md)

