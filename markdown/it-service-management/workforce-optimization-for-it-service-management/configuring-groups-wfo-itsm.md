---
title: Configuring groups in Workforce Optimization for ITSM
description: As a manager, you can manage and optimize your entire workforce using Workforce Optimization for ITSM from one central location. Organizing your teams, for example, different levels of employees in your organizational chart, into groups is the foundation on which Workforce Optimization for ITSM operates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/workforce-optimization-for-it-service-management/configuring-groups-wfo-itsm.html
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 3
breadcrumb: [Getting started, Workforce Optimization for ITSM, IT Service Management]
---

# Configuring groups in Workforce Optimization for ITSM

As a manager, you can manage and optimize your entire workforce using Workforce Optimization for ITSM from one central location. Organizing your teams, for example, different levels of employees in your organizational chart, into groups is the foundation on which Workforce Optimization for ITSM operates.

Therefore, after you set up your teams as groups in Workforce Optimization for ITSM, as a manager, you can route work, set up schedules, train your teams, and analyze all aspects of your workforce from one location.

## Planning for your Workforce Optimization for ITSM implementation

Before you start implementing Workforce Optimization for ITSM, make sure you do the following:

**Important:** Groups are synonymous with assignment groups. A team member can belong to multiple groups but must have one group identified as their primary assignment group. If not, that team member cannot view their schedules in Service Operations Workspace. For more information on Schedules in Service Operations Workspace, see [Service Operations Workspace - Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/itsm-sow-workspace-scheduling.md).

1.  **Identify your teams**

    Define the different teams within your organizations that you want to manage. Each of these teams will be configured as a group in the User Groups \[sys\_user\_group\] table. When a user logs into Workforce Optimization for ITSM, the workspace will only display the logged-in user's teams and information related to those teams.

2.  **Assign a primary assignment group for each member of your team**

    A team member can belong to multiple groups but you must identify one group identified as the primary group for each team member and assign it to them. This determines which assignment group's team calendar that the team member can view in the Schedules module in [Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/itsm-sow-workspace-scheduling.md) and also determines activities such as coaching and approvals. For more information on setting a primary assignment group, see [Assign a primary assignment group for each agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/workforce-optimization-for-it-service-management/setup-primary-group-wfo-itsm.md).

    The following image shows a representation of assigning a primary group to a team member who belongs to more than one group.\[Omitted image "organize-teams-wfo-itsm.png"\] Alt text: Diagram showing three regional assignment groups under Global Teams, each with managers and team members. Two team members belong to more than one group.

3.  **Add a manager to each group**

    Each team must have a manager assigned. This manager is someone who would directly oversee the team.

4.  **Add additional managers to each group**

    For each group that you create, you can also add managers who don’t directly manage the group but need visibility into those groups. These managers are known as additional managers.


If you have three teams in different regions and the first team is in Americas \(AMS\), the second one is in Asia-Pacific \(APJ\) and the third one is in Europe, the Middle East, and Africa \(EMEA\), you must create an assignment group for each one of them and also associate each team member to one of the groups as their primary assignment group. You can also associate more managers to a team although they may not directly manage that team. These managers are referred to as additional managers who have visibility into the what the team does.

-   **[Assign a primary assignment group for each agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/workforce-optimization-for-it-service-management/setup-primary-group-wfo-itsm.md)**  
Associate each agent in your team to a primary assignment group to enable them to see the KPI metrics for the groups to which they belong.

**Parent Topic:**[Getting started with Workforce Optimization for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/workforce-optimization-for-it-service-management/getting-started-workforce-optimization-itsm.md)

**Related topics**  


[Exclude access for specific groups in Workforce Optimization for ITSM manager workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/workforce-optimization-for-it-service-management/configure-access-exclusion-wfo-itsm.md)

[Using extension points to include access for specific groups in Workforce Optimization for ITSM manager workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/workforce-optimization-for-it-service-management/ext-points-exclude-access-wfo-itsm.md)

