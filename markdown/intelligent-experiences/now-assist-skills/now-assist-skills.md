---
title: Now Assist skills
description: Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skills/now-assist-skills.html
release: australia
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 9
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI, Security operations, IT operations, ITSM, IT Service management, Customer service management, CSM, Strategic portfolio management, SPM, Field service management, FSM, Financial services operations, FSO, HR Service Delivery, HRSD, Sourcing and procurement operations, SPO]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills

Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.

The following sections describe the available Now Assist skills.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see .\)

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/ai-native-sku-overview.md).

## Now Assist skills overview

Now Assist skills are discrete, reusable generative AI capabilities that perform a specific type of work within a workflow. A skill focuses on a single, well‑defined task, such as summarizing content, generating text, analyzing records, or providing recommendations, and returns an output that can be reviewed, used, or acted on by a user or workflow.

Skills are the foundational AI building blocks used across Now Assist experiences, workflows, and products. They enable AI‑powered assistance without requiring custom model development.

## What a skill does

Skills are designed to:

-   Perform one focused action

    A skill handles a specific task, such as summarizing a record, generating a response, or analyzing data, rather than completing an end to end workflow.

-   Operate within an existing workflow or product context

    Skills are used in the context of where users work, such as records, tasks, forms, or panels, and act on the data available in that context.

-   Use generative AI safely and securely

    Skills run on the ServiceNow AI Platform and respect data boundaries, access controls, and domain separation.

-   Return usable output

    The output of a skill can be reviewed by the user, edited if needed, or used to support downstream actions in a workflow.


## How users interact with skills

Depending on the product and configuration, users can interact with skills in different ways:

-   Triggering a skill from a contextual UI, such as a panel or record.
-   Using a skill as part of a workflow driven experience.
-   Receiving output generated automatically by a workflow or agentic process.

In all cases, skills are designed to assist, not replace, user decision making by reducing manual effort.

**Note:** Some skills are turned on by default, depending on the product and release. Other skills require explicit enablement or configuration in the Now Assist admin experience. Deactivating certain skills may impact dependent features or workflows.

## Available skills by workflow

<table id="table_yz3_mqd_dbc"><thead><tr><th class="filter">

Workflow

</th><th class="filter">

Product

</th><th>

Available skills

</th></tr></thead><tbody><tr><td>

Technology

</td><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

-   Acceptance criteria generation
-   Docs summarization
-   Doc generation
-   Task generation

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Configuration item \(CI\) summarization
-   Manage duplicate CIs
-   Service Graph Connector diagnosis

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Core Business Suite \(CBS\)

</td><td>

-   Next Best Action
-   Error Resolution

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   ADR DOC summarization and actions
-   Business application insights
-   Create diagram from image
-   Diagram change analysis
-   Refine text
-   Register a business application
-   Register a digital integration

</td></tr><tr><td>

Technology

</td><td>

Operational Sustainability Management \(formerly Environmental, Social, and Governance\)

</td><td>



</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Generate hardware asset insights

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Common control objective creation
-   Control objective impact analyzer
-   
-   Issue summarization
-   Recommendations for regulatory alert impacted areas
-   Recommendation of similar control objectives
-   Regulatory alert summarization
-   Regulatory alert impacted citations
-   Regulatory alert impacted control objectives
-   Regulatory alert impacted controls
-   Regulatory alert impacted policies
-   Risk assessment summarization
-   Risk event summarization
-   Risk event summarization in the classic UI


</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Alert analysis
-   Alert investigation
-   Analyze service health
-   Analyze service observability dashboard
-   LEAP installer
-   Service Mapping Candidate
-   Service mapping candidates Impact

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Catalog task summarization
-   Change request risk explanation
-   Change request summarization
-   Chat reply recommendation
-   Chat summarization
-   Email recommendation
-   Incident assist
-   Incident sentiment analysis
-   Incident summarization
-   Investigate boot time issues
-   Investigate Zoom call quality issues
-   KB generation
-   Release notes generation
-   Request activity response generation
-   Request summarization
-   Requested item activity response generation
-   Requested item summarization
-   Resolution notes generation
-   Sidebar discussion summarization
-   Suggested steps generation

</td></tr><tr><td>

Technology

</td><td>



</td><td>

Search for a related record

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   OT incident summarization
-   OT resolution notes generation

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Control objective impact analyzer
-   Common control objective creation
-   Recommendation of similar control objectives
-   Risk assessment summary

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Correlation insights generation
-   Generate content for shift handover
-   Post-incident analysis
-   Resolution notes generation
-   Security incident quality assessment
-   Security incident recommended actions
-   Security incident resolution plan
-   Security incident summarization
-   Security operations metrics analysis

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Contract entitlement data extraction
-   Error log summarization
-   Error resolution recommendation
-   Publisher compliance summarization
-   Product compliance summarization
-   Product match reviewer
-   Recommended actions
-   Software normalization
-   SaaS user resolution

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Create a demand
-   EAP doc summarization
-   Identify similar records
-   Demand summarization
-   Goal insights
-   Multi feedback summarization
-   Planning item doc summarization
-   Project doc summarization
-   Project insights generation
-   Refine records
-   Story generation
-   Target generation
-   Write planning item

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   TPRM issue summarization
-   TPRM issue management recommendation

</td></tr><tr><td>

Technology

</td><td>



</td><td>

TISC case summarization

</td></tr><tr><td>

Technology

</td><td>



</td><td>

-   Approval recommendation
-   Now Assist recommendation
-   SEM insights
-   SPC setup connector
-   Suggest vulnerability solutions
-   Vulnerable item deduplication

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   Activity response generation
-   Automated quality assurance
-   Case summarization
-   Chat recommendation
-   Chat summarization
-   Customer summarization
-   Email recommendation
-   KB generation
-   Resolution notes generation
-   Sentiment analysis case
-   Sentiment analysis dashboard
-   Sentiment analysis for email interactions
-   Sidebar summarization
-   Special handling notes summarization
-   Suggested steps generation
-   Trending topics dashboard

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   KB generation
-   Sidebar summarization
-   Work order task summarization

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   Case summarization
-   Disputes intake via Virtual Agent
-   Customer profile summarization
-   Customer interaction context summary
-   Insurance customer profile summarization
-   Insurance interaction context summary

</td></tr><tr><td>

Customer

</td><td>



</td><td>

Enhance non conformance description

</td></tr><tr><td>

Customer

</td><td>



</td><td>

Order summarization

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   Government case summarization
-   Chat summarization

</td></tr><tr><td>

Customer

</td><td>



</td><td>

Opportunity summarization

</td></tr><tr><td>

Customer

</td><td>



</td><td>

-   Account onboarding case summarization
-   Customer play summary
-   Customer service summary
-   Engagement summary
-   Internal play summary
-   KB generation
-   Resolution notes generation
-   Risk signal and issues summary
-   Service problem case summarization
-   Success initiative summary
-   Test summarization
-   Touchpoint summary
-   Transform mapping assist

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Requested item summarization for approvals
-   Request summarization for approvals
-   Case summarization for approvals

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Incident summarization
-   H&amp;S Action Planner

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Case summarization
-   Chat reply recommendation
-   Chat summarization
-   Email recommendation
-   KB generation
-   Employee information summarization
-   Resolution notes generation
-   Sentiment analysis for HR case
-   Sentiment analysis for HR task
-   Sidebar discussion summarization

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Conversational intake for Conflict of Interest request
-   Get category of the legal request
-   Legal matter summarization
-   Legal request summarization
-   Triage legal request AI Search
-   Triage legal request capability

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Contract analysis
-   Contract metadata extraction
-   Contract obligation extraction
-   Contracts query classifier
-   Conversational contract search and insights

</td></tr><tr><td>

Employee

</td><td>



</td><td>

-   Reserve Space Virtual Agent topic
-   Workplace Case Summarization

</td></tr><tr><td>

Creator

</td><td>



</td><td>

-   App generation
-   
-   Catalog item generation
-   App summary generation
-   
-   Code Assist autocomplete
-   Code Assist edit
-   Code assist summarization
-   Code Assist generation
-   Event handler generation
-   
-   
-   
-   
-   
-   Mobile card generation
-   Playbook generation
-   Playbook generation with images
-   Playbook recommendations
-   Playbook summarization
-   Process inefficiency highlights
-   
-   Spoke generation
-   Test generation
-   Work notes analysis

</td></tr><tr><td>

Platform

</td><td>

[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/platform-now-assist-landing.md)

</td><td>

-   [Article optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-article-optimization.md)
-   [Complete record generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Conversational Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/conversational-help-skills.md)
-   Document summarization
-   Dynamic Guidance
-   [Extract information from documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-extract-information-from-documents.md)
-   [GAF skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/configure-gaf.md)
-   [Knowledge content recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-platform-knowledge.md)
-   [Multimodal chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/docintel-exploring-now-assist.md)
-   [Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-global-navigation.md)
-   [New column data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md)
-   [Potential knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/potential-knowledge-gaps.md)
-   [Requester approval checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/service-portal-approval-checklist-skill.md)
-   [ServiceNow Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-lens/servicenow-lens-landing-page.md)
-   [TextToResult](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md)

</td></tr><tr><td>

Platform

</td><td>



</td><td>

Dashboard summarization

</td></tr><tr><td>

Data and Analytics

</td><td>

Now Assist skills for Analytics

</td><td>

AI Data Explorer skills-   Analytics exploration
-   Exploration summarization
-   Refine text in exploration

Query Generation skills-   Analytics query generation
-   Analytics insight generation
-   Analytics follow up generation
-   Analytics hidden insight generation

Skills installed by default with Platform:

-   Dashboard and visualization export
-   Data visualization generation

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>



</td><td>

-   Invoice case summarization
-   Purchase order summarization

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>



</td><td>

-   Email response
-   Sentiment analysis
-   Supplier case summarization
-   Supplier summarization
-   Supplier performance summarization

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>



</td><td>

-   Negotiation summarization
-   Procurement case summarization
-   Purchase requisition summarization
-   Sourcing event summarization
-   Sourcing request summarization

</td></tr><tr><td>

App Engine

</td><td>



</td><td>

Custom app record summarization

</td></tr><tr><td>

Impact

</td><td>

The Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   
-   
-   
-   

</td></tr><tr><td>

Vault

</td><td>



</td><td>

-   Check role access
-   Generate custom data pattern
-   Schedule Data Discovery job

</td></tr><tr><td>

Other

</td><td>



</td><td>

-   ERP data discovery
-   ERP data query

</td></tr></tbody>
</table>