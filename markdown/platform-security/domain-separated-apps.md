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
|[App development and low-code](https://www.servicenow.com/docs/access?context=hyperautomation-low-code-landing-page&version=australia&pubname=australia-hyperautomation-low-code&ft:locale=en-US)|[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=australia&pubname=australia-application-development&ft:locale=en-US)|No support|
|[Automation Center](https://www.servicenow.com/docs/access?context=automation-center-landing-page&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)|Basic|
|[Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-explore&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)|Basic|
|ServiceNow Studio|No support|
|[Table Builder](https://www.servicenow.com/docs/access?context=tb-landing-page&version=australia&pubname=australia-application-development&ft:locale=en-US)|Basic|
|[App Engine Management Center](https://www.servicenow.com/docs/access?context=manage-app-development&version=australia&pubname=australia-application-development&ft:locale=en-US)|No support|
|[Decision Builder](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=australia&pubname=australia-build-workflows&ft:locale=en-US)|Standard|
|Enterprise Resource Planning Integration|No support|
|Enterprise Resource Planning Customization Mining|No support|
|[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US)|Basic|
|Workflow Data Fabric Hub/Zero Copy Connectors|No support|
|[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)|[Communities](https://www.servicenow.com/docs/access?context=domain-separation-communities&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)|No support|
|[Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)|Basic|
|[Release Management](https://www.servicenow.com/docs/access?context=domain-separation-release-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic\*|
|Order Management for Customer Service Management|Basic|
|Post-Sales Support|Basic|
|[Workforce Optimization for CSM](https://www.servicenow.com/docs/access?context=domain-separation-configurable-wfo-cs&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)|Basic|
|[Now Assist for CSM](https://www.servicenow.com/docs/access?context=now-assist-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)|Basic|
|[DevOps](https://www.servicenow.com/docs/access?context=dev-ops-landing-page&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|[Dev Ops](https://www.servicenow.com/docs/access?context=devops-domain-separation&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|No support|
|[Dev Ops Config](https://www.servicenow.com/docs/access?context=devops-config-domain-separation&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|No support|
|[Employee Service Management](https://www.servicenow.com/docs/access?context=employee-service-management-overview&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|[HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-domain-separation&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|Basic\*|
|[Health and Safety](https://www.servicenow.com/docs/access?context=health-safety-domain-separation&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|No support|
|[Legal Service Delivery](https://www.servicenow.com/docs/access?context=legal-domain-separation&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|Basic|
|[Procurement Service Management \(PSM\)](https://www.servicenow.com/docs/access?context=psm-domain-separation&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US)|No support|
|[Safe Workplace Suite](https://www.servicenow.com/docs/access?context=domain-separation-safe-workplace&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|See application site for individual application support levels|
|[SharePoint Online Search Connector](https://www.servicenow.com/docs/access?context=sharepoint-online-search-connector-domain-separation&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|Basic|
|[Universal Request](https://www.servicenow.com/docs/access?context=domain-sep-universal-request&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|Basic|
|[Universal Task](https://www.servicenow.com/docs/access?context=domain-sep-universal-task&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|Basic|
|[Workforce Optimization for HR](https://www.servicenow.com/docs/access?context=wfo-hr-overview&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)|Basic|
|[Environmental, Social, and Governance Management](https://www.servicenow.com/docs/access?context=esg-landing-page&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)|[Environmental, Social, and Governance Management](https://www.servicenow.com/docs/access?context=esg-landing-page&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)|No support\*|
|[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=australia&pubname=australia-field-service-management&ft:locale=en-US)|[Field Service Management](https://www.servicenow.com/docs/access?context=domain-separation-field-service&version=australia&pubname=australia-field-service-management&ft:locale=en-US)|Basic|
|[Governance, Risk, and Compliance](https://www.servicenow.com/docs/access?context=r_WhatIsGRC&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|[Advanced Risk](https://www.servicenow.com/docs/access?context=domain-separation-risk-management&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Audit Management](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|Business Continuity Management|Basic|
|[Compliance Case Management](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Governance, Risk, and Compliance \(GRC\)](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|Model Risk Management|Basic|
|[Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Privacy Management](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Policy and Compliance](https://www.servicenow.com/docs/access?context=domain-separation-pol-comp&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Regulatory Change Management](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|No support\*|
|[Third-party risk management](https://www.servicenow.com/docs/access?context=tprm-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[GRC: Metrics](https://www.servicenow.com/docs/access?context=esg-domain-separation&version=australia&pubname=australia-environmental-social-governance&ft:locale=en-US)|Basic|
|Now Assist for TPRM|No support\*|
|Now Assist for IRM|No support\*|
|[Smart Assessment Engine](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Industry Products](https://www.servicenow.com/docs/access?context=industry-products-landing&version=australia&pubname=australia-industry-products&ft:locale=en-US)|
|•[Financial Services](https://www.servicenow.com/docs/access?context=fso-overview&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)|Financial Services Card Operations|Basic|
|Financial Services Deposit Operations|Basic|
|Financial Services Loan Operations|Basic|
|[Financial Services Payment Operations](https://www.servicenow.com/docs/access?context=domain-separation-financial-services-payment-operations&version=australia&pubname=australia-financial-services-operations&ft:locale=en-US)|Basic|
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
|• [Healthcare and Life Sciences](https://www.servicenow.com/docs/access?context=hcls-overview&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)|[EMR Help](https://www.servicenow.com/docs/access?context=emr-help-domain-sep&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Healthcare and Life Sciences Service Management Core](https://www.servicenow.com/docs/access?context=hcls-domain-sep-serv-mgmt-core&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Pre-Visit Management](https://www.servicenow.com/docs/access?context=pre-visit-domain-sep&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Patient Support Services](https://www.servicenow.com/docs/access?context=pss-domain-sep&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Vaccine Administration Management](https://www.servicenow.com/docs/access?context=VAM-domain-separation&version=australia&pubname=australia-healthcare-life-sciences&ft:locale=en-US)|Basic|
|Healthcare Operations Core|Basic|
|Care Team Operations for Healthcare IT|Basic|
|Care Team Operations for Biomed|Basic|
|Care Team Operations for Facilities|Basic|
|Care Team Operations for Environmental Services|Basic|
|[Manufacturing Commercial Operations](https://www.servicenow.com/docs/access?context=manufacturing-overview&version=australia&pubname=australia-manufacturing&ft:locale=en-US)|[Manufacturing Commercial Operations](https://www.servicenow.com/docs/access?context=mco-domain-separation&version=australia&pubname=australia-manufacturing&ft:locale=en-US)|Basic|
|[Retail Core](https://www.servicenow.com/docs/access?context=mco-domain-separation&version=australia&pubname=australia-manufacturing&ft:locale=en-US)|Basic|
|[Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=bun-public-sector-landing-page&version=australia&pubname=australia-government-industry&ft:locale=en-US)|Public Sector Digital Services|Basic|
|[Telecommunications, Media, and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=telecom-media-tech-landing&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)|[Customer Success Management](https://www.servicenow.com/docs/access?context=account-lifecycle-domain-separation&version=australia&pubname=australia-acct-lifecycle-events&ft:locale=en-US)|Basic|
|Customer Service Problem Management|Basic|
|[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US)|Basic \(Inherited from [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)\).|
|[Proactive Service Experience Workflows](https://www.servicenow.com/docs/access?context=domain-separation-assurance-workflows&version=australia&pubname=australia-proactive-service-exp-workflows&ft:locale=en-US)|Standard|
|[Service Bridge](https://www.servicenow.com/docs/access?context=service-bridge-v2-domain-separation&version=australia&pubname=australia-service-exchange&ft:locale=en-US)|Standard|
|[Exploring Technology Product Support Case](https://www.servicenow.com/docs/access?context=tech-product-support-case-app&version=australia&pubname=australia-proactive-service-exp-workflows&ft:locale=en-US)|Basic \(Inherited from [Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)\).|
|[Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=domain-seperation-telecommunication-network-inventory&version=australia&pubname=australia-telecom-network-inventory&ft:locale=en-US)|Basic|
|[IT Asset Management](https://www.servicenow.com/docs/access?context=it-asset-management&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)|[Cloud Insights](https://www.servicenow.com/docs/access?context=domain-separation-cloudin&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)|No support|
|[Hardware Asset Management](https://www.servicenow.com/docs/access?context=domain-separation-ham&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)|Enhanced|
|[Software Asset Management](https://www.servicenow.com/docs/access?context=domain-separation-software-asset-management&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)|Enhanced|
|[Enterprise Asset Management](https://www.servicenow.com/docs/access?context=domain-separation-eam&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)|Standard|
|[Asset Audit Response](https://www.servicenow.com/docs/access?context=asset-audit-response-domain-separation&version=australia&pubname=australia-it-asset-management&ft:locale=en-US)|Basic|
|[Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=r_ITBusinessManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|[Agile Development](https://www.servicenow.com/docs/access?context=agile-development-2.0-domain-separation&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic\*|
|[Alignment Planner Workspace](https://www.servicenow.com/docs/access?context=alignment-planner-domain-separation&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic|
|Application Portfolio Management|Basic|
|[Cost Management](https://www.servicenow.com/docs/access?context=domain-separation-cost-management&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|No support|
|[Demand Management](https://www.servicenow.com/docs/access?context=domain-sep-demand-mgt&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic|
|Financial Management|No support|
|[Investment Funding](https://www.servicenow.com/docs/access?context=domain-separation-investment-funding&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic|
|[Project Portfolio Management](https://www.servicenow.com/docs/access?context=domain-separation-project-portfolio-financials&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic\*|
|[Release Management](https://www.servicenow.com/docs/access?context=domain-separation-release-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic\*|
|[Scaled Agile Framework \(SAFe\)](https://www.servicenow.com/docs/access?context=domain-separation-scaled-agile-framework&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic\*|
|[Test Management](https://www.servicenow.com/docs/access?context=domain-separation-test-management&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic\*|
|[Goal Framework](https://www.servicenow.com/docs/access?context=goal-framework-domain-separation&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic|
|[IT Operations Management](https://www.servicenow.com/docs/access?context=r_ITOMApplications&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|[Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=domain-separation-cloud-management&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|[Agent Client Collector](https://www.servicenow.com/docs/access?context=domain-separation-agent-client-collector&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|[Discovery](https://www.servicenow.com/docs/access?context=c_DiscoveryDomainSeparation&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Standard|
|[Event Management](https://www.servicenow.com/docs/access?context=domain-separation-event-management&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|Service Operations Workspace for ITOM|Basic|
|[Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-domain-separation&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|[Metric Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-operational-intelligence&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|[Service Mapping](https://www.servicenow.com/docs/access?context=domain-separation-service-mapping&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|Cloud Migration Assessment|Basic|
|Action Library|No support|
|Cloud Configuration Governance|No support|
|[Tag Governance](https://www.servicenow.com/docs/access?context=tag-governance-domain-separation&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|Cloud Insights Billing|No support|
|[Cloud Provisioning and Governance: Google Cloud](https://www.servicenow.com/docs/access?context=cloud-mgmt-dom-sep-recommend&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|m[Cloud Provisioning and Governance Terrafor](https://www.servicenow.com/docs/access?context=domain-separation-cloud-management&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)|Basic|
|Cloud Operation Workspace|Basic|
|Cloud Discovery|Standard|
|Synthetic Monitoring|Basic|
|Service Observability|Basic|
|[IT Service Management](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|[Benchmarks](https://www.servicenow.com/docs/access?context=domain-separation-benchmarks&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|No support|
|[Change Management](https://www.servicenow.com/docs/access?context=domain-separation-change-mgt&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic|
|Coaching|Basic|
|[Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-domain-separation&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic|
|[Contract Management](https://www.servicenow.com/docs/access?context=domain-separation-contract-mgmt&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|No support|
|Digital End-User Experience|No support|
|[Domain separation and Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-domain-separation-digital-product-release&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic|
|[Expense Line](https://www.servicenow.com/docs/access?context=r_InstalledWithExpenseLine&version=australia&pubname=australia-it-service-management&section=domain-separation-expense-line&ft:locale=en-US)|No support|
|[Incident Communications Management](https://www.servicenow.com/docs/access?context=domain-separation-incident-comm-mgt&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard|
|[Incident Management](https://www.servicenow.com/docs/access?context=domain-separation-incident-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard|
|[Facilities Service Management](https://www.servicenow.com/docs/access?context=domain-separation-facilities-service-mgt&version=australia&pubname=australia-service-management-for-the-enterprise&ft:locale=en-US)|Standard|
|[Incident Management](https://www.servicenow.com/docs/access?context=domain-separation-incident-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard|
|[On-Call Scheduling](https://www.servicenow.com/docs/access?context=domain-separation-on-call-scheduling&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard|
|Asset Management|Basic|
|[Problem Management](https://www.servicenow.com/docs/access?context=domain-separation-and-problem-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard|
|[Procurement](https://www.servicenow.com/docs/access?context=domain-separation-procurement&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard\*|
|[Product Catalog](https://www.servicenow.com/docs/access?context=domain-separation-product-catalog&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard|
|[Request Management](https://www.servicenow.com/docs/access?context=domain-sep-req-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Standard|
|[Service Catalog](https://www.servicenow.com/docs/access?context=domain-separation-service-catalog-management&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Standard|
|[Service Level Management](https://www.servicenow.com/docs/access?context=domain-separation-sla&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic|
|[Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic\*|
|Site Reliability Operations|Basic\*|
|[Task outage](https://www.servicenow.com/docs/access?context=domain-separation-task-outage&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic|
||No support|
|[Walk-up Experience](https://www.servicenow.com/docs/access?context=domain-separation-walkup-experience&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic|
|[Configure Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=configure-now-assist-for-itsm&version=australia&pubname=australia-it-service-management&ft:locale=en-US)|Basic|
|[Mobile Configuration and Navigation](https://www.servicenow.com/docs/access?context=mobile-config-navigation&version=australia&pubname=australia-mobile&ft:locale=en-US)|[Mobile](https://www.servicenow.com/docs/access?context=mobile-domain-separation&version=australia&pubname=australia-mobile&ft:locale=en-US)|Basic|
|[Now Intelligence](https://www.servicenow.com/docs/access?context=c_performanceAnalyticsAndReporting&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)|[Dashboards](https://www.servicenow.com/docs/access?context=domain-separation-in-dashboards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)|Basic|
|[Performance Analytics](https://www.servicenow.com/docs/access?context=c_PAWithDomainSeparation&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)|Enhanced|
|[Process Optimization](https://www.servicenow.com/docs/access?context=domain-separation-process-optimization&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)|Basic|
|[Reporting](https://www.servicenow.com/docs/access?context=domain-separation-in-reporting&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)|Basic|
|[Usage Insights](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)|Basic|
|[The ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=now-platform-landing&version=australia&pubname=australia-now-platform&ft:locale=en-US)|[Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-domain-separation&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)|Standard|
|[Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-reference&version=australia&pubname=australia-conversational-interfaces&section=domain-separation-agent-chat&ft:locale=en-US)|Standard|
|[AI Search/Now Assist in AI Search](https://www.servicenow.com/docs/access?context=ai-search-domain-separation&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Searches respect domain restrictions from indexed records|
|[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-domain-sep&version=australia&pubname=australia-application-development&ft:locale=en-US)|No support|
|[Application Management](https://www.servicenow.com/docs/access?context=app-management-domain-separation&version=australia&pubname=australia-application-development&ft:locale=en-US)|No support|
|[Assessments](https://www.servicenow.com/docs/access?context=domain-separation-assessments&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Standard|
|[Automated Test Framework](https://www.servicenow.com/docs/access?context=domain-separation-auto-test-framework&version=australia&pubname=australia-application-development&ft:locale=en-US)|Standard\*|
|[ServiceNow Voice](https://www.servicenow.com/docs/access?context=domain-separation-voice&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Basic|
|[Code Signing](../../encryption/concept/code-signing-landing.md)|No support|
|[Contextual Search](https://www.servicenow.com/docs/access?context=domain-separation-contextual-search&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Standard|
|[Configuration Management \(CMDB\)](https://www.servicenow.com/docs/access?context=domain-separation-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Standard|
|[Content Management System](https://www.servicenow.com/docs/access?context=domain-separation-content-management&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)|No support|
|[Credentials and Connections](../../../product/credentials/concept/domain-separation-credentials_conn.md)|Standard|
|Data Certification|Basic\*|
|[Data Classification](../../security/concept/domain-separation-data-classification.md)|Enhanced|
|Data Privacy|No support|
|[Data Management](https://www.servicenow.com/docs/access?context=domain-separation-data-management&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Basic\*|
|[Delegated Development](https://www.servicenow.com/docs/access?context=domain-separation-delegated-development&version=australia&pubname=australia-application-development&ft:locale=en-US)|No support|
|[Dependency Views](https://www.servicenow.com/docs/access?context=domain-separation-dependency-views&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Basic|
|[Document Services](https://www.servicenow.com/docs/access?context=domain-separation-document-services&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|No support|
|[Dynamic Translation](https://www.servicenow.com/docs/access?context=domain-sep-dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Basic|
|[Edge Encryption](../../edge-encryption/concept/edge-encryption-domain-separation.md)|Basic support|
|External Content Connectors|No support\*|
|[Field Encryption](../../encryption/concept/field-encryption.md)|No support|
|[Encryption](../../security/concept/encryption-landing.md)|No support|
|[Cloud Encryption with Key Management](../../encryption-dare/concept/dare-overview.md)|Basic support|
|[Field Normalization](https://www.servicenow.com/docs/access?context=domain-separation-field-normalization&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|No support|
|[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-domain-separation&version=australia&pubname=australia-build-workflows&ft:locale=en-US)|Standard\*|
|[Guided Setup](https://www.servicenow.com/docs/access?context=domain-separation-guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)|No support|
|[Domain separation and Integration Hub](https://www.servicenow.com/docs/access?context=domain-separation-integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)|Standard\*|
|[Integrations with third-party applications and data sources](https://www.servicenow.com/docs/access?context=domain-separation-app-data-source-integration&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Basic+Standard|
|[Knowledge Management](https://www.servicenow.com/docs/access?context=domain-separation-knowledge&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Standard|
|Hermes Messaging Service|Basic|
|[Managed Documents](https://www.servicenow.com/docs/access?context=domain-separation-managed-documents&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|No support|
|[MetricBase](https://www.servicenow.com/docs/access?context=domain-separation-metricbase&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Basic|
|[Natural Language Understanding](https://www.servicenow.com/docs/access?context=domain-separation-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)|Basic+Standard|
|[Notifications](https://www.servicenow.com/docs/access?context=domain-separation-notifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Standard|
|[ODBC Driver](https://www.servicenow.com/docs/access?context=domain-separation-odbc-driver&version=australia&pubname=australia-api-reference&ft:locale=en-US)|Basic\*|
|[Orchestration](https://www.servicenow.com/docs/access?context=domain-separation-orchestration&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Standard\*|
|[Password Reset](https://www.servicenow.com/docs/access?context=domain-separation-pwd-reset&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Standard|
|[Platform Security](domain-sep-landing-page.md)|Domain separation landing page|
|Data Privacy|No support|
|[Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)|Standard|
|Proactive Triggers|Basic|
|[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer-domain-separation&version=australia&pubname=australia-build-workflows&ft:locale=en-US)|Basic|
|[Remote Tables](https://www.servicenow.com/docs/access?context=domain-separation-remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|No support|
|[Schedules](https://www.servicenow.com/docs/access?context=domain-support-for-schedules&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Basic|
|[Script debugger](https://www.servicenow.com/docs/access?context=domain-separation-script-debugging&version=australia&pubname=australia-api-reference&ft:locale=en-US)|Basic|
|[Search Suggestions](https://www.servicenow.com/docs/access?context=domain-separation-search-suggestions&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|No support|
|[Service Portal](https://www.servicenow.com/docs/access?context=domain-separation-service-portal&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)|No support|
|Service Graph Connectors|No support|
|[Domain separation and Sidebar](https://www.servicenow.com/docs/access?context=sidebar-domain-separation&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)|Standard|
|[State Flows](https://www.servicenow.com/docs/access?context=domain-separation-state-flows&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|No support|
|Subscription Management|Basic\*|
|[Survey Management](https://www.servicenow.com/docs/access?context=domain-separation-surveys&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)|Basic\*|
|Task Intelligence|No support|
|[Domain separation and Time Card](https://www.servicenow.com/docs/access?context=domain-separation-time-card&version=australia&pubname=australia-it-business-management&ft:locale=en-US)|Basic\*|
|[UI Builder](https://www.servicenow.com/docs/access?context=uib-domain-sep&version=australia&pubname=australia-application-development&ft:locale=en-US)|Standard|
|[Virtual Agent](https://www.servicenow.com/docs/access?context=domain-separation-virtual-agent&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)|Basic|
|[Visual Task Boards](https://www.servicenow.com/docs/access?context=domain-separation-visual-task-boards&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)|Basic|
|[Web Services](https://www.servicenow.com/docs/access?context=domain-separation-web-services&version=australia&pubname=australia-api-reference&ft:locale=en-US)|Standard\*|
|[Workflow](https://www.servicenow.com/docs/access?context=c_WorkflowsAndDomainSeparation&version=australia&pubname=australia-build-workflows&ft:locale=en-US)|Standard\*|
|Workspace|Standard|
|Platform Fundamentals|[Impact](https://www.servicenow.com/docs/access?context=impact-landing-page&version=australia&pubname=australia-impact&ft:locale=en-US)|No support|
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
|[Domain separation and Subscription Management](https://www.servicenow.com/docs/access?context=domain-separation-subscription-mgmt&version=australia&pubname=australia-platform-administration&ft:locale=en-US)|Basic\*|
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
|[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&version=australia&pubname=australia-security-management&ft:locale=en-US)|Subscription Management[Configuration Compliance](https://www.servicenow.com/docs/access?context=domain-separation-config-compliance&version=australia&pubname=australia-security-management&ft:locale=en-US)|Standard|
|[IBM QRadar Offense Ingestion](https://www.servicenow.com/docs/access?context=qradar-ibm-domain-sep&version=australia&pubname=australia-security-management&ft:locale=en-US)|Basic|
|[Microsoft Graph Security API alert ingestion integration](https://www.servicenow.com/docs/access?context=ms-graph-domain-sep&version=australia&pubname=australia-security-management&ft:locale=en-US)|Basic|
|[Security Incident Response](https://www.servicenow.com/docs/access?context=domain-separation-security-incident-response&version=australia&pubname=australia-security-management&ft:locale=en-US)|Standard|
|[Threat Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-threat-intelligence&version=australia&pubname=australia-security-management&ft:locale=en-US)|Standard|
|Threat Intelligence Security Center|Standard|
|[Vulnerability Response](https://www.servicenow.com/docs/access?context=domain-separation-vulnerability-response&version=australia&pubname=australia-security-management&ft:locale=en-US)|Standard|
|[Service Management](https://www.servicenow.com/docs/access?context=c_ServiceManagement&version=australia&pubname=australia-service-management-for-the-enterprise&ft:locale=en-US)|[Facilities Service Management](https://www.servicenow.com/docs/access?context=domain-separation-facilities-service-mgt&version=australia&pubname=australia-service-management-for-the-enterprise&ft:locale=en-US)|Standard|
|[Planned Maintenance](https://www.servicenow.com/docs/access?context=domain-separation-planned-maintenance&version=australia&pubname=australia-service-management-for-the-enterprise&ft:locale=en-US)|Standard\*|
|Structured Problem Analysis|No support|
|Workforce Optimization for ITSM|Basic|
|Vendor Management Workspace|Basic|
|[Proactive Triggers](https://www.servicenow.com/docs/access?context=proactive-triggers&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)|Basic|
|Employee Service Management|SharePoint Online Search Connector|Basic|
|Workforce Optimization for ITSM|Basic|
|Application Portfolio Management|Application Portfolio Management|Basic|
|Domain separation and Conversational Analytics|Basic|
|[Sales Customer Relationship Management](https://www.servicenow.com/docs/access?context=order-mgt-overview&version=australia&pubname=australia-order-management&ft:locale=en-US)|Advanced Approval for Sales Management|Enhanced|

**Parent Topic:**[Domain separation for service providers](domain-sep-landing-page.md)

