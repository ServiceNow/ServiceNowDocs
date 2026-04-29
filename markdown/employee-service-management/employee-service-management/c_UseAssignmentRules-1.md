---
title: Assignment and matching rules in HR
description: The base system uses the automatic case assignment feature to assign an HR case to an agent. It attempts to assign an agent with the least number of cases assigned, has the skills required by the case, and matches the location of the subject person.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Assignment and matching rules in HR

The base system uses the automatic case assignment feature to assign an HR case to an agent. It attempts to assign an agent with the least number of cases assigned, has the skills required by the case, and matches the location of the subject person.

## Auto Assign business rule

HR Case has a business rule called Auto Assign that invokes matching rule logic.

When auto assignment is triggered, the matching rules logic obtains a list of agents. The number of agents returned is based on a parameter that specifies the length of the list. The default is one.

**Note:** For specific HR services, the auto-assignment functionality can be skipped. See Case options in [Configure an HR service](../task/configure-hr-service.md).

## Matching Rules

HR assignment rules use the Resource Matching Engine \[com.snc.matching\_rule\] plugin that is activated with the Human Resources Scoped App: Core \[com.sn\_hr\_core\] plugin. You can specify a table and a condition. By default, the base system sets an assignment group for each table and leaves the Assigned to field empty.

For HR cases that meet these conditions, the hr\_AssignmentAPI script include is called to return a list of agents that are eligible for assignment. See [Add or modify a matching rule](../task/CreateModMatchingRule.md).

**Note:** The base system provides matching rules for every COE table and HR task table.

Each HR table and task in the base system have two matching rules:

-   Agents by skills and country
-   Agents by skills

The higher priority \(lower execution order\) rule for each pair is the match by skills and country.

-   If this matching rule does not find eligible agents, then the condition of the lower priority rule is still true and attempts to match by skills alone.
-   If the higher priority rule finds an agent, the assigned to field is no longer empty and the secondary rule does not match.
-   Either the getAgentsByCountryAndSkillsOrderLeastLoaded or getAgentsBySkillOrderLeastLoaded in the hr\_AssignmentAPI script include are called.

## Assignment script includes

The hr\_AssignmentAPI passes the call through to the hr\_AssignmentUtil script include to reduce upgrade issues. Rather than update hr\_AssignmentUtil, you can add to hr\_AssignmentAPI or another customer script include.

The getAgentsByCountryAndSkillsOrderLeastLoaded or getAgentsBySkillOrderLeastLoaded in the hr\_AssignmentAPI script include looks for the least ordered by country and skills.

-   These scripts also look at the agents in the assignment group.
-   They then look for agents that have the required skills for the case and are in the same country as the subject person.
-   The list of agents that are returned are sorted according to case assignment load defined as active cases of type HR case \(or extension\) or active HR tasks.

Auto assignment for HR tasks is slightly different than HR cases.

-   The list of possible agents for an HR task is generated like an HR case.
-   But, after ordering the list, the task is checked for a parent HR case and if the agent assigned is on the list.
-   If it is, the agent is placed at the top of the list ignoring case load.

## Required skills

If you have more than one HR department, you can remove the HR group assignment from the HR template and use assignment rules to assign the HR group. For example, if you have HR departments in both the U.S. and German offices, you can create an HR group for each office. You set up assignment rules to assign the HR group based on the location of the employee who submitted the HR case.

If your organization is using HR skills to qualify HR case assignments, ensure that the assigned user or group members have the required skills. To determine whether skills are being used and assigned, check the following configuration options.

-   **HR Administration** &gt; **HR Services** &gt; **HR Templates**: Look at the template that corresponds to the assignment rule to see what skills, if any, are required.
-   **HR Administration** &gt; **Manage Roles** &gt; **Manage HR Skills**: Find the HR user assigned to the case and click the **Skills: \#** button to see whether the required skill is assigned. If not, check the box to assign it, and click **Save**.

Refer to [Create rules to route and assign customer service cases](https://www.servicenow.com/docs/access?context=c_CaseRouting&version=australia&pubname=australia-customer-service-management&ft:locale=en-US) for more information on matching and assignment rules.

-   **[Add or modify an HR assignment rule](../task/t_CreatingAnAssignmentRule.md)**  
Assignment rules are used to assign the HR group when it is not assigned from the catalog item template. You can create HR assignment rules as needed.
-   **[Test an assignment rule](../task/t_TestingAssignmentRules.md)**  
You can test a new assignment rule to verify that it works as intended.
-   **[Add or modify a matching rule](../task/CreateModMatchingRule.md)**  
You can add or modify a matching rule to assign HR cases to specific users or groups.

**Parent Topic:**[HR Service Delivery case assignment](hr-case-assignment.md)

