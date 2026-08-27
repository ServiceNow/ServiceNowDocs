---
title: Exploring L1 IT Service Desk AI Specialist
description: The L1 IT Service Desk AI Specialist uses AI agents to accomplish bigger tasks, such as task triage or updating customers with solutions that worked for similar issues. Unlike AI agents that automate specific business tasks, the L1 IT Service Desk AI Specialist is designed to perform many relevant tasks to function like a member of your team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/exploring-l1-sd-ai-specialist.html
release: zurich
topic_type: concept
last_updated: "2026-08-14"
reading_time_minutes: 5
keywords: [explore]
breadcrumb: [L1 IT Service Desk AI Specialist, IT Service Management]
---

# Exploring L1 IT Service Desk AI Specialist

The L1 IT Service Desk AI Specialist uses AI agents to accomplish bigger tasks, such as task triage or updating customers with solutions that worked for similar issues. Unlike AI agents that automate specific business tasks, the L1 IT Service Desk AI Specialist is designed to perform many relevant tasks to function like a member of your team.

## L1 IT Service Desk AI Specialist overview

The L1 IT Service Desk AI Specialist is an autonomous worker that is designed to help handle incidents end-to-end without human intervention. It uses knowledge articles and historical data to investigate and resolve assigned incidents. It communicates directly with requesters and escalates incidents to human agents when confidence is low.

Onboarding the L1 IT Service Desk AI Specialist can be helpful for high-volume, repeatable L1 incidents, a well-maintained knowledge base, and a clear resolution path. The L1 IT Service Desk AI Specialist addresses routine and low-level work, such as handling password reset requests. This frees human agents to focus on more complex work.

You can assign the L1 IT Service Desk AI Specialist to different assignment groups and roles to limit the scope of work and the data accessed.

Skills are the types of issues that the L1 IT Service Desk AI Specialist can handle. Tasks are the specific actions that the L1 IT Service Desk AI Specialist uses to solve those issues. After configuring, you can test your L1 IT Service Desk AI Specialist to verify it's working as expected. Once the L1 IT Service Desk AI Specialist has been activated, you can monitor its performance and activity on the records it handles.

The tasks available to the L1 IT Service Desk AI Specialist include:

-   Task classification and assignment
-   Incident triage and diagnosis
-   Investigate and resolve
-   Communicate updates
-   Handle escalations and reroute tickets

You can learn more about the different tasks and their options in [Configure L1 IT Service Desk AI Specialist tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/config-tasks-l1-sd-ai-spec-sow.md).

## L1 IT Service Desk AI Specialist users

<table id="table_eg5_bz2_q3c"><thead><tr><th>

User

</th><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Desk agent

</td><td>

sn\_itsm\_common.sn\_service\_desk\_agent

</td><td>

Service Desk agents resolve tasks, such as incidents and cases, using their knowledge, research, and experience.

 They have access to the Service Operations Workspace, where they have the ability to view the work of the L1 IT Service Desk AI Specialist on a record.

</td></tr><tr><td>

Service Desk manager

</td><td>

sn\_sow\_itsm\_common.sn\_service\_desk\_manager

</td><td>

Service Desk managers have the capabilities of a standard Service Desk Agent \(sn\_service\_desk\_agent\) as well as team level oversight and task resolution.

 They can view and manage team performance reports, analytics, and tasks and onboard the L1 IT Service Desk AI Specialist to the team in Service Operations Workspace.

</td></tr></tbody>
</table>## L1 IT Service Desk AI Specialist workflow

Follow this workflow to implement and manage the L1 IT Service Desk AI Specialist in your organization.

1.  [Configure the L1 Service Desk AI Specialist.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/configuring-l1-sd-ai-specialist.md)

    -   [Basic details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/config-details-l1-sd-ai-spec-sow.md), including name, profile icon, department, and description.
    -   [Profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/config-profile-l1-sd-ai-spec-sow.md), including roles and assignment groups.
    -   [Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/config-tasks-l1-sd-ai-spec-sow.md), which consist of its tasks.
    Once you have configured the L1 IT Service Desk AI Specialist, you can [test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/test-l1-sd-ai-spec-sow.md) it on specific task records to preview how it works.

2.  [Monitor activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/activity-l1-sd-ai-spec.md) to review the records that the L1 IT Service Desk AI Specialist has worked on to verify the details.
3.  [Track performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/perf-l1-sd-ai-spec.md), including analytics that show effectiveness, incident outcomes, and value and feedback. Use the analytics routinely to view the details in these areas. You can configure the L1 IT Service Desk AI Specialist to make changes at any time.

## L1 IT Service Desk AI Specialist benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Automate common categories of tasks|L1 IT Service Desk AI Specialist skills|Service Desk agent|
|Classify and triage incoming work|L1 IT Service Desk AI Specialist tasks|Service Desk agent|
|Investigate related records|L1 IT Service Desk AI Specialist tasks|Service Desk agent|
|Communicate with users|L1 IT Service Desk AI Specialist tasks|Service Desk agent|
|Monitor team and L1 Service Desk AI Specialist performance|Performance metrics|Service Desk manager or admin|
|Test before activation|L1 IT Service Desk AI Specialist guided setup in SOW|Service Desk manager or admin|

## What to explore next

To learn more about configuring and using the L1 Service Desk AI Specialist, see:

-   [Configuring the L1 Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/configuring-l1-sd-ai-specialist.md)
-   [Using L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/using-l1-sd-ai-specialist.md)
-   [Reference for L1 IT Service Desk AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/reference-l1-sd-ai-specialist.md)

## Related products

For more information about ServiceNow Autonomous Workforce, which is made up of AI specialists, see [Autonomous Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-workforce.md), and review the [General guidelines for deploying an autonomous workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/gg-ai-workforce.md).

