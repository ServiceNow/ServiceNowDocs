---
title: Agentic workflows
description: Agentic workflows are AI‑driven workflow orchestrations that use one or more AI agents to achieve a specific outcome. They go beyond single‑step automation by dynamically planning, executing, and adapting actions based on context, data, and intermediate results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/sn-aia-use-cases-list.html
release: yokohama
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 7
keywords: [AI Agents, Agentic AI]
breadcrumb: [AI agents and agentic workflows, Enable AI Experiences]
---

# Agentic workflows

Agentic workflows are AI‑driven workflow orchestrations that use one or more AI agents to achieve a specific outcome. They go beyond single‑step automation by dynamically planning, executing, and adapting actions based on context, data, and intermediate results.

Agentic workflows handle routine but variable procedures, such as investigation, remediation, and analysis, where the exact steps may differ from case to case.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/ai-native-sku-overview.md).

## Agentic workflows overview

Agentic workflows use multiple AI agents to achieve specific outcomes. Different workflows offer different available tasks. Many agentic workflow templates are available for you to activate, duplicate, or customize. For more information, see [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/activate-aia-use-case.md) and [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/clone-aia-usecase.md).

For more information about the in-product agentic AI experience, see [In-product agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/in-product-agentic-ai.md). You can create UI actions for your agentic workflows in AI Agent Studio. Open the agentic workflow, navigate to the [Select channels and access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/channels-access-aw.md) step in the guided setup, and create a UI action.

## What an agentic workflow does

Agentic workflows can:

-   Achieve an outcome, not just complete a task

    The workflow focuses on resolving a business problem or completing a goal, rather than executing a single action.

-   Coordinate multiple AI agents and skills

    Agentic workflows can invoke generative AI skills and AI agents as needed to gather information, reason over data, take action, and verify results.

-   Adapt to variability

    Workflows can adjust execution paths based on conditions, findings, or system responses, making them suitable for non-deterministic scenarios such as troubleshooting or analysis.

-   Operate across systems and records

    Agentic workflows interact with the ServiceNow AI Platform and connected systems to read data, update records, and trigger downstream actions.


## How agentic workflows are used

Agentic workflows are commonly used to:

-   Resolve tasks that follow a repeatable decision pattern but vary in execution.
-   Investigate issues by gathering and analyzing contextual data.
-   Execute remediation steps based on findings.
-   Assist users with analytical or exploratory workflows.

Depending on the product and configuration, agentic workflows can be triggered automatically or initiated by a user through a contextual UI or action.

## Available agentic workflows

The following tables describe the available agentic workflows that are included in the ServiceNow applications, grouped by workflow area.

## IT and digital operations

<table id="table_aw-technology-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available agentic workflows

</th></tr></thead><tbody><tr><td>

Enterprise Asset Management

</td><td>

-   Help repair enterprise assets
-   Help manage enterprise asset requests

</td></tr><tr><td>

[IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/r_ITOMApplications.md)

</td><td>

[ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-visibility-landing-page.md)

-   Pattern diagnostic
-   [Analyze potential impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-analyze-potential-impact-workflow.md)
-   Firewall management task creation

 [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-health-landing-page.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-health-landing-page.md)

-   [Triage and analyze alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-alert-triage-agentic-workflow.md)
-   [Analyze alert impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-agentic-aia.md)
-   [Analyze potential impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-analyze-potential-impact-workflow.md)
-   [Manage alerts autonomously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-autonomous-operator-workflow.md)
-   Agent Client Collector \(ACC\) diagnostic workflow

</td></tr><tr><td>

Now Assist for Operational Technology Service Management \(OTSM\)

</td><td>



</td></tr><tr><td>

[Operational Technology \(OT\) Manager Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-for-otm-landing.md)

</td><td>

[Import the OT device spreadsheet into OT CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-otm-aiagents-import-ot-device-workflow.md)

</td></tr><tr><td>

[ServiceNow Otto for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md)

</td><td>

[Generate enterprise architecture diagram](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-aiagents-ea-diagramming-usecase.md)

</td></tr><tr><td>

ServiceNow Otto for Hardware Asset Management \(HAM\)

</td><td>

-   Help manage hardware asset requests
-   Help repair hardware assets

</td></tr><tr><td>

[ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm.md)

</td><td>

-   [Assess conflicts for a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-assess-conflicts-workflow.md)
-   [Assess quality of a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-assess-quality-change-request-workflow.md)
-   [Create outages for a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-create-outages-for-a-change-request.md)
-   [Create standard change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-create-change-request-workflow.md)
-   [Create standard change template proposal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-create-standard-change-template-proposal.md)
-   [DEX issue diagnosis and resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-dex-diagnosis-resolution-workflow.md)
-   [Explain SLA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-explain-sla-workflow.md)
-   [Generate change request plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-change-planner-usecase.md)
-   [Generate post incident reviews](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-mim-usecase.md)
-   Incident assist
-   [Investigate and resolve ITSM incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-incident-resolver-workflow.md)
-   [Manage Microsoft 365 group members](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-O365-groupmembers-workflow.md)
-   [Notify users with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-twilio-text-usecase.md)
-   [Schedule a change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-schedule-change-agentic-workflow.md)
-   [Suggest configuration items for a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-suggest-configuration-items-for-a-change-request.md)
-   [Triage and categorize ITSM incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-aiagents-catincidents-usecase.md)
-   Who is On Call
-   [Wrap-up and resolve ITSM incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm-wrap-up-resolve-incident-aw.md)

</td></tr><tr><td>

ServiceNow Otto for Software Asset Management \(SAM\)

</td><td>

-   Create software reclamation rule
-   Evaluate software removal candidate
-   Help manage software asset requests

</td></tr><tr><td>

ServiceNow Otto for Strategic Portfolio Management

</td><td>

-   Generate Agile stories
-   Monitor project tasks

</td></tr></tbody>
</table>## Security and Risk

<table id="table_aw-security-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available agentic workflows

</th></tr></thead><tbody><tr><td>

ServiceNow Otto for Integrated Risk Management \(IRM\)

</td><td>

-   Generate regulatory action plans
-   Get regulatory analysis
-   Identify risks for an entity
-   Optimize issue resolution

</td></tr><tr><td>

[ServiceNow Otto for Operational Sustainability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/now-assist-for-esg.md)

</td><td>

Generate carbon calculations for metrics

</td></tr><tr><td>

[ServiceNow Otto for Security Incident Response \(SIR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-security-incident-landing.md)

</td><td>

-   [Analyze security operations metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-sir-soc-efficiency-usecase.md)
-   [Close security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-sir-close-incident-usecase.md)
-   [Generate SIR shift handover report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/add-incidents-shifthandover-ai-agent.md)
-   [Resolve security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-sir-resolve-incident-ai-workflow.md)

</td></tr><tr><td>

[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/vuln-landing-page.md)

</td><td>

-   
-   [Assess your exposure to vulnerabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/assess-exposure-vr-aiagent.md)
-   [Analyze vulnerability remediation status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/sla-targets-vr-aiagent.md)
-   Security Exposure 360

</td></tr></tbody>
</table>## Customer experiences \(CRM\)

<table id="table_aw-customer-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available agentic workflows

</th></tr></thead><tbody><tr><td>

[Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/fso-overview.md)

</td><td>

[Help resolve friendly fraud disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/friendly-fraud-agentic-ai-workflow.md)

</td></tr><tr><td>

[ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm.md)

</td><td>

-   Accelerate complaint case handling
-   [Provide Customer 360 insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/customer-service-management-ai-agent-collection-customer-360.md)
-   [Triage cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/case-resolving-use-case.md)

</td></tr><tr><td>

Field Service Management

</td><td>

Create a work order

</td></tr><tr><td>

ServiceNow Otto for Manufacturing Commercial Operations \(MCO\)

</td><td>

Execute recall campaigns faster

</td></tr><tr><td>

[ServiceNow Otto for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/bun-public-sector-landing-page.md)

</td><td>

Help manage public information requests

</td></tr><tr><td>

[Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/order-mgt-overview.md)

</td><td>

[Help nurture new leads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/help-nurture-new-leads-agentic-workflow.md)

</td></tr><tr><td>

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md)

</td><td>

-   Analyze risk and recommend solutions
-   Draft and schedule touchpoint meetings
-   Monitor engagement health
-   Support renewals and expansions

</td></tr><tr><td>

[Telecommunications, Media, and Technology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/telecom-media-tech-landing.md)

</td><td>

-   [Analyze network incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/network-incident-analysis-usecase.md)
-   [Customer voice quality issue resolutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-customer-voice.md)
-   [Help remediate bill issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/billissue-remediation-usecase.md)
-   Service test and repair
-   Smart Actions for Telecom

</td></tr><tr><td>

[Service Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-exchange/tmt-service-bridge-both-landing-page.md)

</td><td>

-   Service Exchange Knowledge Assistant
-   Service Exchange onboarding

</td></tr><tr><td>



</td><td>

Request care team assistance

</td></tr></tbody>
</table>## Employee experiences

<table id="table_aw-employee-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available agentic workflows

</th></tr></thead><tbody><tr><td>

[Now Assist for Finance and Supply Chain \(FSC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-fsc-common-landing.md)

</td><td>

[Conversational intake for sourcing and procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/spo-help-fulfill-pr-agentic.md)

</td></tr><tr><td>



</td><td>

-   Define PO exception mitigation strategy
-   Email Intent to Action

</td></tr><tr><td>

Contract Management Pro

</td><td>

-   Conversational contract search and insights
-   Manage contract repository

</td></tr><tr><td>



</td><td>

CBS setup

</td></tr><tr><td>

ServiceNow Otto for Health and Safety

</td><td>

-   Create actions for safety incidents
-   
-   

</td></tr><tr><td>

ServiceNow Otto for HR Service Delivery \(HRSD\)

</td><td>

-   Help resolve tuition requests
-   Help resolve tuition reimbursement requests
-   Predict service and transfer HR cases
-   Resolve noncritical HR cases
-   Resolve critical HR cases
-   Generate onboarding ramp-up plan
-   Recommend catalog and order guide tasks in Onboarding Journey
-   Offboarding knowledge transfer plan generation
-   Schedule interviews

</td></tr><tr><td>

Legal Service Delivery

</td><td>

-   Conversational contract search and insights
-   Triage legal requests

</td></tr><tr><td>

[ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)

</td><td>

[Email intent to action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/automated-supplier-case-creation-from-emails.md)

</td></tr><tr><td>

ServiceNow Otto for Workplace Service Delivery \(WSD\)

</td><td>

-   Automate map updates
-   Help manage workplace reservations
-   Manage temporary space closures
-   Optimize cleaning activities
-   Process images for new tasks
-   Workplace Concierge

</td></tr></tbody>
</table>## AI Platform

<table id="table_aw-platform-workflow"><thead><tr><th class="filter">

Product

</th><th>

Available agentic workflows

</th></tr></thead><tbody><tr><td>

Now Assist for Zero Copy Connector

</td><td>

Explore ERP models

</td></tr><tr><td>

[Now Assist in Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/now-assist-notifications.md)

</td><td>

[Email Intent to Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/email-agentic-workflow.md)

</td></tr><tr><td>

[Now Assist Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/na-ai-agents.md)

</td><td>

-   [Analyze incident trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/incident-trends.md)
-   [Classify tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/classify-tasks.md)
-   Error Analysis and Remediation workflow
-   [Generate my work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/generate-work-plan.md)
-   [Generate resolution plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/resolve-requests.md)
-   [Help optimize team productivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/help-optimize-productivity.md)
-   [Identify ways to improve services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/service-improvement.md)
-   [Investigate IT problems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/problem-investigation.md)
-   Notification agent
-   [Process images for tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/images-tasks.md)
-   [Suggest survey responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/survey-suggest.md)

</td></tr><tr><td>

[ServiceNow Otto for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-landing-cmdb.md)

</td><td>

-   [Create configuration item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-awf-ci-creator.md)
-   [Provide advice on CMDB governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-awf-governance.md)
-   [Search CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/na-cmdb-awf-search.md)

</td></tr><tr><td>

ServiceNow Otto for Vault

</td><td>

-   Access observer configuration
-   Classify assets with ServiceNow Vault agents
-   Field encryption and auto-generate access policies
-   Field encryption with Vault module
-   Securing custom apps with Vault agents
-   Summarize access observer logs

</td></tr></tbody>
</table>## App development

|Product|Available agentic workflows|
|-------|---------------------------|
|Build Agent|Create in-app agents, skills, and workflows|
|ServiceNow Otto for Creator||

