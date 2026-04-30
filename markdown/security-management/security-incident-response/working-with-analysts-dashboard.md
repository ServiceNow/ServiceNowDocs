---
title: Viewing SIR Workspace Dashboards
description: This section present the important metrics to analyze your Security Incident Response process such as new security incidents or the average age of open security incidents.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Viewing SIR Workspace Dashboards

This section present the important metrics to analyze your Security Incident Response process such as new security incidents or the average age of open security incidents.

In the Classic UI, there are few standard dashboards available under homepage and Performance Analytics Dashboards that are available when Performance Analytics for Security Incident Response plugin is installed. All of these will now be available in the new workspace under the **SIR Dashboards** section.

**Standard Dashboards under homepage**:

-   Security Incident Response Overview
    -   Analyst Overview
    -   Manager Overview \(supported in future releases\)
    -   CISO Overview \(supported in future releases\)
-   **Platform Analytics for Security Incident Response**
    -   Security Incident Explorer
    -   CISO Dashboard \(future release\)
    -   Security Incident Management
    -   Security Incident Management Premium KPIs
    -   Security Operations Efficiency
    -   Context Sensitive Analytics – SI Dashboard

**Note:** There might be some repetition of dashboards across standard and platform analytics for security incident response dashboards such as CISO Dashboard. When the plugin is installed, there will be additional content in these dashboards and will not be available as duplicate.

Users need to install the plugin for the dashboards listed under Platform Analytics for Security Incident Response Dashboards to be present in the workspace. Otherwise, only the standard dashboards will be available.

In the current version of the SIR Workspace, the following dashboards are available under the **SIR Dashboards** section. The other dashboards that are missing will be available in later releases.

|Dashboard|Description|
|---------|-----------|
|Standard Dashboard|
|Security Analyst Overview|With this dashboard, security analysts can view security incidents summarized based on analyst’s critical priority work, high priority work, security Incidents that are assigned to the analyst, tasks assigned to the analysts, and incident count.|
|Performance Analytics \(PA\) for Security Incident Response Dashboards|
|Security Incident Explorer|With this dashboard, security managers and analysts can view security incidents summarized and grouped by category, subcategory, location, priority, and business impact. These views let managers and analysts quickly gain insight into the frequency in which attacks are occurring and which business services are affected.|
|Security Incident Management|With this dashboard, security managers can easily track the volume, performance, and progress of security incidents from initial analysis/detection to containment, eradication, and recovery.|
|CISO Dashboard|Proposed to support in future release.|
|Security Operations Efficiency|With this dashboard, managers and analysts can view overall efficiency metrics and measure the performance of the SOC.|
|Security Incident Management Premium KPIs|With this dashboard, security managers can track and view the volume, performance, and progress of security incidents from initial analysis/detection to containment, eradication, and recovery.|
|Context Sensitive Analytics – S|With this dashboard, managers and analysts can view the open security incidents, the average age of open Security Incidents, the average close time of security incidents, the percentage of security incidents that were opened and closed on the same day, and the percentage of the incidents that were not updated in the last 5 days and 30 days.|

## Access SIR and PA Dashboards

The **SIR Dashboards** icon displayed on the left side of the workspace home page.

**Note:** Users with sn\_si.manager or sn\_si.admin access can edit the dashboards. The users must be within the same scope of the dashboards that the user is trying to make edits. For example, security analyst overview dashboard is available in the SIR workspace, then the user should also be in the same SIR workspace scope to make the edits to the dashboard.

1.  Navigate to **Workspaces** &gt; **Security Incident Management Workspace**.
2.  Click on the **SIR Dashboards** ![Dashboard icon](../image/dashboard.png)icon.
3.  Select the desired Dashboard from the drop down list.

    ![Selecting the Security Incident Explorer Dashboard.](../image/dashboard-drop-down.png)


You can edit the dashboards, add new elements to the dashboards, and create your own dashboards. For more information on how to use dashboards, see [Working with responsive dashboards](https://www.servicenow.com/docs/access?context=c_ResponsiveDashboards&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

