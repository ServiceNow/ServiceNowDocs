---
title: Configure data permissions for Now Assist skills
description: Add the user roles for a Now Assist skill to specify the roles that Now Assist uses to access data while performing a task. The user roles control the information that Now Assist can read, update, or share, based on the permissions of the selected roles.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure data permissions for Now Assist skills

Add the user roles for a Now Assist skill to specify the roles that Now Assist uses to access data while performing a task. The user roles control the information that Now Assist can read, update, or share, based on the permissions of the selected roles.

## Before you begin

Role required: admin

## About this task

Now Assist skills use [role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) to determine the data that the roles can access.

In Contract Management Pro - Prime, the following roles are configured with the base system to provide necessary data access to the Now Assist skills.

-   sn\_cm\_gen\_ai.ai\_contract\_fulfiller
-   sn\_lg\_cnt.contract\_fulfiller
-   sn\_lg\_ops.request\_fulfiller
-   sn\_cm\_core.contract\_fulfiller
-   contract\_manager
-   sn\_lg\_cnt.contract\_owner
-   sn\_cm\_obligation.obligation\_fulfiller

You must configure the necessary roles for your workspace to ensure that Now Assist skills can access all the required information.

## Procedure

1.  Select the All ****menu and enter `sys_agent_access_role_configuration.list` in the navigation filter.

    The Agent Access Role Configurations table appears.

2.  Open the skill that you want to configure.

3.  In the **Role List** field, select the lock icon ![](../../workplace-connectors/images/wsd-unlock-connectors-list-icon.png).

    ![Role list field used to add new roles.](../image/cmpro-lock-role-list.png "Role list")

4.  In the search field, search for the role that you want to add.

5.  Select the desired role from the search results.

    The selected role is added to the **Role List** field.


**Parent Topic:**[Configure Now Assist in Contract Management](confg-na-in-cmpro.md)

**Related topics**  


[Select large language models for use cases in Now Assist in Contract Management](cmpro-na-manage-llm.md)

[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)

[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

[Post-upgrade steps for Now Assist in Contract Management](cmpro-na-upgrade-steps.md)

