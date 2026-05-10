---
title: Agentic AI security and governance
description: Now Assist AI agents operate securely within the boundaries you define. Layered controls govern who can invoke each agent, what data it can access, how interactions are monitored, and how your organization retains oversight.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 4
---

# Agentic AI security and governance

Now Assist AI agents operate securely within the boundaries you define. Layered controls govern who can invoke each agent, what data it can access, how interactions are monitored, and how your organization retains oversight.

Deploying AI agents introduces security considerations that go beyond standard platform hardening. Agents act autonomously, invoke tools, access data, and make decisions on behalf of users. This requires controls at every layer: who can invoke an agent, what it can access once running, how its actions are logged, and what catches harmful or unintended behavior at runtime.

Now Assist is built on the ServiceNow AI Platform security model. AI agents are subject to the same ACL enforcement, role-based access controls, and domain separation that govern all platform activity. The controls in these sections extend that foundation with capabilities specific to agentic AI. These include identity classification for AI users, role masking to enforce least-privilege during tool execution, and runtime guardrails through Now Assist Guardian. Readiness assessment tools help verify your instance is prepared before agents go to production.

## AI security concepts

<table id="table_udv_5wf_d3c" class="nav-card presentation"><tbody><tr><td>

[Permissions-based access control![](../../../reuse/icons/brand-icons/bus-why-servicenow.svg)Use Agent Role Inheritance, identity types, and granular roles to verify your AI agents have only the permissions they need, and can act only within their intended boundaries.](naai-permissions-based-access-control.md)

</td><td>

[Data protection![](../../../reuse/icons/brand-icons/bus-security.svg)Learn how ServiceNow tools like Key Management Framework, Field Encryption, and Data Classification protect your data, including where it is stored and processed, and how it stays isolated when third-party agents are involved.](naai-data-protection.md)

</td><td>

[Agent traceability and monitoring![](../../../reuse/icons/brand-icons/bus-scan.svg)Use AI Control Tower and agent activity logs to track what your agents do, what data they access, and when, and provide the auditable, explainable records your security and compliance teams require.](naai-auditing-and-monitoring.md)

</td></tr><tr><td>

[Governance and admin safeguards![](../../../reuse/icons/brand-icons/bus-automated-testing-framework.svg)Find guidance on managing roles, policies, and configurations to reduce risk and meet compliance requirements, including HIPAA, GDPR, and NIST.](naai-governance-and-admin-safeguards.md)

</td><td>

[AI threat protection![](../../../reuse/icons/brand-icons/bus-problem-benefit.svg)Learn how Now Assist helps defend against AI-specific threats including offensive content, prompt injection, and sensitive subject detection using Now Assist Guardian.](naai-threat-protection.md)

</td><td>

[External AI agent security![](../../../reuse/icons/brand-icons/bus-community.svg)Learn how to monitor and govern AI agents from external providers, with visibility into third-party data flows and assurances that sensitive data stays properly isolated across your AI ecosystem.](naai-3rd-party-security.md)

</td></tr></tbody>
</table>## AI security products

<table id="table_bm1_dbp_w3c" class="nav-card presentation"><tbody><tr><td>

[Now Assist Guardian![](../../../reuse/icons/brand-icons/bus-trust-in-us.svg)Now Assist Guardian is built on the ServiceNow Small Language Model \(SLM\) and monitors generative AI interactions to detect offensive content, prompt injection attacks, and sensitive topics.](../../now-assist-platform/concept/now-assist-guardian.md)

</td><td>

 

</td><td>

[AI Control Tower![](../../../reuse/icons/brand-icons/ind-telecom-tower.svg)The AI Control Tower is a platform that connects different parts of an organization to speed up the AI adoption.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-control-tower-landing.md)

</td></tr></tbody>
</table>-   **[Permissions-based access control](naai-permissions-based-access-control.md)**  
Use Agent Role Inheritance, identity types, and granular roles to verify your AI agents have only the permissions they need, and can act only within their intended boundaries.
-   **[Data protection](naai-data-protection.md)**  
Learn how ServiceNow security tools such as the Key Management Framework, Field Encryption, and Data Classification work to keep your data secure.
-   **[Agent traceability and monitoring](naai-auditing-and-monitoring.md)**  
Learn how to use tools like AI Control Tower to track, monitor, and report on your AI assets.
-   **[Governance and admin safeguards](naai-governance-and-admin-safeguards.md)**  
Find guidance on preparing your instance for AI deployment, maintaining domain separation, and reducing risk across your Now Assist implementation.
-   **[AI threat protection](naai-threat-protection.md)**  
Learn how Now Assist helps defend against AI-specific threats including offensive content, prompt injection, and sensitive subject detection using Now Assist Guardian.
-   **[External AI agent security](naai-3rd-party-security.md)**  
Learn how to monitor and govern AI agents from external providers, with visibility into third-party data flows and assurances that sensitive data stays properly isolated across your AI ecosystem.
-   **[Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md)**  
Now Assist Guardian is built on the ServiceNow Small Language Model \(SLM\) and monitors generative AI interactions to detect offensive content, prompt injection attacks, and sensitive topics.
-   **[Create and secure an AI agent in Now Assist](naai-tutorial-overview.md)**  
Plan, build, secure, test, and deploy a Now Assist AI agent.

