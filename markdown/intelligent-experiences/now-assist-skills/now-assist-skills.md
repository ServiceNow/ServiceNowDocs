---
title: Now Assist skills
description: Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.
locale: en-US
release: australia
product: Now Assist Skills
classification: now-assist-skills
topic_type: concept
last_updated: "2026-04-27"
reading_time_minutes: 10
keywords: [Now Assist, Now Assist skills, Generative AI, Gen AI, Security operations, IT operations, ITSM, IT Service management, Customer service management, CSM, Strategic portfolio management, SPM, Field service management, FSM, Financial services operations, FSO, HR Service Delivery, HRSD, Sourcing and procurement operations, SPO]
breadcrumb: [Now Assist AI assets, Enable AI experiences]
---

# Now Assist skills

Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows.

The following sections describe the available Now Assist skills.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](../../now-assist-admin/concept/domain-separation-in-the-now-assist-admin-console.md). \(Note that global domain is not the same as global scope. For more information, see Exploring Next Experience pickers.\)

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](now-assist-skills-on-by-default.md).

**Note:** Some workflow skills support Now Assist functionality. Deactivating these skills may negatively impact some features.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](../../ai-implementation/concept/ai-native-sku-overview.md).

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

Now Assist for Configuration Management Database \(CMDB\)

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

Now Assist for Enterprise Architecture \(EA\)

</td><td>

-   ADR DOC summarization and actions
-   Business application insights
-   Diagram change analysis
-   Refine text
-   Register a business application
-   Register a digital integration

</td></tr><tr><td>

Technology

</td><td>

Operational Sustainability Management \(formerly Environmental, Social, and Governance\)

</td><td>

Extract data from utility invoices

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

-   Generate hardware asset insights

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Integrated Risk Management \(IRM\)

</td><td>

-   Common control objective creation
-   Control objective impact analyzer
-   Generate recommendation for similar control objective
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

Now Assist for ITOM

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

Now Assist for IT Service Management \(ITSM\)

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

Operational Technology \(OT\) Manager Foundation

</td><td>

Search for a related record

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Operational Technology Service Management \(OTSM\)

</td><td>

-   OT incident summarization
-   OT resolution notes generation

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Privacy Management

</td><td>

-   Control objective impact analyzer
-   Common control objective creation
-   Recommendation of similar control objectives
-   Risk assessment summary

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Security Incident Response

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

Now Assist for Software Asset Management \(SAM\)

</td><td>

-   Error log summarization
-   Error resolution recommendation
-   Publisher compliance summarization
-   Product compliance summarization
-   Recommended actions
-   SaaS user resolution
-   Contract entitlement data extraction

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Strategic Portfolio Management \(SPM\)

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

Now Assist for Third-party Risk Management \(TPRM\)

</td><td>

-   TPRM issue summarization
-   TPRM issue management recommendation

</td></tr><tr><td>

Technology

</td><td>

Now Assist for Vulnerability Response

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

Now Assist for Customer Service Management \(CSM\)

</td><td>

-   Activity response generation
-   Automated quality assurance
-   Case summarization
-   Chat recommendation
-   Chat summarization
-   Email recommendation
-   KB generation
-   Resolution notes generation
-   Sentiment analysis case
-   Sentiment analysis dashboard
-   Sidebar summarization
-   Suggested steps generation
-   Trending topics dashboard

</td></tr><tr><td>

Customer

</td><td>

Now Assist for Field Service Management \(FSM\)

</td><td>

-   KB generation
-   Sidebar summarization
-   Work order task summarization

</td></tr><tr><td>

Customer

</td><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

-   Case summarization
-   Disputes intake via Virtual Agent
-   Customer profile summarization
-   Customer interaction context summary

</td></tr><tr><td>

Customer

</td><td>

Now Assist for Manufacturing Commercial Operations

</td><td>

Enhance non conformance description

</td></tr><tr><td>

Customer

</td><td>

Now Assist for Order Management

</td><td>

Order summarization

</td></tr><tr><td>

Customer

</td><td>

Now Assist for Public Sector Digital Services \(PSDS\)

</td><td>

-   Government case summarization
-   Chat summarization

</td></tr><tr><td>

Customer

</td><td>

Now Assist for Telecommunications, Media and Technology \(TMT\)

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

Now Assist for Employee Experience

</td><td>

-   Requested item summarization for approvals
-   Request summarization for approvals
-   Case summarization for approvals

</td></tr><tr><td>

Employee

</td><td>

Now Assist for Health and Safety

</td><td>

Incident summarization

</td></tr><tr><td>

Employee

</td><td>

Now Assist for HR Service Delivery \(HRSD\)

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

Now Assist for Legal Service Delivery \(LSD\)

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

Now Assist in Contract Management

</td><td>

-   Contract analysis
-   Contract metadata extraction
-   Contract obligation extraction
-   Contracts query classifier
-   Conversational contract search and insights

</td></tr><tr><td>

Employee

</td><td>

Now Assist for Workplace Service Delivery \(WSD\)

</td><td>

-   Reserve Space Virtual Agent topic
-   Workplace Case Summarization

</td></tr><tr><td>

Creator

</td><td>

Now Assist for Creator

</td><td>

-   App generation
-   Build Agent
-   Catalog item generation
-   App summary generation
-   Summarize a client script using Now Assist
-   Code Assist autocomplete
-   Code Assist edit
-   Code assist summarization
-   Code Assist generation
-   Event handler generation
-   Create an AI-generated experience
-   Flow generation
-   Flow generation with images
-   Flow recommendations
-   Flow summarization
-   Mobile card generation
-   Playbook generation
-   Playbook generation with images
-   Playbook recommendations
-   Process inefficiency highlights
-   Robotic Process Automation \(RPA\) bot generation
-   Spoke generation
-   Test generation
-   Work notes analysis

</td></tr><tr><td>

Platform

</td><td>

[Now Assist Platform](../../now-assist-platform/concept/platform-now-assist-landing.md)

</td><td>

-   [Article optimization](now-assist-article-optimization.md)
-   [Complete record generation](../../now-assist-data-kit/concept/now-assist-data-kit-landing.md)
-   [Conversational Help](conversational-help-skills.md)
-   Document summarization
-   Dynamic Guidance
-   [Extract information from documents](now-assist-extract-information-from-documents.md)
-   [GAF skills](../../now-assist-ai-agents/task/configure-gaf.md)
-   [Knowledge content recommendation](now-assist-platform-knowledge.md)
-   [Multimodal chat](../../document-intelligence/concept/docintel-exploring-now-assist.md)
-   [Navigation](now-assist-global-navigation.md)
-   [New column data generation](../../now-assist-data-kit/concept/now-assist-data-kit-landing.md)
-   [Potential knowledge gaps](potential-knowledge-gaps.md)
-   [Requester approval checklist](service-portal-approval-checklist-skill.md)
-   [ServiceNow Lens](../../../product/servicenow-lens/concept/servicenow-lens-landing-page.md)
-   [TextToResult](../../knowledge-graph/concept/knowledge-graph-landing.md)

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

Now Assist for Accounts Payable Operations \(APO\)

</td><td>

-   Invoice case summarization
-   Purchase order summarization

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

Now Assist for Supplier Lifecycle Operations \(SLO\)

</td><td>

-   Email response
-   Sentiment analysis
-   Supplier case summarization
-   Supplier summarization
-   Supplier performance summarization

</td></tr><tr><td>

Finance &amp; Supply Chain

</td><td>

Now Assist for Sourcing and Procurement Operations \(SPO\)

</td><td>

-   Negotiation summarization
-   Procurement case summarization
-   Purchase requisition summarization
-   Sourcing event summarization
-   Sourcing request summarization

</td></tr><tr><td>

App Engine

</td><td>

Now Assist for App Engine

</td><td>

Custom app record summarization

</td></tr><tr><td>

Impact

</td><td>

ImpactThe Impact workflow contains technical accelerators that can help you get started more quickly with some Now Assist features.

</td><td>

-   Jumpstart Your Now Assist for Creator
-   Jumpstart Your Now Assist in Document Intelligence
-   Jumpstart Your Now Assist in Virtual Agent
-   Jumpstart Your Now Assist Skill Kit

</td></tr><tr><td>

Vault

</td><td>

Now Assist for Vault

</td><td>

-   Check role access
-   Generate custom data pattern
-   Schedule Data Discovery job

</td></tr><tr><td>

Other

</td><td>

Now Assist for Zero Copy Connector

</td><td>

-   ERP data discovery
-   ERP data query

</td></tr></tbody>
</table>