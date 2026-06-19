---
title: Deny-by-default ACL configuration
description: The ServiceNow AI Platform enforces a deny-by-default ACL \(Access Control Lists\) configuration for AI agentic types on freshly reset instances, for any AI agents and agentic workflows that don't have an individual ACL configured to reduce unauthorized access risks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/aia-acl-configuration.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 5
breadcrumb: [Security for AI agents, Configure, Now Assist AI agents, Enable AI experiences]
---

# Deny-by-default ACL configuration

The ServiceNow AI Platform enforces a deny-by-default ACL \(Access Control Lists\) configuration for AI agentic types on freshly reset instances, for any AI agents and agentic workflows that don't have an individual ACL configured to reduce unauthorized access risks.

## Configure ACLs in AI Agent Studio

ACLs configured in the AI Agent Studio for AI agents and agentic workflows are role-based and of the Allow If type:

-   **Allow-If**: Grants access to data or resources when any of the specified conditions in the ACL are met. Allow If ACLs don't prevent other ACLs from granting access to the same resource even if it that specific ACL itself doesn't grant access.
-   **Deny-Unless**: Grants access only when the invoking user identity meets all the specified conditions. No other ACLs can override or grant access to that resource once a Deny Unless ACL is in place. This is available when configuring ACLS in the ACL \[sys\_security\_acl\] table and not in the AI Agent Studio.

There are three possible options for ACLs created in AI Agent Studio:

-   **Any authenticated user**: Grants access to any user who is authenticated on the instance, regardless of the role.
-   **Users with specified roles**: The default ACL option that requires you to select the specific roles required to invoke an AI agent or an agentic workflow.

    **Note:** As the ACLs are Allow If ACLs, any user with at least one of the roles will be able to invoke the AI agent or agentic workflow.

-   **Public**: Grants access to all users, including guests who aren’t signed in.

Each AI agent and agentic workflow must have its own unique ACL.

-   To configure an ACL in the AI Agent Studio for an AI agent, see the [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aia.md) guided setup.
-   To configure an ACL for an agentic workflow, see the [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md) guided setup.

**Note:** If there are conflicting security requirements between agentic workflows, AI agents, and AI agent tools, or if the invoking user meets the criteria for some ACLs but not others, your agentic AI fails to execute. When configuring these security settings, consider all aspects of the agentic system- including the agentic workflow, AI agents, and tools.

## Security checks on AI Agent Studio

To inform users about security checks on the agentic system, the platform provides the following notifications in the AI Agent Studio interface:

-   AI Agent Studio Overview page: The AI Agent Studio overview page displays a warning when agents or agentic workflows don't have explicit ACLs configured on the instance.

    \[Omitted image "acl-warning-aias.png"\] Alt text: AI Agent Studio overview page displaying the number of AI agents and agentic workflows that don't have the access control lists configured.

-   AI agent guided setup: The AI agent guided setup page displays a warning banner when that agent doesn't have the required ACLs configured.

    \[Omitted image "acl-warning-aia.png"\] Alt text: An AI agent guided setup page displaying a warning banner when no ACLs are configured.

    **Note:** To configure access control lists for an AI agent, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aia.md).

-   Agentic workflow guided setup: The agentic workflow agent guided setup page displays a warning banner when that agentic workflow doesn't have the required ACLs configured.

    \[Omitted image "acl-warning-aw.png"\] Alt text: An agentic workflow guided setup page displaying a warning banner when no ACLs are configured.

    **Note:** To configure access control lists for an agentic workflow, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aw.md).


These warnings indicate that ACLs are missing and should be configured to verify secure and uninterrupted operation. Users who have already switched to deny-by-default and users who still use wildcard ACLs will both see these warnings. For wildcard ACL users, the warnings are informational.

## ACL types

The AI access control changes brought in five new ACL types that default to allow access, expanding the platform attack surface. The ServiceNow AI Platform enforces a deny-by-default directive for these agentic ACL types on the freshly reset instances. This configuration verifies that records without explicit ACLs aren't inadvertently exposed, aligning the platform with secure-by-default best practices for AI agentic components.

The ACL types are:

-   `gen_ai_agent`
-   `gen_ai_workflow`
-   `gen_ai_skill`
-   `Flow`
-   `flow_action`

## How deny-by-default enforcement works

The **Security Attribute** field value for AI Agent and agentic workflow on the Access Controls table \[sys\_security\_acl\] is set to **Never**, enforcing the deny behavior and leaving the **Decision Type** field value as is, that is, **Allow If**. This configuration verifies that if an AI component already has a primary ACL in place, access continues to be governed by that ACL. The backup \(wild card\) ACLs deny access only when no primary ACL is present. The old wildcard ACLs allow users with agents that predate the availability of access controls in agentic products to continue to run their agents, but that general guidelines is to implement deny by default in all instances. The replacement means that the AI agents and agentic workflows must have explicit ACL entries to operate. Without explicit ACLs, access is denied by default.

**Note:** The enforcement applies only to the freshly reset instances. Any instances that aren't reset aren't affected by this configuration change.

## Scope and applicability

The deny-by-default ACL configuration applies under the following conditions:

-   The instance is a freshly reset instance.
-   The ACL type is one of the five agentic types.
-   The existing ACL record uses a wildcard \(`*`\) pattern.

## Security benefits

Enforcing deny-by-default ACLs for agentic types provides the following security benefits:

-   Reduces the risk of unauthorized access to AI agents and agentic workflows resulting from permissive wildcard ACLs.
-   Verifies that records without explicit ACL entries aren't inadvertently exposed.
-   Aligns the platform with secure-by-default principles for AI agentic components.
-   Provides a clear, auditable ACL model for agentic workflows and AI agents.

