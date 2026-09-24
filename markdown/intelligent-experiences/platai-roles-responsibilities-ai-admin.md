---
title: Roles and responsibilities for AI administration
description: Each AI capability on the ServiceNow AI Platform requires specific administrative roles for installation, configuration, and ongoing management. Identifying these roles before implementation helps you plan access and assign accountability for each capability.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-roles-responsibilities-ai-admin.html
release: brazil
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 4
keywords: [AI administration roles, Now Assist roles, AI implementation roles, AI Platform roles and responsibilities]
breadcrumb: [Implementing AI, Getting started with AI, Enable AI Experiences]
---

# Roles and responsibilities for AI administration

Each AI capability on the ServiceNow AI Platform requires specific administrative roles for installation, configuration, and ongoing management. Identifying these roles before implementation helps you plan access and assign accountability for each capability.

AI administration on the ServiceNow AI Platform is distributed across multiple specialized roles rather than a single platform-wide role. Each tool has its own dedicated administrative role. This separation supports least-privilege access and lets organizations assign responsibility to the people closest to each capability.

The sys\_admin role does not automatically grant the following roles. Assign the AI administrative roles directly to the users who require them.

The following table identifies the role required to administer each area of AI implementation. Reviewing the table during planning helps you confirm assignments, request access ahead of activation, and align team members with their administrative responsibilities.

**Note:** Some roles, such as the Now Assist admin, apply to more than one implementation area. A single user can hold multiple administrative roles when their responsibilities span several areas.

<table id="table_roles_by_implementation_area"><thead><tr><th>

Implementation area

</th><th>

Role

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td rowspan="5">

AI policy

</td><td>

[AI steward](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-installed-with.md)

 \[`sn_ai_governance_ai_steward`\]

</td><td>

Manages the platform's data assets and AI capabilities, ensuring data quality, integrity, and ethical use. Implements governance policies to maintain compliance, security, and responsible AI practices across ServiceNow applications and workflows.

</td></tr><tr><td>

[AI asset owner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-installed-with.md)

 \[`sn_ai_asset_mgmt.ai_asset_owner`\]

</td><td>

Drives the development and delivery of AI-powered products, ensuring alignment with business goals and user needs. Defines product vision, manages feature prioritization, and translates business requirements into technical deliverables.

</td></tr><tr><td>

[AI Risk and Compliance Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-installed-with.md)

 \[`sn_grc_ai_gov.ai_risk_and_compliance_manager`\]

</td><td>

Identifies, assesses, and mitigates risks related to AI use within the enterprise. Ensures AI compliance with laws, regulations, and internal standards while addressing issues such as bias, privacy, and transparency.

</td></tr><tr><td>

[AI Risk and Compliance admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-installed-with.md)\[`sn_grc_ai_gov.ai_risk_and_compliance_admin`\]

</td><td>

Configures risk assessment methodologies, risk contribution factors, and impact assessment templates. Defines automation rules for impact assessments, sets up and profiles AI case types, and deletes AI systems.

</td></tr><tr><td>

[Now Assist admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/roles-installed-with-now-assist-admin.md)

 \[`sn_nowassist_admin.nsa_admin`\]

</td><td>

Enables and manages the AI Guardian guardrails within the AI Admin Hub console. Configures detection settings for offensiveness, prompt injection, and sensitive topics, and monitors logs to assess harmful or malicious AI outputs.

</td></tr><tr><td rowspan="2">

Data management

</td><td>

[AI Data Kit admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/data-kit-admin-role.md)

 \[`sn_data_kit.admin`\]

</td><td>

Creates, updates, and publishes datasets in AI Data Kit.

</td></tr><tr><td>

[Knowledge Graph admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-roles.md)

 \[`kg_admin`\]

</td><td>

Designs, manages, and audits Knowledge Graph schemas, including configuring nodes \(tables\), properties \(columns\), and relationships.

</td></tr><tr><td rowspan="2">

Internal and external content search

</td><td>

[AI Search admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/components-installed-ais.md)

 \[`ais_admin`\]

</td><td>

Manages configuration settings for the AI Search application.

</td></tr><tr><td>

[External Content Connectors admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/installed-with-ext-content-connectors.md)

 \[`sn_ext_conn.xcc_admin`\]

</td><td>

Manages configuration and crawl settings for the External Content Connectors application.

</td></tr><tr><td rowspan="2">

Generative AI skills

</td><td>

[Now Assist admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/roles-installed-with-now-assist-admin.md)

 \[`sn_nowassist_admin.nsa_admin`\]

</td><td>

Installs AI plugins, activates skills, and configures generative AI preferences and settings.

</td></tr><tr><td>

[AI Skill Kit admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/na-skill-kit-roles.md)

 \[`sn_skill_builder.admin`\]

</td><td>

Creates, updates, and publishes skills in AI Skill Kit.

</td></tr><tr><td rowspan="3">

Agentic AI

</td><td>

[AI Agent admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md)

 \[`sn_aia_admin`\]

</td><td>

Creates, manages, updates, tests, and deletes AI agents and agentic workflows.

</td></tr><tr><td>

[MCP Client admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mcp-reference.md)

 \[`sn_mcp_client.admin`\]

</td><td>

Administers the MCP client in AI Agent Studio. This role is inherited from the AI Agent admin \[`sn_aia.admin`\] role.

</td></tr><tr><td>

[MCP Server administrator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/installed-mcp-server-console.md)

 \[`sn_mcp_server.admin`\]

</td><td>

Administers the MCP Server Console.

</td></tr><tr><td rowspan="2">

Conversational AI engagement

</td><td>

Virtual Agent

 \[`virtual_agent_admin`\]

</td><td>

Installs ServiceNow Otto for Virtual Agent and sets up and manages assistants in Assistant Designer. Also required for users who create and manage Virtual Agent topics and assets. The admin role can be used in place of this role.

</td></tr><tr><td>

[Now Assist admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/roles-installed-with-now-assist-admin.md)

 \[`sn_nowassist_admin.nsa_admin`\]

</td><td>

Turns on and configures the ServiceNow Otto panel in the AI Admin Hub console.

</td></tr></tbody>
</table>