---
title: Monitoring and analytics for Field Service Management
description: Manage, supervise, and monitor various managerial activities involved in Field Service Management, such as managing work order task assignments, approving agent time-off, workload, and others.Manage contractor work and service level agreements \(SLA\). With the ServiceNow Contractor Management application, connect, engage, and collaborate with third-party contractor companies and their staff to outsource the work order tasks.The Emergency Exposure Management feature in Field Service Management helps identify field service agents and customers who may have visited an affected location. It helps find people who have come in contact with an agent who has been classified as positive for a condition, such as COVID-19.Resolve work orders more efficiently by using Predictive Intelligence for Field Service Management to identify work orders with similar issues. Each group of similar work orders represents a work order trends topic.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore, Field Service Management]
---

# Monitoring and analytics for Field Service Management

Manage, supervise, and monitor various managerial activities involved in Field Service Management, such as managing work order task assignments, approving agent time-off, workload, and others.

## Field Service Contractor Management

Manage contractor work and service level agreements \(SLA\). With the ServiceNow Contractor Management application, connect, engage, and collaborate with third-party contractor companies and their staff to outsource the work order tasks.

The Field Service Contractor Management application enables Field Service managers of your organization to outsource work by onboarding contractor companies and their staff, such as external managers and external agents. Work order tasks are assigned to the contractor group's manager from the contractor company. A group qualifies the assignment criterion based on the selected assignment group values, such as the external group, and its coverage area, skills, and product models.

The managers of these contractor companies use the [Contractor Portal](field-service-contractor-portal.md) to review the assigned work order task details and can choose to reject work on the tasks. If they accept the task, they can then reassign the tasks to their contractor team members.

If the preferred assignment group is internal but no one in the internal group qualifies for the assignment group criterion, then the system searches for a suitable external group to assign the task to and vice versa.

**Related topics**  


[Activate Field Service Contractor Management](../task/activate-contractor-management-plugin.md)

[Configuring Contractor Management](configuring-fsm-contractor-management.md)

[Contractor Portal](field-service-contractor-portal.md)

[Contractor dashboard](../../../use/dashboards/application-content-packs/contractor-dashboard.md)

## Emergency Exposure Management

The Emergency Exposure Management feature in Field Service Management helps identify field service agents and customers who may have visited an affected location. It helps find people who have come in contact with an agent who has been classified as positive for a condition, such as COVID-19.

By using the Emergency Exposure Management application in collaboration with Field Service Management, you can identify potentially affected customers and other agents by checking the work order history of the affected agent.

If an agent is reported as positive for a condition, the diagnostic admin can run a diagnostic report to identify other potentially affected agents, customers who might have come in contact with the affected agent, and other agents who visited the affected customers during the selected time period. The Field Service manager can view the diagnostic report and take appropriate action to mitigate the spread of infection. The manager can promote agent safety by blocking the affected or potentially exposed agents from being available for future dates.

The Emergency Exposure Management application enables you to do the following:

-   **Trace affected agents and customers**

    Run a diagnostic report for affected agents based on their work order history for the selected time period and view the report to identify other potentially affected agents and customers.

-   **Block agent calendars**

    Mark the affected and potentially affected agents unavailable for the selected time period to avoid assigning any further tasks.

-   **Enforce compliance checks for agents**

    Require agents to participate in a compliance survey before starting work on the task and before completing the work order task to check whether they have taken proper precautions based on the recommended safety protocol guidelines.

-   **View data with Covid19 impact**

    View task, agent, and asset locations on a map that shows the COVID-19 impact.


**Related topics**  


[Use Emergency Exposure Management for Field Service agent monitoring and assignments](use-exposure-management-fsm.md)

## Predictive analytics: Work order insights

Resolve work orders more efficiently by using Predictive Intelligence for Field Service Management to identify work orders with similar issues. Each group of similar work orders represents a work order trends topic.

### Key benefits

Using work order trends topic has the following benefits:

-   Increase manager productivity: Quickly identify clusters of cases that point to similar underlying issues and act to resolve them.
-   Improve agent experiences: Proactively resolve issues by analyzing other work orders in the topic.​
-   Enhance operational efficiency: Reduce the backlog of work orders by resolving several similar type of work orders at once.​

System administrators train solution definitions to identify and cluster similar type of work orders. Managers use the **Work Order Trends** topic lists to analyze the backlog of work orders.

**Related topics**  


[View work order trends topics](../task/view-wo-trends.md)

