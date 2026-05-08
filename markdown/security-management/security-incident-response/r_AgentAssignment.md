---
title: Assigning security analysts
description: Depending on your settings in the SIR Administration Configuration screen, you can assign security analysts to security incidents manually; automatically by using a workflow; or automatically by using auto-assignment.You can configure the Security Incident Response Administration Configuration screen to require that security analysts be assigned manually whenever someone or the SIR application creates a security incident or generates a security response task.You can configure the Security Incident Response Administration Configuration screen to use a selected workflow to assign the security analyst whenever someone or the SIR application creates a security incident or security response task.You can configure the Security Incident Response Administration Configuration screen to auto-assign the security analyst whenever someone or the SIR application creates a security incident or security response task. Auto-assignment allows you to define, based on the needs of your organization, the criteria by which analysts are assigned automatically to security incidents.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Assigning security analysts

Depending on your settings in the SIR Administration Configuration screen, you can assign security analysts to security incidents manually; automatically by using a workflow; or automatically by using auto-assignment.

## Manual analyst assignment

You can configure the Security Incident Response Administration Configuration screen to require that security analysts be assigned manually whenever someone or the SIR application creates a security incident or generates a security response task.

If a security incident or response task cannot be auto-assigned, you can set the SIR Administration Configuration screen to require the manual assignment of security analysts. This is a good choice if you have a limited number of security analysts for completing requests or if you simply do not want to auto-assign them.

## Workflow-based security analyst assignment

You can configure the Security Incident Response Administration Configuration screen to use a selected workflow to assign the security analyst whenever someone or the SIR application creates a security incident or security response task.

In the Security Incident Administration configuration screen, you can choose to use a workflow to assign an analyst to each security incident or security response task. This option is a good choice for organizations that use a custom process for resolving security issues or otherwise have a process that can be automated.

## Automatic security analyst assignment

You can configure the Security Incident Response Administration Configuration screen to auto-assign the security analyst whenever someone or the SIR application creates a security incident or security response task. Auto-assignment allows you to define, based on the needs of your organization, the criteria by which analysts are assigned automatically to security incidents.

### Agent auto-assignment based on agent ratings

If auto-assignment is enabled and a security incident or a response task is created, the following actions occur:

-   The available security analysts are evaluated based on the criteria defined in the configuration.
-   An appropriate security analyst is automatically assigned to the task.
-   The task is moved to the **Assigned** state.

If the configuration is set up to consider more than one set of conditions, such as skills, location, time zone, or group coverage area, the security analysts are evaluated based on the weighting property settings and other criteria. These configuration settings help you auto-assign agents based on optional properties. The calculated ratings are used to determine the best agent for the security incident or response task. Any combination of rating-based methods can be enabled in the application configuration screen.

When a task is created, a rating for each type of enabled selection criteria is calculated for each available agent. The agent whose total rating is highest is considered for auto-assignment.

The settings for the auto-assignment weighting properties, found in **Security Incident** &gt; **Administration** &gt; **Properties**, are included in the rating calculations.

These values help you prioritize which auto-assignment selection criterion is more important to your organization. Set the priority values between 1 \(less important\) and 10 \(important\).

For an example of how the weighting properties affect agent ratings, see [Agent auto-assignment using multiple selection criteria](r_AgentAssignment.md#auto-agent-mult-criteria).

### On-call scheduling

The On-Call Scheduling application helps you to ensure that dedicated support team members are available to resolve issues as they arise. You can set up on-call schedules, roster rotations, and escalation policies, escalate notifications for a group, and determine the current contact for an escalation. The application identifies the assigned and available member of a support group, for example, when assigning an incident. See On-Call Scheduling for more information. On-call scheduling for Security Incident Response works the same way.

### Agent auto assignment using location

Agents can be auto-assigned based on the home location in their user record and the location of the tasks.

Auto-assignment by location is performed when the **Auto-selection of agents will consider location of agents configuration** option is enabled.

When a task \(security incident or response task\) is created, the agent closest to the task location is considered for the task. If the application is configured so that only location is considered, the closest agent is auto-assigned the task.

When a task is created, agent locations are compared to the following ranges to determine each agent location rating.

|Distance \(mi.\) from agent to task|Rating|
|-----------------------------------|------|
|0 to 0.1|1|
|0.11 to 0.5|0.9|
|0.51 to 5|0.7|
|5.1 to 10|0.5|
|10.1 to 20|0.4|
|20.1 to 30|0.3|
|30.1 to 40|0.2|
|40.1 to 100|0.1|
|&gt;100|0|

If the application is configured to use other selection criteria, such as skills, time zone, or schedule, the ratings of all selection criteria are weighted and summed up. The agent with the highest overall rating is auto-assigned for the task. See [Agent auto-assignment using multiple selection criteria](r_AgentAssignment.md#auto-agent-mult-criteria) for details.

### Agent auto-assignment using skills

Agents can be auto-assigned based on their skills and the skills required to perform the task. Assign skills to their user records using **Skills** &gt; **Users**.

Auto-assignment by skills can be performed when the **Auto-selection of agents for tasks requires them to have skills** configuration option is set to **all** or **some**.

When a task that includes skills is auto-assigned, an agent's skills are compared with the skills required to perform the task. A rating is calculated based on the skills configuration option. If the option is set to **some**, the agent with the closest skills match is auto-assigned the task. If the option is set to **all**, only agents who possess all the required skills are considered. If no agents possess all the skills required to perform the task, no one is auto-assigned.

A skills rating is calculated as:

Skills\_agent/Skills\_task

Where:

-   Skills\_agent is the number of skills possessed by the agent that match the skills required for the task.
-   Skills\_task is the total number of skills required for the task.

For example, if a task requires four skills, and Agent A possesses three of them and Agent B possesses two of them:

-   Agent A skill rating = 3/4 or 0.75
-   Agent B skill rating = 2/4 or 0.5

If the application is configured to use other selection criteria, such as location or time zone, the ratings of all selection criteria are weighted and summed up. The agent with the highest overall rating is selected for the task. See [Agent auto-assignment using multiple selection criteria](r_AgentAssignment.md#auto-agent-mult-criteria) for details.

### Agent auto-assignment using time zones

Agents can be auto-assigned based on the time zone defined in their user records and the time zone of the tasks.

If the **Auto-selection of agents will consider time zone for the task** configuration option is enabled, auto-assignment by time zone can be performed.

When a task is created, agents in the time zone closest to the task time zone are considered for the task. If the application is configured so that only time zone is considered, only an agent in the same time zone can be auto-assigned the task.

**Note:** It is important that the time zones for the agent and the task set correctly.

When a task is created, agents are rated based on the time zone of the task and the time zone of the agent using the following formula:

1 - \[abs\(Task\_tz – Agent\_tz\) ÷ 12\]

where:

-   abs is the mathematical function to compute the absolute value.
-   Task\_tz is the offset between the time zone of the task and GMT.
-   Agent\_tz is the offset between the time zone of the agent and GMT.

For example, a task is created in New York City \(GMT-4\), and two agents are available to perform the task, one in Los Angeles \(GMT-7\) and one in Paris, France \(GMT+1\).

The rating of the agent in Los Angeles is calculated as:

1 - abs\(\(-4\) - \(-7\)\) ÷ 12 or 0.75

The rating of the agent in Paris is calculated as:

1 - abs\(\(-4\) - \(+1\)\) ÷ 12 or 0.58

So if the auto-assignment of the task is based on the time zone alone, it’s assigned to the agent from Los Angeles.

If the application is configured to use other selection criteria, such as skills or location, the ratings of all selection criteria are weighted and summed. The agent with the highest overall rating is selected for the task. See [Agent auto-assignment using multiple selection criteria](r_AgentAssignment.md#auto-agent-mult-criteria) for the details.

### Agent auto-assignment using group coverage areas

Agents can be auto-assigned based on the group coverage area defined in their user records.

### Agent auto-assignment using multiple selection criteria

When a task is created, the agents ratings are calculated. For more information, see:

-   [Agent auto assignment using location](r_AgentAssignment.md#auto-agent-location)
-   [Agent auto-assignment using skills](r_AgentAssignment.md#auto-agent-skills)
-   [Agent auto-assignment using time zones](r_AgentAssignment.md#auto-agent-timezones)

Auto-assignment is based on the following calculation:

\(Criteria\_1 rating x Criteria\_1 weight\) + \(Criteria\_2 rating x Criteria\_2 weight\) + \(Criteria\_3 rating x Criteria\_3 weight\) / Number of criteria types used where:

Number of criteria types used = 1, 2, or 3 depending on the location, skill, and time zone settings used.

This example calculates agent auto-assignment based on location and skills. The example is based on the following assumptions.

-   The **Auto-selection of agents will consider location of agents** configuration option is enabled for the application.
-   The **Auto-selection of agents requires them to have some of the required skills for the task** configuration option is enabled for the application.
-   The **Skills Weight** property is set to 10 for the application.
-   The **Location Weight** property is set to 5 for the application.
-   Agents A and B are available to perform a task, and the task requires four specific skills.
-   Agent A location is 5 miles from the site of the task and possesses three of the four required skills.
-   Agent B' location is one-quarter mile from the site, and possesses two of the required skills.

Auto-assignment for the agents uses this calculation: `[(Location rating x Location weight) + (Skills rating x Skills weight)]/ 2`

-   The auto-assignment calculation for Agent A is: `[(0.7 x 0.5) + (0.75 x 1)]/ 2 = 0.55`
-   The auto-assignment calculation for Agent B is: `[(0.9 x 0.5) + (0.5 x 1)]/ 2 = 0.475`

In this example, Agent A is auto-assigned the task.

### Agent assignment using Advanced Work Assignment \(AWA\)

You can configure Advanced Work Assignment to automatically assigns security incidents to your security analysts, based on their availability, capacity, and optionally, skills. AWA pushes work to qualified security analysts using work item queues, routing conditions, and assignment criteria that you define.

