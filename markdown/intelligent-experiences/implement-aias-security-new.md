---
title: Implement access control in AI Agent Studio
description: Implement security in AI Agent Studio through access control lists \(ACLs\), user identities, and role filtering with the access control-based security measures in the agentic system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/implement-aias-security-new.html
release: australia
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 9
keywords: [agentic AI Security, ACLs in AI agents]
breadcrumb: [Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Implement access control in AI Agent Studio

Implement security in AI Agent Studio through access control lists \(ACLs\), user identities, and role filtering with the access control-based security measures in the agentic system.

## Security for AI agents

Access controls for agentic AI on the ServiceNow AI Platform comprises the major aspects: determining which users can access agentic AI resources and what access each of those resources has once invoked. These aspects are controlled through three main components: access control lists \(ACLs\), user identities and role filtering. The interaction between these components at the agentic workflow, AI agent, and tool levels within AI Agent Studio influences their overall security and functionality.

## Access Control Lists \(ACLs\)

The access control lists \(ACLs\) in AI agents determine which role\(s\) a user must have to be allowed to invoke an agentic workflow or an AI agent. ACLs must be configured individually for each agentic workflow, AI agent, external AI agent, and certain AI agent tools such as generative AI Skills, Flows, and Flow Actions.

ACLs configured in the AI Agent Studio for are role-based and of the Allow If type:

-   **Allow-If**: Grants access to data or resources when any of the specified conditions in the ACL are met. Allow If ACLs don't prevent other ACLs from granting access to the same resource even if it that specific ACL itself doesn't grant access.
-   **Deny-Unless**: Grants access only when the invoking user identity meets all the specified conditions. No other ACLs can override or grant access to that resource once a Deny Unless ACL is in place. This is available when configuring ACLS in the ACL \[sys\_security\_acl\] table and not in the AI Agent Studio.

There are three possible options for ACLs created in AI Agent Studio:

-   **Any authenticated user**: Grants access to any user who is authenticated on the instance, regardless of the role.
-   **Users with specified roles**: The default ACL option that requires you to select the specific roles required to invoke an AI agent or an agentic workflow.

    **Note:** As the ACLs are Allow If ACLs, any user with at least one of the roles will be able to invoke the AI agent or agentic workflow.

-   **Public**: Grants access to all users, including guests who aren’t signed in.

    **Note:** Understand that this configuration should be used sparingly and only when needed.


**Note:**

-   ACLs configured in AI Agent Studio only determine the roles required for users to invoke an agentic workflow or an AI agent. They don't determine the access that the agentic workflow or an AI agent has once it’s invoked.
-   For an agentic workflow or AI agent to successfully execute, the invoking user \(or relevant AI user\) must meet the criteria of all of the ACLs of any downstream components which have their own ACLs and are assigned to the agentic workflow or AI agent \(even if the specific execution might not need to invoke all of those AI agents or tools\). Therefore:
    -   If there are conflicting security requirements between agentic workflows, AI agents, and AI agent tools, your agentic AI fails to execute.
    -   The same occurs if the invoking user meets the criteria for some ACLs but not others. This includes components assigned to the agentic AI that might not be required for the specific execution.
-   When configuring these security settings, consider all aspects of the agentic system- including the agentic workflow, AI agents, and tools.

## User identities

After configuring the access control lists \(ACLs\), you must configure the User identity \(also called as **Run as**\) which the AI agent or agentic workflow will run as during execution.

After configuring the access control lists \(ACLs\), you must also configure the user identity \(also called as Run as\) which the AI agent or agentic workflow will run as during execution.

The user identity determines which user the AI agent or an agentic workflow operates as during execution, and therefore the data it can access and the actions it can take, depending on the roles assigned to the user identity.

**Note:** Each agentic workflow and AI agent has its own user identity configuration.

There are two possible user configurations to select from:

-   **Dynamic user**: The user identity of the person or resource \(automated trigger/agentic workflow/parent agent\) which invokes the execution of an AI agent or an agentic workflow. The roles assigned to the agentic workflow or AI agent will change dynamically depending on the identity of the invoking user.

    **Note:** Dynamic user is the default user identity, and you can use the dynamic user unless there's a specific need that justifies an AI user.

-   **AI user**: A dedicated user identity that the AI agent or an agentic workflow runs as during execution, which has assigned roles that remain consistent regardless of who or how the execution is invoked. For example, an AI agent or an agentic workflow may need to be run with elevated privileges that the dynamic user might not have. If configured as a dynamic user, the execution would fail. However, if the AI agent or agentic workflow is configured to run as an AI user that has the elevated roles assigned to it, the execution will succeed even when invoked by a user with lower privileges.

    **Note:** If you don't have a suitable AI user but want to use the **AI user** identity, you must create a record on the User \[sys\_user\] table. See [Create a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAUser.md) and select **AI user** as the identity type.


## Role filtering

Role filtering restricts the roles that AI agents can inherit from the invoking user to a subset of approved roles. This limits the capabilities of the agent, ensuring it can only use the roles that the builder of the AI agent has specifically permitted, even if the user possesses additional roles.

Role filtering only applies when the agent runs as a dynamic user — because the identity \(and resulting roles\) of the invoking user can't be known in advance. There could be situations in which high-privileged users invoke AI agents that should not run with high privileges. By applying role filtering, the builders of AI agents can make sure that their agents adhere to the Least Privilege Principle. Role filtering is not required when an AI agent runs as an AI user. Since the roles of the AI user are preconfigured and can \(and should\) be set to meet the needs of the specific AI agent – no additional filtering is required to conform to the Least Privilege Principle, which can be controlled entirely by the AI user configurations.

## Deny by Default

The ServiceNow AI Platform enforces a deny-by-default ACL \(Access Control Lists\) configuration certain types of agentic components on newly activated instances. In earlier releases, these record types defaulted to allow access unless an ACL was configured for a specific record. In Australia release, newly activated instances start from a deny-by-default posture instead, so access has to be configured explicitly by creating an ACL for the specific record, rather than inherited through permissive defaults. This applies to any AI agents and agentic workflows that don't have an individual ACL configured, reducing unauthorized access risks.

The deny-by-default enforcement works as follows: The **Security Attribute** field value for AI Agent and agentic workflow on the Access Controls table \[sys\_security\_acl\] is set to **Never**, enforcing the deny behavior and leaving the **Decision Type** field value as is, that is, **Allow If**. This configuration verifies that if an AI component already has a primary ACL in place, access continues to be governed by that ACL. The backup \(wild card\) ACLs deny access only when no primary ACL is present. The old wildcard ACLs allow users with agents that predate the availability of access controls in agentic products to continue to run their agents, but that general guidelines is to implement deny by default in all instances. The replacement means that the AI agents and agentic workflows must have explicit ACL entries to operate. Without explicit ACLs, access is denied by default.

**Note:** The enforcement applies only to the newly activated instances. Any instances that are upgraded to Australia release from previous releases aren't automatically affected by this configuration change and the adoption of the deny-by-default ACL configuration will require admins to proactively opt in.

## Security check on AI Agent Studio

To inform users about security checks on the agentic system, the platform provides the following notifications in the AI Agent Studio interface:

-   AI Agent Studio Home page: The AI Agent Studio Home page displays a warning when AI agents or agentic workflows don't have explicit ACLs configured on the instance.

    \[Omitted image "acl-warning-aias-home.png"\] Alt text: AI Agent Studio Home page displaying the number of AI agents and agentic workflows that don't have the access control lists configured.

-   AI Agent guided setup: The AI agent guided setup page displays a warning banner when that agent doesn't have the required ACLs configured.

    \[Omitted image "acl-warning-aia-new.png"\] Alt text: An AI agent guided setup page displaying a warning banner when no ACLs are configured.

-   Agentic workflow guided setup: The agentic workflow agent guided setup page displays a warning banner when that agentic workflow doesn't have the required ACLs configured.

    \[Omitted image "acl-warning-aw-new.png"\] Alt text: An agentic workflow guided setup page displaying a warning banner when no ACLs are configured.


## Security mechanisms

Using ACLs, user identities, and role filtering together provides layered security for AI agents.

-   ACLs prevent unauthorized users from reaching and invoking the agent.
-   User identities verify the agent operates under the correct privilege scope at runtime, preventing escalation beyond what the assigned dynamic user permits.
-   Role filtering verifies that agents can't take actions that exceed defined boundaries even when invoking use has that access.

A common source of confusion is assuming that ACLs define agent actions. They don't! ACLs determine who can invoke the agent. The scope of permissible agent actions are determined by the user identity and role filtering. Use the following summary to distinguish the mechanisms:

|Feature|ACLs|User identities|Role filtering|
|-------|----|---------------|--------------|
|Controls|Who can access the agent|Which identity the agent acts as|What the agent can do|
|Applied to|Users, groups, and roles that invoke the agent|The user identity with which the agent executes at runtime|The agent's runtime execution context|
|Security purpose|Restricts agent discoverability and invocation|Determines privilege scope during execution|Restricts agent actions and data access|

|Feature|AI user|Dynamic user|
|-------|-------|------------|
|Definition|A predefined identity the agent runs as|The identity of the agent at runtime which is inherited from the invoking user.|
|Role filtering applies|No|Yes|
|Roles used|Fixed to the AI user's assigned roles|Scoped down by role filtering|
|Identity source|Configured statically|Determined dynamically at runtime|

**Note:** Configuring only one of these mechanisms leaves a gap in the agent's security posture. Therefore, it is necessary to configure the security mechanisms across the AI Agent Studio and other AI components such as generative AI Sills, Flows, and Flow Actions.

For more information, see [Configure access controls across AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-aias-acls.md).

