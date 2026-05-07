---
title: Create and secure an AI agent in Now Assist
description: Plan, build, secure, test, and deploy a Now Assist AI agent.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 3
breadcrumb: [Agentic AI security and governance]
---

# Create and secure an AI agent in Now Assist

Plan, build, secure, test, and deploy a Now Assist AI agent.

Use this tutorial to go through the full life-cycle of creating an AI agent on the ServiceNow AI Platform. Security configuration \(controlling access, protecting data, and enabling guardrails\) is integrated at each phase rather than treated as separate steps.

This tutorial is intended for ServiceNow AI Platform administrators and AI developers who are building and deploying AI agents for the first time. It assumes familiarity with the ServiceNow AI Platform but no prior experience building AI agents.

## Before you begin

Before starting this tutorial, verify the following:

-   A Now Assist license that includes AI agents.
-   Administrator access to your instance.
-   You should have the **sn\_aia.admin**, **sn\_nowassist\_admin.nsa\_admin**, and **sn\_generative\_ai.data\_steward** roles assigned to you or users to whom you will delegate tasks. Further details on roles can be found in [Assess readiness](naai-tutorial-assess-readiness.md).

## How the security model works

Reviewing the Now Assist security model before you build can help make configuration decisions easier.

-   **[Access control lists \(ACLs\)](../../contextual-security/concept/access-control-rules.md)**

    Determine who can discover and invoke an agent or agentic workflow. ACLs are configured on the agent itself and are checked before the agent executes.

-   **[User identity](../../general/concept/identity-landing.md)**

    Determines what data the agent can access once invoked. A dynamic user agent inherits the invoking user's roles. An AI user agent runs as a dedicated system user with fixed assigned roles.

-   ****

    Monitors prompts and responses at runtime to detect offensive content, prompt injection attempts, and sensitive subjects. Guardian runs independently of ACLs and user identity.


## Tutorial steps

Complete the following steps in order:

-   **1. [Assess readiness](naai-tutorial-assess-readiness.md)**

    Verify your instance is ready for AI agent deployment and assign the roles needed to build and manage agents.

-   **2. [Plan your agent](naai-tutorial-plan-agent.md)**

    Define your use case, choose between an OOTB and custom agent, and set your success criteria.

-   **3. [Build your agent](naai-tutorial-build-agent.md)**

    Create your agent in AI Agent Studio, configure tools, and set access controls.

-   **4. [Configure security controls](naai-tutorial-configure-security.md)**

    Configure Now Assist Guardian guardrails and data privacy settings.

-   **5. [Test and validate](naai-tutorial-test-validate.md)**

    Test agent execution, verify access controls, and run automated evaluations.

-   **6. [Go live and monitor](naai-tutorial-go-live-monitor.md)**

    Deploy to production and set up ongoing monitoring.


-   **[Assess readiness](naai-tutorial-assess-readiness.md)**  
Verify that your instance is prepared for AI agent deployment, install the required applications, assign the required roles, and classify user identity types before you begin building.
-   **[Plan your agent](naai-tutorial-plan-agent.md)**  
Define your use case, decide between an base system and custom agent, choose an activation model, and set your success criteria before you begin building.
-   **[Build your agent](naai-tutorial-build-agent.md)**  
Create your agent in AI Agent Studio, configure its tools and knowledge sources, and set the access controls that determine who can invoke it and what data it can access.
-   **[Configure security controls](naai-tutorial-configure-security.md)**  
Set up Now Assist Guardian guardrails and data privacy controls to protect your AI agent interactions before testing begins.
-   **[Test and validate](naai-tutorial-test-validate.md)**  
Test your agent's execution and access controls, run automated evaluations, and review Guardian logs before approving the agent for production deployment.
-   **[Go live and monitor](naai-tutorial-go-live-monitor.md)**  
Deploy your agent to production, activate analytics and monitoring, and establish the ongoing review cadence that keeps your agent performing securely over time.

**Parent Topic:**[Agentic AI security and governance](now-assist-security.md)

