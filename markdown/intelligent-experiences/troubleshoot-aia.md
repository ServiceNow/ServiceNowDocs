---
title: Troubleshoot AI agents
description: Use this troubleshooting guide to resolve issues with AI agents' roles, testing procedures, silent failure diagnosis and reference resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/troubleshoot-aia.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Reference, AI Agent Studio \(legacy\), Enable AI experiences]
---

# Troubleshoot AI agents

Use this troubleshooting guide to resolve issues with AI agents' roles, testing procedures, silent failure diagnosis and reference resources.

## Required roles assignments

Role assignments control access to AI Agent Studio and determine what tables and tools an agent or an agentic workflow can access.

Each agent comes with predefined user and data roles by default that can be modified by the customer. It is important to understand the difference between these roles, as an AI agent may not function correctly if it lacks the appropriate user or data role assigned. For more information about the default AI agent roles, see the [ServiceNow AI agents library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-landing-page.md).

**Note:** If the customer alters the default user or data roles, it may lead to issues with the agent's functionality and execution.

Some of the individual ServiceNow AI Platform AI agent roles include:

|AI agent|Role or Condition|
|--------|-----------------|
|Issue readiness|sn\_uxc\_gen\_ai.platform\_ai\_issue\_readiness|
|Request status|LoggedIn=true^ORAllowUnauthRolelessAcl=true|
|Domain separation|domain\_admin|
|Access analyzer agent|access\_analyzer\_admin OR user\_admin|

To identify the roles currently assigned to:

-   AI agents: Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and Manage** &gt; **AI Agents**, select an AI agent, and navigate to the **Define security controls** section.

    For more information, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aia.md).

-   Agentic workflows: Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and Manage** &gt; **Agentic workflows**, select an agentic workflow, and navigate to the **Define security controls** section.

    For more information, see [Define security controls for an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-controls-aw.md).


## Diagnose AI agents' failures

-   **Test agents and workflows**

    Test your all your AI agents and agentic workflows to make sure they have the correct access. When an AI agent role does not have required resource access, verify that the agent is assigned the correct role. Verify the role has resource access records for all required tables and confirm that role masking does not override the resource access.

    Supporting tables for diagnosing AI agent's failures:

    -   generative AI Log \[sys\_generative\_ai\_log\] table: The primary resource for diagnosing AI agent failures is the generative AI Log \[sys\_generative\_ai\_log\] table. The table logs agentic execution details, errors, and state transitions that help diagnose role-related failures, permission and workflow issues.
    -   generative AI Configurations \[sys\_generative\_ai\_config\] table: Contains configuration records for AI agents; useful for validating that agent setups are correct before testing failures.
    -   AI Agent memory \[sn\_aia\_memory\] table: Contains the agent memory state and helps test memory-related failures or edge cases.
    -   AI Agent \[sn\_aia\_agent\] table: Verify agent definitions during failure scenarios.
    **Important:** Silent failures that return no values may indicate an underlying access error. You might have access to the agentic workflow, but the AI agent within the workflow may lack necessary permissions. Always test all underlying AI agents individually, not just the workflow, to catch permission gaps that your own access level might mask.

    -   To test an agentic workflow, see [Manually test the execution of an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md).
    -   To test an AI agent, see [Manually test the execution of an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-agent.md).
-   **Review logs**

    Use these columns in the generative AI Log \[sys\_generative\_ai\_log\] table to identify root causes of AI agent and agentic workflow failures. The table records all generative AI activity within your ServiceNow instance, including AI agent invocations, model responses, performance metrics, and errors.

    Common issues include:

    -   Permission and ACL failures
    -   Model endpoint unavailability
    -   Token limit exhaustion
    -   Skill or action failures
    -   Performance degradation
    |Column name|Troubleshooting use|
    |-----------|-------------------|
    |user\_role|Shows what role the agent has; compare to what's required|
    |error\_message|Direct indication of permission versus natural-language mismatch|
    |permission\_denied|Boolean flag to quickly filter permission failures|
    |table\_name|Target table the agent was accessing when it failed|
    |operation\_type|Type of operation attempted: `read`, `write`, `execute`, `query`|
    |action|Shows exactly which step failed \(e.g. "update\_incident", "create\_change", "query\_table"\)|
    |execution\_log|Full context; shows agent's reasoning before failure|
    |acl\_rule|References the specific ACL that denied access|


## Additional resources

Use the following documentation resources for more information:

-   Access control: [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md)
-   To test user access to an:
    -   AI agent: [Test user access to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-access.md).
    -   Agentic workflow: [Test user access to an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aw-access.md).
-   Agent library: [ServiceNow AI agents library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-landing-page.md)
-   Knowledge base: [AI agent advanced scenarios and runtime issues playbook](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3042061).
-   [AI Agents FAQ and Troubleshooting](https://www.servicenow.com/community/servicenow-otto-articles/ai-agents-faq-and-troubleshooting/ta-p/3200454).
-   [Access control Security enhancements for AI agents and Skill Kit](https://www.servicenow.com/community/servicenow-otto-articles/latest-access-control-security-enhancements-for-ai-agents-and/ta-p/3374036).
-   [Common solutions for ServiceNow AI Agent, MCP Server, and AI Agent Fabric](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2076278).
-   [Accessing AI Agent Studio after upgrading the ServiceNow Otto AI Agents plugin](https://www.servicenow.com/community/servicenow-otto-for-creator/access-denied-to-ai-agent-studio-after-upgrading-sn-aia-plugin/td-p/3453111).

