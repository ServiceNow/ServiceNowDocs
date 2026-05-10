---
title: Application support for domain separation
description: Many ServiceNow applications support domain separation in the base system but not all. Some supported applications include limitations on the data and administrative settings that can be domain-separated. These definitions delineate the domain separation support levels from the perspective of actual use cases and the people who use them.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Domain separation for service providers, Access Management]
---

# Application support for domain separation

Many ServiceNow applications support domain separation in the base system but not all. Some supported applications include limitations on the data and administrative settings that can be domain-separated. These definitions delineate the domain separation support levels from the perspective of actual use cases and the people who use them.

## Domain separation support levels

ServiceNow applications that support domain separation may support the separation of data and data routing only, have advanced business logic separation, or support tenant \(customer\) level administration of the application. ServiceNow applications are defined with the following incremental support levels.

![Domain separation support levels](../image/ds-support-levels.png)

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
|Domain column is present for base system application tables.|![supported](../image/icon-active-plugin.png)|![supported](../image/icon-active-plugin.png)|![supported](../image/icon-active-plugin.png)|
|Domain-specific configuration is managed by instance owner.|![supported](../image/icon-active-plugin.png)|![supported](../image/icon-active-plugin.png)|![supported](../image/icon-active-plugin.png)|
|Tenant domains can manage their own application data.| |![supported](../image/icon-active-plugin.png)|![supported](../image/icon-active-plugin.png)|
|Application properties are domain aware when needed.| |![supported](../image/icon-active-plugin.png)|![supported](../image/icon-active-plugin.png)|
|Business logic and processes can be domain-separated by instance owner.| |![supported](../image/icon-active-plugin.png)|![supported](../image/icon-active-plugin.png)|
|Business logic and processes can be administered by the tenant domain.| | |![supported](../image/icon-active-plugin.png)|

## Support levels by application

|Product Suite|Application|Support level|
|-------------|-----------|-------------|
|[App development and low-code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/hyperautomation-low-code/hyperautomation-low-code-landing-page.md)|[App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-overview.md)|No support|
|[Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/automation-center-landing-page.md)|Basic|
|[Robotic Process Automation \(RPA\) Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-explore.md)|Basic|
|ServiceNow Studio|No support|
|[Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/tb-landing-page.md)|Basic|
|[App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/manage-app-development.md)|No support|
|[Decision Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/decision-designer-overview.md)|Standard|
|Enterprise Resource Planning Integration|No support|
|Enterprise Resource Planning Customization Mining|No support|
|[Next Experience UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md)|Basic|
|Workflow Data Fabric Hub/Zero Copy Connectors|No support|
|[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/c_CustomerServiceManagement.md)|[Communities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/domain-separation-communities.md)|No support|
|[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/domain-separation-customer-service.md)|Basic|
|[Release Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/release-management/domain-separation-release-management.md)|Basic\*|
|Order Management for Customer Service Management|Basic|
|Post-Sales Support|Basic|
|[Workforce Optimization for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/domain-separation-configurable-wfo-cs.md)|Basic|
|[Now Assist for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm.md)|Basic|
|[DevOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-landing-page.md)|[Dev Ops](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/devops-domain-separation.md)|No support|
|[Dev Ops Config](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/devops-config-domain-separation.md)|No support|
|[Employee Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-service-management-overview.md)|[HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/hr-domain-separation.md)|Basic\*|
|[Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/health-and-safety-incident-management/health-safety-domain-separation.md)|No support|
|[Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-service-delivery/legal-domain-separation.md)|Basic|
|[Procurement Service Management \(PSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/psm-domain-separation.md)|No support|
|[Safe Workplace Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/safe-workplace/domain-separation-safe-workplace.md)|See application site for individual application support levels|
|[SharePoint Online Search Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/sharepoint-online-search-connector-domain-separation.md)|Basic|
|[Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-request-for-hr-service-delivery/domain-sep-universal-request.md)|Basic|
|[Universal Task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-task/domain-sep-universal-task.md)|Basic|
|[Workforce Optimization for HR](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workforce-optimization-for-hr/wfo-hr-overview.md)|Basic|
|[Environmental, Social, and Governance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-landing-page.md)|[Environmental, Social, and Governance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-landing-page.md)|No support\*|
|[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md)|[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/domain-separation-field-service.md)|Basic|
|[Governance, Risk, and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/r_WhatIsGRC.md)|[Advanced Risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-risk-management-workspace/domain-separation-risk-management.md)|Basic|
|[Audit Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-domain-separation.md)|Basic|
|Business Continuity Management|Basic|
|[Compliance Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-domain-separation.md)|Basic|
|[Continuous Authorization and Monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-domain-separation.md)|Basic|
|[Governance, Risk, and Compliance \(GRC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-domain-separation.md)|Basic|
|Model Risk Management|Basic|
|[Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-opres-landing-page.md)|Basic|
|[Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-domain-separation.md)|Basic|
|[Policy and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/domain-separation-pol-comp.md)|Basic|
|[Regulatory Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-domain-separation.md)|No support\*|
|[Third-party risk management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-domain-separation.md)|Basic|
|[GRC: Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/esg-domain-separation.md)|Basic|
|Now Assist for TPRM|No support\*|
|Now Assist for IRM|No support\*|
|[Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-domain-separation.md)|Basic|
|[Industry Products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industry-products/industry-products-landing.md)|
|•[Financial Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/fso-overview.md)|Financial Services Card Operations|Basic|
|Financial Services Deposit Operations|Basic|
|Financial Services Loan Operations|Basic|
|[Financial Services Payment Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-payment-operations/domain-separation-financial-services-payment-operations.md)|Basic|
|Financial Services Treasury Operations|Basic|
|Intelligent Servicing for Fraud|Basic|
|Property and Casualty Insurance Servicing|Basic|
|Life Insurance Servicing|Basic|
|Insurance Claims|Basic|
|Individual Life Claims|Basic|
|Financial Services Know Your Customer|Basic|
|Financial Services Credit Operation|Basic|
|[Financial Services Document Processor](domain-separated-apps.md)|Basic|
|Now Assist for Financial Services Operations|Basic|
|Dispute Rules Content Pack for Visa|Basic|
|Dispute Rules Content Pack for Mastercard|Basic|
|• [Healthcare and Life Sciences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hcls-overview.md)|[EMR Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/emr-help/emr-help-domain-sep.md)|Basic|
|[Healthcare and Life Sciences Service Management Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-domain-sep-serv-mgmt-core.md)|Basic|
|[Pre-Visit Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/pre-visit-domain-sep.md)|Basic|
|[Patient Support Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/pss-domain-sep.md)|Basic|
|[Vaccine Administration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/vaccine-administration-management/VAM-domain-separation.md)|Basic|
|Healthcare Operations Core|Basic|
|Care Team Operations for Healthcare IT|Basic|
|Care Team Operations for Biomed|Basic|
|Care Team Operations for Facilities|Basic|
|Care Team Operations for Environmental Services|Basic|
|[Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-overview.md)|[Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-domain-separation.md)|Basic|
|[Retail Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-domain-separation.md)|Basic|
|[Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/bun-public-sector-landing-page.md)|Public Sector Digital Services|Basic|
|[Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/telecom-media-tech-landing.md)|[Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-domain-separation.md)|Basic|
|Customer Service Problem Management|Basic|
|[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)|Basic \(Inherited from [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/domain-separation-in-the-now-assist-admin-console.md)\).|
|[Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/domain-separation-assurance-workflows.md)|Standard|
|[Service Bridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-exchange/service-bridge-v2-domain-separation.md)|Standard|
|[Exploring Technology Product Support Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/tech-product-support-case-app.md)|Basic \(Inherited from [Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/domain-separation-customer-service.md)\).|
|[Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/domain-seperation-telecommunication-network-inventory.md)|Basic|
|[IT Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/it-asset-management.md)|[Cloud Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/domain-separation-cloudin.md)|No support|
|[Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/domain-separation-ham.md)|Enhanced|
|[Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/domain-separation-software-asset-management.md)|Enhanced|
|[Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/enterprise-asset-management/domain-separation-eam.md)|Standard|
|[Asset Audit Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/asset-audits/asset-audit-response-domain-separation.md)|Basic|
|[Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/r_ITBusinessManagement.md)|[Agile Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/agile-development-2.0-domain-separation.md)|Basic\*|
|[Alignment Planner Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/alignment-planner-domain-separation.md)|Basic|
|Application Portfolio Management|Basic|
|[Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/cost-management/domain-separation-cost-management.md)|No support|
|[Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/domain-sep-demand-mgt.md)|Basic|
|Financial Management|No support|
|[Investment Funding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/investment-funding/domain-separation-investment-funding.md)|Basic|
|[Project Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/ppm-collaboration/domain-separation-project-portfolio-financials.md)|Basic\*|
|[Release Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/release-management/domain-separation-release-management.md)|Basic\*|
|[Scaled Agile Framework \(SAFe\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scaled-agile-framework-safe/domain-separation-scaled-agile-framework.md)|Basic\*|
|[Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/test-management/domain-separation-test-management.md)|Basic\*|
|[Goal Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/goal-framework/goal-framework-domain-separation.md)|Basic|
|[IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/r_ITOMApplications.md)|[Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/domain-separation-cloud-management.md)|Basic|
|[Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/domain-separation-agent-client-collector.md)|Basic|
|[Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_DiscoveryDomainSeparation.md)|Standard|
|[Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/domain-separation-event-management.md)|Basic|
|Service Operations Workspace for ITOM|Basic|
|[Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-domain-separation.md)|Basic|
|[Metric Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/domain-separation-operational-intelligence.md)|Basic|
|[Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/domain-separation-service-mapping.md)|Basic|
|Cloud Migration Assessment|Basic|
|Action Library|No support|
|Cloud Configuration Governance|No support|
|[Tag Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/tag-governance/tag-governance-domain-separation.md)|Basic|
|Cloud Insights Billing|No support|
|[Cloud Provisioning and Governance: Google Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/cloud-mgmt-dom-sep-recommend.md)|Basic|
|m[Cloud Provisioning and Governance Terrafor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/domain-separation-cloud-management.md)|Basic|
|Cloud Operation Workspace|Basic|
|Cloud Discovery|Standard|
|Synthetic Monitoring|Basic|
|Service Observability|Basic|
|[IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/r_ITServiceManagement.md)|[Benchmarks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/benchmarks/domain-separation-benchmarks.md)|No support|
|[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/domain-separation-change-mgt.md)|Basic|
|Coaching|Basic|
|[Continual Improvement Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/continual-improvement-management/cim-domain-separation.md)|Basic|
|[Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/domain-separation-contract-mgmt.md)|No support|
|Digital End-User Experience|No support|
|[Domain separation and Digital Product Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-domain-separation-digital-product-release.md)|Basic|
|[Expense Line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/expense-line/r_InstalledWithExpenseLine.md)|No support|
|[Incident Communications Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-communications-management/domain-separation-incident-comm-mgt.md)|Standard|
|[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/domain-separation-incident-management.md)|Standard|
|[Facilities Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/domain-separation-facilities-service-mgt.md)|Standard|
|[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/domain-separation-incident-management.md)|Standard|
|[On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/domain-separation-on-call-scheduling.md)|Standard|
|Asset Management|Basic|
|[Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/problem-management/domain-separation-and-problem-management.md)|Standard|
|[Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/procurement/domain-separation-procurement.md)|Standard\*|
|[Product Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/product-catalog/domain-separation-product-catalog.md)|Standard|
|[Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/request-management/domain-sep-req-management.md)|Standard|
|[Service Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/domain-separation-service-catalog-management.md)|Standard|
|[Service Level Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/domain-separation-sla.md)|Basic|
|[Service Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-portfolio-management/SPM2-landing-page.md)|Basic\*|
|Site Reliability Operations|Basic\*|
|[Task outage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-outage/domain-separation-task-outage.md)|Basic|
||No support|
|[Walk-up Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/walk-up-experience/domain-separation-walkup-experience.md)|Basic|
|[Configure Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/configure-now-assist-for-itsm.md)|Basic|
|[Mobile Configuration and Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-config-navigation.md)|[Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-domain-separation.md)|Basic|
|[Now Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/c_performanceAnalyticsAndReporting.md)|[Dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/domain-separation-in-dashboards.md)|Basic|
|[Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PAWithDomainSeparation.md)|Enhanced|
|[Process Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/domain-separation-process-optimization.md)|Basic|
|[Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/reporting/domain-separation-in-reporting.md)|Basic|
|[Usage Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/user-exp-analytics-landing.md)|Basic|
|[The ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-platform/now-platform-landing.md)|[Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-domain-separation.md)|Standard|
|[Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ci-agent-chat-reference.md)|Standard|
|[AI Search/Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ai-search-domain-separation.md)|Searches respect domain restrictions from indexed records|
|[App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-domain-sep.md)|No support|
|[Application Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-management-domain-separation.md)|No support|
|[Assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/domain-separation-assessments.md)|Standard|
|[Automated Test Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/domain-separation-auto-test-framework.md)|Standard\*|
|[ServiceNow Voice](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/domain-separation-voice.md)|Basic|
|[Code Signing](../../encryption/concept/code-signing-landing.md)|No support|
|[Contextual Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/contextual-search/domain-separation-contextual-search.md)|Standard|
|[Configuration Management \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/domain-separation-cmdb.md)|Standard|
|[Content Management System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/domain-separation-content-management.md)|No support|
|[Credentials and Connections](../../../product/credentials/concept/domain-separation-credentials_conn.md)|Standard|
|Data Certification|Basic\*|
|[Data Classification](../../security/concept/domain-separation-data-classification.md)|Enhanced|
|Data Privacy|No support|
|[Data Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/domain-separation-data-management.md)|Basic\*|
|[Delegated Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/delegated-development-and-deployment/domain-separation-delegated-development.md)|No support|
|[Dependency Views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/domain-separation-dependency-views.md)|Basic|
|[Document Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/domain-separation-document-services.md)|No support|
|[Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/domain-sep-dynamic-translation.md)|Basic|
|[Edge Encryption](../../edge-encryption/concept/edge-encryption-domain-separation.md)|Basic support|
|External Content Connectors|No support\*|
|[Field Encryption](../../encryption/concept/field-encryption.md)|No support|
|[Encryption](../../security/concept/encryption-landing.md)|No support|
|[Cloud Encryption with Key Management](../../encryption-dare/concept/dare-overview.md)|Basic support|
|[Field Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/domain-separation-field-normalization.md)|No support|
|[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-designer-domain-separation.md)|Standard\*|
|[Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/domain-separation-guided-setup.md)|No support|
|[Domain separation and Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/domain-separation-integrationhub.md)|Standard\*|
|[Integrations with third-party applications and data sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/domain-separation-app-data-source-integration.md)|Basic+Standard|
|[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/domain-separation-knowledge.md)|Standard|
|Hermes Messaging Service|Basic|
|[Managed Documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/document-management-services/domain-separation-managed-documents.md)|No support|
|[MetricBase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/metricbase/domain-separation-metricbase.md)|Basic|
|[Natural Language Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/domain-separation-virtual-agent.md)|Basic+Standard|
|[Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/domain-separation-notifications.md)|Standard|
|[ODBC Driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/domain-separation-odbc-driver.md)|Basic\*|
|[Orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/domain-separation-orchestration.md)|Standard\*|
|[Password Reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/domain-separation-pwd-reset.md)|Standard|
|[Platform Security](domain-sep-landing-page.md)|Domain separation landing page|
|Data Privacy|No support|
|[Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/domain-separation-predictive-intelligence.md)|Standard|
|Proactive Triggers|Basic|
|[Process Automation Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-domain-separation.md)|Basic|
|[Remote Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/domain-separation-remote-tables.md)|No support|
|[Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/domain-support-for-schedules.md)|Basic|
|[Script debugger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/domain-separation-script-debugging.md)|Basic|
|[Search Suggestions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-suggestions/domain-separation-search-suggestions.md)|No support|
|[Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/domain-separation-service-portal.md)|No support|
|Service Graph Connectors|No support|
|[Domain separation and Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/sidebar/sidebar-domain-separation.md)|Standard|
|[State Flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/domain-separation-state-flows.md)|No support|
|Subscription Management|Basic\*|
|[Survey Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/domain-separation-surveys.md)|Basic\*|
|Task Intelligence|No support|
|[Domain separation and Time Card](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/time-card-management/domain-separation-time-card.md)|Basic\*|
|[UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/uib-domain-sep.md)|Standard|
|[Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/domain-separation-virtual-agent.md)|Basic|
|[Visual Task Boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/visual-task-boards/domain-separation-visual-task-boards.md)|Basic|
|[Web Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/domain-separation-web-services.md)|Standard\*|
|[Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/legacy-workflow/c_WorkflowsAndDomainSeparation.md)|Standard\*|
|Workspace|Standard|
|Platform Fundamentals|[Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/impact-landing-page.md)|No support|
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
|[Domain separation and Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/domain-separation-subscription-mgmt.md)|Basic\*|
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
|[Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations-landing-page.md)|Subscription Management[Configuration Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/domain-separation-config-compliance.md)|Standard|
|[IBM QRadar Offense Ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/qradar-ibm-domain-sep.md)|Basic|
|[Microsoft Graph Security API alert ingestion integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/ms-graph-domain-sep.md)|Basic|
|[Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/domain-separation-security-incident-response.md)|Standard|
|[Threat Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/domain-separation-threat-intelligence.md)|Standard|
|Threat Intelligence Security Center|Standard|
|[Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/domain-separation-vulnerability-response.md)|Standard|
|[Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/c_ServiceManagement.md)|[Facilities Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/domain-separation-facilities-service-mgt.md)|Standard|
|[Planned Maintenance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/planned-maintenance-family/domain-separation-planned-maintenance.md)|Standard\*|
|Structured Problem Analysis|No support|
|Workforce Optimization for ITSM|Basic|
|Vendor Management Workspace|Basic|
|[Proactive Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/product-support-for-technology/proactive-triggers.md)|Basic|
|Employee Service Management|SharePoint Online Search Connector|Basic|
|Workforce Optimization for ITSM|Basic|
|Application Portfolio Management|Application Portfolio Management|Basic|
|Domain separation and Conversational Analytics|Basic|
|[Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-overview.md)|Advanced Approval for Sales Management|Enhanced|

**Parent Topic:**[Domain separation for service providers](domain-sep-landing-page.md)

