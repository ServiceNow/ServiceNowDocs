---
title: Configure data permissions for AI skills
description: Add the user roles for the skill to specify the roles that AI uses to access data while performing a task. The user roles control the information that AI can read, update, or share, based on the permissions of the selected roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cmpro-conf-roles-skills.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist in Contract Management, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure data permissions for AI skills

Add the user roles for the skill to specify the roles that AI uses to access data while performing a task. The user roles control the information that AI can read, update, or share, based on the permissions of the selected roles.

## Before you begin

Role required: admin

## About this task

AI skills use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md) to determine the data that the roles can access.

In Contract Management Pro - Prime, the following roles are configured with the base system to provide necessary data access to the AI skills.

-   sn\_cm\_gen\_ai.ai\_contract\_fulfiller
-   sn\_lg\_cnt.contract\_fulfiller
-   sn\_lg\_ops.request\_fulfiller
-   sn\_cm\_core.contract\_fulfiller
-   contract\_manager
-   sn\_lg\_cnt.contract\_owner
-   sn\_cm\_obligation.obligation\_fulfiller

You must configure the necessary roles for your workspace to ensure that skills can access all the required information.

## Procedure

1.  Select the All ****menu and enter `sys_agent_access_role_configuration.list` in the navigation filter.

    The Agent Access Role Configurations table appears.

2.  Open the skill that you want to configure.

3.  In the **Role List** field, select the lock icon \[Omitted image "wsd-unlock-connectors-list-icon.png"\] Alt text:.

4.  In the search field, search for the role that you want to add.

5.  Select the desired role from the search results.

    The selected role is added to the **Role List** field.


**Parent Topic:**[Configure Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/confg-na-in-cmpro.md)

**Related topics**  


[Select large language models for use cases in Now Assist in Contract Management]()

[Configuring contract metadata extraction]()

[Configuring contract analysis]()

[Configuring contract obligation extraction]()

[Configuring agentic workflows in Now Assist in Contract Management]()

[Post-upgrade steps for Now Assist in Contract Management]()

