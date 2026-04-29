---
title: View Security Incident Response Health dashboard
description: Security Incident Response Health dashboard feature provides a centralized view of critical aspects related to incident response process implementation, issues/errors encountered, and performance metrics. It serves as a vital tool for monitoring and optimizing the effectiveness of an organization's security incident response capabilities.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [View SIR Workspace Dashboards, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View Security Incident Response Health dashboard

Security Incident Response Health dashboard feature provides a centralized view of critical aspects related to incident response process implementation, issues/errors encountered, and performance metrics. It serves as a vital tool for monitoring and optimizing the effectiveness of an organization's security incident response capabilities.

## Before you begin

Role required: sn\_si.admin, or sn\_si.analyst, or sn\_si.analytics\_read - View dashboard.

## About this task

You can monitor the health of the security incidents using the widgets and trend charts for each application. These statistics present a comprehensive health score detailing the configuration state and remediation effectiveness within the SIR applications. The Security Incident Response Health dashboard supports the following four tabs:

-   **Process**: The tab displays a summary of all the incidents from various alert sensors grouped on a weekly basis.
-   **Implementation**: This tab displays the customizations that the customers perform in their instances covering script includes, business rules, flows, and upgrades.
-   **Issues/Errors**: The tab displays widgets highlighting errors in integration processes, discrepancies during the ingestion of raw incident data, outbound HTTP errors in SIR applications, and any issues arising during the execution of playbooks.
-   **Performance**: This tab displays the performance issues in the SIR applications, including slowness in performance queries, business rules, and scripts.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select the **SIR Dashboards** icon on the SIR workspace homepage.

3.  Select **Security Incident Response Health dashboard** from the drop-down list.

4.  Select the **Process** tab to view the number of security incidents that were triggered on a weekly basis for each alert sensor on the chart.

    ![Process tab on the SIR Health dashboard](../image/sir-health-dash-process.png "Process tab")

    You can perform the following tasks:

    1.  Select an alert sensor on the chart to view the KPI details of the number of security incidents that triggered by alert sensors in a week.

    2.  To get the KPI details for a particular week, use the **Calendar** option.

    3.  To compare the security incidents triggered by the alert sensor, select the **Compare Records** option.

    4.  To use the Chart type, Time series, or Analysis, select the **Chart Options**.

5.  Select the **Implementation** tab to view the number of customizations that were created for the security incidents in the Security Incident Response applications.

    ![Implementation tab on the SIR Health dashboard](../image/sir-health-dash-implementation.png "Implementation tab")

    **Implementation** tab:

    You can view the aggregated dashboard for the number of customizations that were created for each Incident Response application.

    -   **Customized Script Includes**: This widget displays the number of customized scripts that were added based on your requirements in the SIR applications.
    -   **Customized Business Rules**: This widget displays the number of customized business rules that were added based on your requirements in the SIR applications.
    -   **Customized Flows**: This widget displays the number of customized flows that were added based on your requirements in the SIR applications.
    -   **New Business Rule on Security Incident table**: This widget displays the number of business rules that were created on the Security Incident table.
    -   **Upgrade Conflicts**: This widget displays the number of conflicts that were triggered during upgrades in the SIR applications.
6.  Select the **Issues/Errors** tab to view the number of issues or errors that were triggered in the Security Incident Response applications.

    ![Issues/Errors tab on the SIR Health dashboard](../image/sir-health-dash-errors.png "Issues/Errors tab")

    **Issues/Errors** tab:

    You can view the aggregated dashboard for issues or errors in the Security Incident Response applications.

    -   **Errors during transformation import**: This widget displays the number of errors that were triggered during the transformation import in SIR applications.
    -   **Errors related to integrations**: This widget displays the number of errors that were triggered during the SIR integrations.
    -   **Capability framework executions in error state**: This widget displays the number of errors that were triggered during the capability framework executions in SIR applications.
    -   **Failed outbound HTTP calls**: This widget displays the number of failed outbound HTTP calls that were triggered in the SIR applications.
    -   **PAD Playbook executions in error state**: This widget displays the number of PAD Playbook execution errors that were triggered in the SIR applications.
7.  Select the **Performance** tab to view the number of performance issues that were triggered in the Security Incident Response applications.

    ![Performance tab on the SIR Health dashboard](../image/sir-health-dash-performance.png "Performance tab")

    **Performance** tab:

    You can view the aggregated dashboard for performance issues in the Security Incident Response applications.

    -   **Slow Performance Queries**: This widget displays the number of performance queries in the SIR applications whose average execution time is greater than 10 ms and averaged on 1000 or more executions.
    -   **Slow business rules and scripts**: This widget displays the number of business rules and scripts in the SIR applications whose average execution time is greater than 10 ms and averaged on 1000 or more executions.
8.  You can use the **Refresh** icon to refresh the data in the Security Incident Response Health dashboard.

9.  You can use the **View dashboard details** icon to view the details of the Security Incident Response Health dashboard.

10. You can use the **Edit** option to modify the details of the Security Incident Response Health dashboard.

11. You can use the **More** option to perform additional actions on the Security Incident Response Health dashboard.


