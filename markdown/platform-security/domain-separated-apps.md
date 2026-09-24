---
title: Application support for domain separation
description: Many ServiceNow applications support domain separation in the base system but not all. Some supported applications include limitations on the data and administrative settings that can be domain-separated. These definitions delineate the domain separation support levels from the perspective of actual use cases and the people who use them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/domain-separated-apps.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [Domain separation for service providers, Access Management]
---

# Application support for domain separation

Many ServiceNow applications support domain separation in the base system but not all. Some supported applications include limitations on the data and administrative settings that can be domain-separated. These definitions delineate the domain separation support levels from the perspective of actual use cases and the people who use them.

## Domain separation support levels

ServiceNow applications that support domain separation may support the separation of data and data routing only, have advanced business logic separation, or support tenant \(customer\) level administration of the application. ServiceNow applications are defined with the following incremental support levels.

\[Omitted image "ds-support-levels.png"\] Alt text: Domain separation support levels

**No support**

-   The domain field may exist on data tables, but no logic exists to manage data.
-   This level is not considered domain-separated.

**Basic**

-   Business logic: Ensure data goes into the proper domain for the application’s service provider \(SP\) use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all use domain at production run time.
-   The owner of the instance must be able to set up the application to function across multiple tenants.

Sample use case: When an SP uses chat to respond to a tenant-customer’s message, the client must be able to see the SP's response.

**Standard**

-   Includes **Basic** level support.
-   Business logic: Processes can be created or modified per customer by the service provider \(SP\). The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The owner of the instance must be able to configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments mandatory when a record closes for one tenant but not for another.

**Enhanced**

-   Includes **Basic** and **Standard** levels.
-   Data-driven process enables service provider customers to modify business logic that is based on defined use cases. These configurations are UI-based and fail-safe so that configurations by one customer cannot affect another.
-   Tenants of the instance must be able to configure minimum viable product \(MVP\) business logic and data parameters for themselves. This logic and parameters would be expected for the application's normal function.

Sample use case: Tenant-customers of a shared environment must be able to change to the impact, urgency, or priority matrix to set priority within their domain.

**Note:** **Effective Domain \(\*\)**

Sometimes, a platform feature or application may effectively support SP use cases even without the domain framework. If so, the use cases must detail its support of domain separation. An asterisk \(**\***\) after the support level indicates this kind of configuration.

|Supported feature|Basic|Standard|Enhanced|
|-----------------|-----|--------|--------|
|Domain column is present for base system application tables.|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|
|Domain-specific configuration is managed by instance owner.|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|
|Tenant domains can manage their own application data.| |\[Omitted image "icon-active-plugin.png"\] Alt text: supported|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|
|Application properties are domain aware when needed.| |\[Omitted image "icon-active-plugin.png"\] Alt text: supported|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|
|Business logic and processes can be domain-separated by instance owner.| |\[Omitted image "icon-active-plugin.png"\] Alt text: supported|\[Omitted image "icon-active-plugin.png"\] Alt text: supported|
|Business logic and processes can be administered by the tenant domain.| | |\[Omitted image "icon-active-plugin.png"\] Alt text: supported|

## Support levels by application

|Product Suite|Application|Support level|
|-------------|-----------|-------------|
|[App development, agentic development, and low-code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/hyperautomation-low-code/hyperautomation-low-code-landing-page.md)|App Engine Studio|No support|
|Automation Center|Basic|
|Robotic Process Automation \(RPA\) Hub|Basic|
|ServiceNow Studio|No support|
|Table Builder|Basic|
|App Engine Management Center|No support|
|[Decision Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/decision-designer-overview.md)|Standard|
|Enterprise Resource Planning Integration|No support|
|Enterprise Resource Planning Customization Mining|No support|
|Next Experience UI Builder|Basic|
|Workflow Data Fabric Hub/Zero Copy Connectors|No support|
|[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/c_CustomerServiceManagement.md)|Communities|No support|
|Customer Service Management|Basic|
|Release Management|Basic\*|
|Order Management for Customer Service Management|Basic|
|Post-Sales Support|Basic|
|Workforce Optimization for CSM|Basic|
|Now Assist for CSM|Basic|
|DevOps|Dev Ops|No support|
|Dev Ops Config|No support|
|Employee Service Management|HR Service Delivery|Basic\*|
|Health and Safety|No support|
|Legal Service Delivery|Basic|
|[Procurement Service Management \(PSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/psm-domain-separation.md)|No support|
|Safe Workplace Suite|See application site for individual application support levels|
|SharePoint Online Search Connector|Basic|
|Universal Request|Basic|
|Universal Task|Basic|
|Workforce Optimization for HR|Basic|
|[Environmental, Social, and Governance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/environmental-social-governance/esg-landing-page.md)|[Environmental, Social, and Governance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/environmental-social-governance/esg-landing-page.md)|No support\*|
|[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/fsm-application-landing-page.md)|[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/domain-separation-field-service.md)|Basic|
|Governance, Risk, and Compliance|Advanced Risk|Basic|
|Audit Management|Basic|
|Business Continuity Management|Basic|
|Compliance Case Management|Basic|
|Continuous Authorization and Monitoring|Basic|
|Governance, Risk, and Compliance \(GRC\)|Basic|
|Model Risk Management|Basic|
|Operational Resilience|Basic|
|Privacy Management|Basic|
|Policy and Compliance|Basic|
|Regulatory Change Management|No support\*|
|Third-party risk management|Basic|
|[GRC: Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/environmental-social-governance/esg-domain-separation.md)|Basic|
|Now Assist for TPRM|No support\*|
|Now Assist for IRM|No support\*|
|Smart Assessment Engine|Basic|
|[Industry Products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/industry-products/industry-products-landing.md)|
|•[Financial Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/fso-overview.md)|Financial Services Card Operations|Basic|
|Financial Services Deposit Operations|Basic|
|Financial Services Loan Operations|Basic|
|[Financial Services Payment Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/domain-separation-financial-services-payment-operations.md)|Basic|
|Financial Services Treasury Operations|Basic|
|Intelligent Servicing for Fraud|Basic|
|Property and Casualty Insurance Servicing|Basic|
|Life Insurance Servicing|Basic|
|Insurance Claims|Basic|
|Individual Life Claims|Basic|
|Financial Services Know Your Customer|Basic|
|Financial Services Credit Operation|Basic|
|[Financial Services Document Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/domain-separated-apps.md)|Basic|
|Now Assist for Financial Services Operations|Basic|
|Dispute Rules Content Pack for Visa|Basic|
|Dispute Rules Content Pack for Mastercard|Basic|
|• [Healthcare and Life Sciences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/hcls-overview.md)|[EMR Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/emr-help-domain-sep.md)|Basic|
|[Healthcare and Life Sciences Service Management Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/hcls-domain-sep-serv-mgmt-core.md)|Basic|
|[Pre-Visit Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/pre-visit-domain-sep.md)|Basic|
|[Patient Support Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/pss-domain-sep.md)|Basic|
|[Vaccine Administration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/VAM-domain-separation.md)|Basic|
|Healthcare Operations Core|Basic|
|Care Team Operations for Healthcare IT|Basic|
|Care Team Operations for Biomed|Basic|
|Care Team Operations for Facilities|Basic|
|Care Team Operations for Environmental Services|Basic|
|[Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/manufacturing-overview.md)|[Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-domain-separation.md)|Basic|
|[Retail Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-domain-separation.md)|Basic|
|[Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/bun-public-sector-landing-page.md)|Public Sector Digital Services|Basic|
|[Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/telecom-media-tech-landing.md)|[Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-domain-separation.md)|Basic|
|Customer Service Problem Management|Basic|
|[ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-spmc.md)|Basic \(Inherited from [Domain separation in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md)\).|
|[Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/proactive-service-exp-workflows/domain-separation-assurance-workflows.md)|Standard|
|[Service Bridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/service-bridge-v2-domain-separation.md)|Standard|
|[Exploring Technology Product Support Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/proactive-service-exp-workflows/tech-product-support-case-app.md)|Basic \(Inherited from Customer Service Management\).|
|[Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-network-inventory/domain-seperation-telecommunication-network-inventory.md)|Basic|
|IT Asset Management|Cloud Insights|No support|
|Hardware Asset Management|Enhanced|
|Software Asset Management|Enhanced|
|Enterprise Asset Management|Standard|
|Asset Audit Response|Basic|
|Strategic Portfolio Management|Agile Development|Basic\*|
|Alignment Planner Workspace|Basic|
|Application Portfolio Management|Basic|
|Cost Management|No support|
|Demand Management|Basic|
|Financial Management|No support|
|Investment Funding|Basic|
|Project Portfolio Management|Basic\*|
|Release Management|Basic\*|
|Scaled Agile Framework \(SAFe\)|Basic\*|
|Test Management|Basic\*|
|Goal Framework|Basic|
|IT Operations Management|Cloud Provisioning and Governance|Basic|
|Agent Client Collector|Basic|
|Discovery|Standard|
|Event Management|Basic|
|Service Operations Workspace for ITOM|Basic|
|Health Log Analytics|Basic|
|Metric Intelligence|Basic|
|Service Mapping|Basic|
|Cloud Migration Assessment|Basic|
|Action Library|No support|
|Cloud Configuration Governance|No support|
|Tag Governance|Basic|
|Cloud Insights Billing|No support|
|Cloud Provisioning and Governance: Google Cloud|Basic|
|mCloud Provisioning and Governance Terrafor|Basic|
|Cloud Operation Workspace|Basic|
|Cloud Discovery|Standard|
|Synthetic Monitoring|Basic|
|Service Observability|Basic|
|IT Service Management|Benchmarks|No support|
|Change Management|Basic|
|Coaching|Basic|
|Continual Improvement Management|Basic|
|Contract Management|No support|
|Digital End-User Experience|No support|
||Basic|
|Expense Line|No support|
|Incident Communications Management|Standard|
|Incident Management|Standard|
|Facilities Service Management|Standard|
|Incident Management|Standard|
|On-Call Scheduling|Standard|
|Asset Management|Basic|
|Problem Management|Standard|
|Procurement|Standard\*|
|Product Catalog|Standard|
|Request Management|Standard|
|[Service Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-service-catalog-management.md)|Standard|
|Service Level Management|Basic|
|[Service Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/SPM2-landing-page.md)|Basic\*|
|Site Reliability Operations|Basic\*|
|Task outage|Basic|
||No support|
|Walk-up Experience|Basic|
||Basic|
|[Mobile Configuration and Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/mobile-config-navigation.md)|[Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/mobile/mobile-domain-separation.md)|Basic|
|Now Intelligence|Dashboards|Basic|
|Performance Analytics|Enhanced|
|Process Optimization|Basic|
|Reporting|Basic|
||Basic|
|[The ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-platform/now-platform-landing.md)|[Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-domain-separation.md)|Standard|
|[Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ci-agent-chat-reference.md)|Standard|
||Basic\*|
|AI Search/Now Assist in AI Search|Searches respect domain restrictions from indexed records|
|App Engine Studio|No support|
|Application Management|No support|
|[Assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-assessments.md)|Standard|
|Automated Test Framework|Standard\*|
|[ServiceNow Voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-voice.md)|Basic|
|[Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-signing-landing.md)|No support|
|Contextual Search|Standard|
|[Configuration Management \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-cmdb.md)|Standard|
|[Content Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/domain-separation-content-management.md)|No support|
|[Credentials and Connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/connections-and-credentials/domain-separation-credentials_conn.md)|Standard|
|Data Certification|Basic\*|
|[Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-classification/domain-separation-data-classification.md)|Enhanced|
|Data Privacy|No support|
|Data Management|Basic\*|
|Delegated Development|No support|
|[Dependency Views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-dependency-views.md)|Basic|
|[Document Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-document-services.md)|No support|
|Dynamic Translation|Basic|
|[Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/edge-encryption/edge-encryption-domain-separation.md)|Basic support|
|External Content Connectors|No support\*|
|[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/field-encryption.md)|No support|
|[Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/encryption-landing.md)|No support|
|[Cloud Encryption with Key Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/cloud-encryption/dare-overview.md)|Basic support|
|Field Normalization|No support|
|[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/flow-designer-domain-separation.md)|Standard\*|
|[Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/domain-separation-guided-setup.md)|No support|
||Standard\*|
|Integrations with third-party applications and data sources|Basic+Standard|
|[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-knowledge.md)|Standard|
|Hermes Messaging Service|Basic|
|[Managed Documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-managed-documents.md)|No support|
|[MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-metricbase.md)|Basic|
|[Natural Language Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/domain-separation-virtual-agent.md)|Basic+Standard|
|Notifications|Standard|
|[ODBC Driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/domain-separation-odbc-driver.md)|Basic\*|
|[Orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-orchestration.md)|Standard\*|
|[Password Reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-pwd-reset.md)|Standard|
|[Platform Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/domain-sep-landing-page.md)|Domain separation landing page|
|Data Privacy|No support|
|Predictive Intelligence|Standard|
|Proactive Triggers|Basic|
|[Process Automation Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/process-automation-designer-domain-separation.md)|Basic|
|[Remote Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-remote-tables.md)|No support|
|Schedules|Basic|
|[Script debugger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/domain-separation-script-debugging.md)|Basic|
|Search Suggestions|No support|
|[Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/domain-separation-service-portal.md)|No support|
|Service Graph Connectors|No support|
|[Domain separation and Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/sidebar-domain-separation.md)|Standard|
|[State Flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-state-flows.md)|No support|
|Subscription Management|Basic\*|
|[Survey Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/domain-separation-surveys.md)|Basic\*|
|Task Intelligence|No support|
||Basic\*|
|UI Builder|Standard|
|[Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/domain-separation-virtual-agent.md)|Basic|
|[Visual Task Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/domain-separation-visual-task-boards.md)|Basic|
|[Web Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/domain-separation-web-services.md)|Standard\*|
|[Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/c_WorkflowsAndDomainSeparation.md)|Standard\*|
|Workspace|Standard|
|Platform Fundamentals|[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-landing-page.md)|No support|
|Instance Data Replication|No support|
|Integration Hub|Standard\*|
|Integrations with third-party applications and data sources|Basic Standard|
|Knowledge Management|Standard|
|Localization Framework|No support|
|Localization Workspace|No support|
|MetricBase|Basic|
|Model Context Protocol Client|Basic|
|Natural Language Understanding|Basic+Standard|
|Notifications|Standard|
|Now Assist AI Agents|Basic|
|ODBC Driver|Basic\*|
|Omnichannel Callback|No support|
|Orchestration|Standard\*|
|Password Reset|Standard|
|Platform Security|Domain Separation landing page|
|Data Privacy|No support|
|Predictive Intelligence|Basic+Standard|
|Proactive Triggers|Basic|
|Process Automation Designer|Basic|
|Remote Tables|No support|
|Robotic Process Automation Hub|Basic|
|Schedules|Basic|
|Script debugger|Basic|
|Search suggestions|No support|
|Service Graph Connectors|Standard\*|
|ServiceNow Vault|No support|
|Service Portal|No support|
|Sidebar \(aka Collaborative Chat\)|Standard|
|State Flows|No support|
||Basic\*|
|Survey Management|Basic\*|
|Task Intelligence|No support|
|Theme Builder|No support|
|TinyMCE|No support|
|Time Card|Basic\*|
|Transaction and Session Management|No support|
|UI Builder|Standard|
|Virtual Agent|Standard|
|Visual Task Boards|Basic|
|Web Services|Standard\*|
|Workflow|Standard\*|
|Workspace|Standard|
|Operational Technology|Operational Technology Manager|Basic|
|Industrial Process Manager|Basic|
|Operational Technology Vulnerability Response|Basic|
|Operational Technology Incident Management|Basic|
|[Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-operations-landing-page.md)|Subscription Management[Configuration Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/domain-separation-config-compliance.md)|Standard|
|[IBM QRadar Offense Ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/qradar-ibm-domain-sep.md)|Basic|
|[Microsoft Graph Security API alert ingestion integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/ms-graph-domain-sep.md)|Basic|
|[Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/domain-separation-security-incident-response.md)|Standard|
|[Threat Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/domain-separation-threat-intelligence.md)|Standard|
|Threat Intelligence Security Center|Standard|
|[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/domain-separation-vulnerability-response.md)|Standard|
|[Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-management-for-the-enterprise/c_ServiceManagement.md)|Facilities Service Management|Standard|
|[Planned Maintenance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-management-for-the-enterprise/domain-separation-planned-maintenance.md)|Standard\*|
|Structured Problem Analysis|No support|
|Workforce Optimization for ITSM|Basic|
|Vendor Management Workspace|Basic|
|[Proactive Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/proactive-triggers.md)|Basic|
|Employee Service Management|SharePoint Online Search Connector|Basic|
|Workforce Optimization for ITSM|Basic|
|Application Portfolio Management|Application Portfolio Management|Basic|
|Domain separation and Conversational Analytics|Basic|
|[Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-mgt-overview.md)|Advanced Approval for Sales Management|Enhanced|

**Parent Topic:**[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/domain-sep-landing-page.md)

