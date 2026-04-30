---
title: Security Incident Response Platform Analytics Solutions
description: Platform Analytics Solutions contain preconfigured dashboards. The dashboards present important metrics for analyzing your Security Incident Response process, such as new security incidents or the average age of open security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response Platform Analytics Solutions

Platform Analytics Solutions contain preconfigured dashboards. The dashboards present important metrics for analyzing your Security Incident Response process, such as new security incidents or the average age of open security incidents.

Platform Analytics data visualizations use Performance Analytics [indicator](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-indicator&ft:locale=en-US) data to show you data over time, helping you analyze your business processes and identify areas of improvement. With Platform Analytics Solutions, you can get value from Performance Analytics for your application with minimal setup. You can always create your own objects as well.

The Security Incident Response Performance Analytics Solution is available from the ServiceNow Store. For information about downloading and installing this application, see [Security Operations and the ServiceNow Store](../../../product/planning-and-policy/concept/secops-and-store.md).

**Note:** To evaluate the functionality, you can activate Performance Analytics solutions and in-form analytics on instances that have not licensed Performance Analytics. However, you have the following limitations:

-   You cannot create new indicators.
-   You cannot collect data older than 180 days.

For full functionality, license Performance Analytics. For more information, see [Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

**Important:** By default, the data collection limit for the `(com.snc.pa.dc.max_records)` property in Performance Analytics is set as 5,000 records. But you can increase this limit per your requirements, such as 50,000 records. However, increasing this limit may impact performance during data collection or when performing operations on the Snapshot table. To learn more about the Performance Analytics properties, see [Performance Analytics properties](https://www.servicenow.com/docs/access?context=pa-properties&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

-   **[CISO dashboard](ciso-dashboard.md)**  
This dashboard reveals the overall security posture of your organization, including security vulnerability and incidents.
-   **[Security Incident Management Premium dashboard](si-mgmt-premium-dashboard.md)**  
This dashboard uses advanced Platform Analytics visualizations to aid security managers to track the volume, performance and progress of security incidents from initial analysis/detection to containment, eradication, and recovery. The licensed version of Performance Analytics is therefore required.
-   **[Security Incident Management dashboard](security-incident-mgmt-dashboard.md)**  
With this dashboard, security managers can easily track the volume, performance and progress of security incidents from initial analysis/detection to containment, eradication, and recovery.
-   **[Security Incident Explorer dashboard](si-explorer-dashboard.md)**  
With this dashboard, security managers are able to view security incidents summarized and grouped by category, subcategory, location, priority and business impact. These views let managers quickly gain insight into the frequency in which attacks are occurring and which business services are affected.
-   **[Security Operations Efficiency dashboard](../../../product/security-incident-response/concept/cj-sir-socpa-dashboard.md)**  
Security operations center \(SOC\) managers can view overall efficiency metrics and measure the individual performance of the SOC team members in the organization.

**Parent Topic:**[Security Incident Response setup](../../../product/security-incident-response/concept/setup-sir.md)

**Related topics**  


[Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=content-packs-in-form-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

[Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

