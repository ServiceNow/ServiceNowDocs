---
title: Application support for domain separation
description: Many ServiceNow applications support domain separation in the base system but not all. Some supported applications include limitations on the data and administrative settings that can be domain-separated. These definitions delineate the domain separation support levels from the perspective of actual use cases and the people who use them.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
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
|[App development and low-code](https://www.servicenow.com/docs/access?context=hyperautomation-low-code-landing-page&version=yokohama&pubname=yokohama-hyperautomation-low-code&ft:locale=en-US)|[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|No support|
|[Automation Center](https://www.servicenow.com/docs/access?context=automation-center-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|Basic|
|[Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|Basic|
|ServiceNow Studio|No support|
|[Table Builder](https://www.servicenow.com/docs/access?context=tb-landing-page&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|Basic|
|[App Engine Management Center](https://www.servicenow.com/docs/access?context=manage-app-development&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|No support|
|[Exploring Decision Tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)|Standard|
|Enterprise Resource Planning Integration|No support|
|Enterprise Resource Planning Customization Mining|No support|
|[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|Basic|
|[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)|[Communities](https://www.servicenow.com/docs/access?context=domain-separation-communities&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)|No support|
|[Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)|Basic|
|[Release Management](https://www.servicenow.com/docs/access?context=domain-separation-release-management&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic\*|
|Order Management for Customer Service Management|Basic|
|Post-Sales Support|Basic|
|[Domain separation in Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=domain-separation-configurable-wfo-cs&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)|Basic|
|[DevOps](https://www.servicenow.com/docs/access?context=dev-ops-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|[Domain separation and DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-domain-separation&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|No support|
|[Domain separation and DevOps Config](https://www.servicenow.com/docs/access?context=devops-config-domain-separation&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|
|[Employee Service Management](https://www.servicenow.com/docs/access?context=employee-service-management-overview&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|[HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-domain-separation&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|Basic\*|
|[Health and Safety](https://www.servicenow.com/docs/access?context=health-safety-domain-separation&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|No support|
|[Contract Management Pro](https://www.servicenow.com/docs/access?context=cncore-cmpro-landing-page&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|Basic|
|[Legal Service Delivery](https://www.servicenow.com/docs/access?context=legal-domain-separation&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|Basic|
|[Procurement Service Management \(PSM\)](https://www.servicenow.com/docs/access?context=psm-domain-separation&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)|No support|
|[Safe Workplace Suite](https://www.servicenow.com/docs/access?context=domain-separation-safe-workplace&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|See application site for individual application support levels|
|[SharePoint Online Search Connector](https://www.servicenow.com/docs/access?context=sharepoint-online-search-connector-domain-separation&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|Basic|
|[Universal Request](https://www.servicenow.com/docs/access?context=domain-sep-universal-request&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|Basic|
|[Universal Task](https://www.servicenow.com/docs/access?context=domain-sep-universal-task&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|Basic|
|[Workforce Optimization for HR](https://www.servicenow.com/docs/access?context=wfo-hr-overview&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)|Basic|
|[Environmental, Social, and Governance Management](https://www.servicenow.com/docs/access?context=esg-landing-page&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)|[Environmental, Social, and Governance Management](https://www.servicenow.com/docs/access?context=esg-landing-page&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)|Basic|
|[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)|[Field Service Management](https://www.servicenow.com/docs/access?context=domain-separation-field-service&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)|Basic|
|[Governance, Risk, and Compliance](https://www.servicenow.com/docs/access?context=r_WhatIsGRC&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|Business Continuity Management|Basic|
|[Governance, Risk, and Compliance \(GRC\)](https://www.servicenow.com/docs/access?context=grc-domain-separation&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Operational Resilience](https://www.servicenow.com/docs/access?context=grc-opres-landing-page&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)|Basic|
|[Industry Products](https://www.servicenow.com/docs/access?context=industry-products-landing&version=yokohama&pubname=yokohama-industry-products&ft:locale=en-US)|
|•[Financial Services](https://www.servicenow.com/docs/access?context=fso-overview&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)|[Financial Services Card Operations](https://www.servicenow.com/docs/access?context=domain-separation-fso-card-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)|Basic|
|Financial Services Deposit Operations|
|[Financial Services Payment Operations](https://www.servicenow.com/docs/access?context=domain-separation-financial-services-payment-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)|
|Intelligent Servicing for Fraud|
|Property and Casualty Insurance Servicing|
|Life Insurance Servicing|
|Insurance Claims|
|Financial Services Know Your Customer|
|Financial Services Credit Operation|
|[Financial Services Document Processor](domain-separated-apps.md)|
|• [Healthcare and Life Sciences](https://www.servicenow.com/docs/access?context=hcls-overview&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)|[EMR Help](https://www.servicenow.com/docs/access?context=emr-help-domain-sep&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Healthcare and Life Sciences Service Management Core](https://www.servicenow.com/docs/access?context=hcls-domain-sep-serv-mgmt-core&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Pre-Visit Management](https://www.servicenow.com/docs/access?context=pre-visit-domain-sep&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Patient Support Services](https://www.servicenow.com/docs/access?context=pss-domain-sep&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)|Basic|
|[Vaccine Administration Management](https://www.servicenow.com/docs/access?context=VAM-domain-separation&version=yokohama&pubname=yokohama-healthcare-life-sciences&ft:locale=en-US)|Basic|
|Manufacturing Commercial Operations|[Manufacturing Commercial Operations](https://www.servicenow.com/docs/access?context=mco-domain-separation&version=yokohama&pubname=yokohama-manufacturing&ft:locale=en-US)|Standard|
|Retail Core|Basic|
|Retail Task Management|Basic|
|• [Manufacturing](https://www.servicenow.com/docs/access?context=manufacturing-domain-separation&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)|[Industrial Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)|Standard|
|[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)|Standard|
|[Operational Technology Vulnerability Response](https://www.servicenow.com/docs/access?context=oper-tech-vulnerability-response-landing-page&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)|Standard|
|[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)|Standard|
|[Telecommunications, Media, and Technology](https://www.servicenow.com/docs/access?context=telecom-media-tech-landing&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)|[Account Lifecycle Events](https://www.servicenow.com/docs/access?context=account-lifecycle-domain-separation&version=yokohama&pubname=yokohama-acct-lifecycle-events&ft:locale=en-US)|Basic|
|[Customer Service Problem Management](https://www.servicenow.com/docs/access?context=domain-separation-cspm&version=yokohama&pubname=yokohama-proactive-service-exp-workflows&ft:locale=en-US)|Basic|
|[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)|Basic \(Inherited from [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)\).|
|[Proactive Service Experience Workflows](https://www.servicenow.com/docs/access?context=domain-separation-assurance-workflows&version=yokohama&pubname=yokohama-proactive-service-exp-workflows&ft:locale=en-US)|Standard|
|[Service Bridge](https://www.servicenow.com/docs/access?context=service-bridge-v2-domain-separation&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)|Standard|
|[Technology Product Support Case application](https://www.servicenow.com/docs/access?context=tech-product-support-case-app&version=yokohama&pubname=yokohama-proactive-service-exp-workflows&ft:locale=en-US)|Basic \(Inherited from [Customer Service Management](https://www.servicenow.com/docs/access?context=domain-separation-customer-service&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)\).|
|[Telecommunications Network Inventory](https://www.servicenow.com/docs/access?context=domain-seperation-telecommunication-network-inventory&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)|Basic|
|[IT Asset Management](https://www.servicenow.com/docs/access?context=it-asset-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)|[Cloud Insights](https://www.servicenow.com/docs/access?context=domain-separation-cloudin&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)|No support|
|[Hardware Asset Management](https://www.servicenow.com/docs/access?context=domain-separation-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)|Enhanced|
|[Software Asset Management](https://www.servicenow.com/docs/access?context=domain-separation-software-asset-management&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)|Enhanced|
|Enterprise Asset Management|Standard|
|[Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=r_ITBusinessManagement&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|[Agile Development](https://www.servicenow.com/docs/access?context=agile-development-2.0-domain-separation&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic\*|
|[Alignment Planner Workspace](https://www.servicenow.com/docs/access?context=alignment-planner-domain-separation&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic|
|[Application Portfolio Management](https://www.servicenow.com/docs/access?context=domain-separation-app-portfolio-mgt&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)|Basic|
|[Cost Management](https://www.servicenow.com/docs/access?context=domain-separation-cost-management&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|No support|
|[Demand Management](https://www.servicenow.com/docs/access?context=domain-sep-demand-mgt&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic|
|Financial Management|No support|
|[Investment Funding](https://www.servicenow.com/docs/access?context=domain-separation-investment-funding&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic|
|[Project Portfolio Management](https://www.servicenow.com/docs/access?context=domain-separation-project-portfolio-financials&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic\*|
|[Release Management](https://www.servicenow.com/docs/access?context=domain-separation-release-management&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic\*|
|[Scaled Agile Framework \(SAFe\)](https://www.servicenow.com/docs/access?context=domain-separation-scaled-agile-framework&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic\*|
|[Test Management](https://www.servicenow.com/docs/access?context=domain-separation-test-management&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic\*|
|Goal Framework|Basic|
|[IT Operations Management](https://www.servicenow.com/docs/access?context=r_ITOMApplications&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|[Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=domain-separation-cloud-management&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|Basic|
|Agent Client Collector|Basic|
|[Discovery](https://www.servicenow.com/docs/access?context=c_DiscoveryDomainSeparation&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|Standard|
|[Event Management](https://www.servicenow.com/docs/access?context=domain-separation-event-management&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|Basic|
|Service Operations Workspace for ITOM|Basic|
|[Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-domain-separation&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|Basic|
|[Metric Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-operational-intelligence&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|Basic|
|[Service Mapping](https://www.servicenow.com/docs/access?context=domain-separation-service-mapping&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|Basic|
|Cloud Migration Assessment|Basic|
|Action Library|No support|
|Cloud Configuration Governance|No support|
|[Tag Governance](https://www.servicenow.com/docs/access?context=tag-governance-domain-separation&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|Basic|
|Cloud Insights Billing|No support|
|Cloud Provisioning and Governance: Google Cloud|Basic|
|Cloud Provisioning and Governance Terraform|Basic|
|Cloud Operation Workspace|Basic|
|Cloud Discovery|Standard|
|[IT Service Management](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|[Benchmarks](https://www.servicenow.com/docs/access?context=domain-separation-benchmarks&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|No support|
|[Change Management](https://www.servicenow.com/docs/access?context=domain-separation-change-mgt&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[Coaching](https://www.servicenow.com/docs/access?context=domain-separation-coaching&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-domain-separation&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[Contract Management](https://www.servicenow.com/docs/access?context=domain-separation-contract-mgmt&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|No support|
|[Domain separation and Digital Product Release](https://www.servicenow.com/docs/access?context=dpr-domain-separation-digital-product-release&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[Expense Line](https://www.servicenow.com/docs/access?context=r_InstalledWithExpenseLine&version=yokohama&pubname=yokohama-it-service-management&section=domain-separation-expense-line&ft:locale=en-US)|No support|
|[Incident Communications Management](https://www.servicenow.com/docs/access?context=domain-separation-incident-comm-mgt&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard|
|[Incident Management](https://www.servicenow.com/docs/access?context=domain-separation-incident-management&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard|
|[Facilities Service Management](https://www.servicenow.com/docs/access?context=domain-separation-facilities-service-mgt&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)|Standard|
|[Incident Management](https://www.servicenow.com/docs/access?context=domain-separation-incident-management&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard|
|[On-Call Scheduling](https://www.servicenow.com/docs/access?context=domain-separation-on-call-scheduling&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard|
|Asset Management|Basic|
|[Problem Management](https://www.servicenow.com/docs/access?context=domain-separation-and-problem-management&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard|
|[Procurement](https://www.servicenow.com/docs/access?context=domain-separation-procurement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard\*|
|[Product Catalog](https://www.servicenow.com/docs/access?context=domain-separation-product-catalog&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard|
|[Request Management](https://www.servicenow.com/docs/access?context=domain-sep-req-management&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Standard|
|[Service Catalog](https://www.servicenow.com/docs/access?context=domain-separation-service-catalog-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Standard|
|[Service Level Management](https://www.servicenow.com/docs/access?context=domain-separation-sla&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[Service Portfolio Management](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic\*|
|Site Reliability Operations|Basic\*|
|[Task outage](https://www.servicenow.com/docs/access?context=domain-separation-task-outage&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[Domain separation and Vendor Management Workspace](https://www.servicenow.com/docs/access?context=domain-sep-vendor-management-workspace&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|No support|
|[Walk-up Experience](https://www.servicenow.com/docs/access?context=domain-separation-walkup-experience&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[Mobile Configuration and Navigation](https://www.servicenow.com/docs/access?context=mobile-config-navigation&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)|[Mobile](https://www.servicenow.com/docs/access?context=mobile-domain-separation&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)|Basic|
|[Now Intelligence](https://www.servicenow.com/docs/access?context=c_performanceAnalyticsAndReporting&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)|[Dashboards](https://www.servicenow.com/docs/access?context=domain-separation-in-dashboards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)|Basic|
|[Performance Analytics](https://www.servicenow.com/docs/access?context=c_PAWithDomainSeparation&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)|Enhanced|
|[Process Optimization](https://www.servicenow.com/docs/access?context=domain-separation-process-optimization&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)|Basic|
|[Reporting](https://www.servicenow.com/docs/access?context=domain-separation-in-reporting&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)|Basic|
|[User Experience Analytics](https://www.servicenow.com/docs/access?context=user-exp-analytics-landing&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)|Basic|
|[The ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=now-platform-landing&version=yokohama&pubname=yokohama-now-platform&ft:locale=en-US)|[Administration](https://www.servicenow.com/docs/access?context=intro-now-platform-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)| |
|[Domain separation and Agent Chat](https://www.servicenow.com/docs/access?context=ci-agent-chat-reference&version=yokohama&pubname=yokohama-conversational-interfaces&section=domain-separation-agent-chat&ft:locale=en-US)|Standard|
|[ServiceNow AI Platform Capabilities](https://www.servicenow.com/docs/access?context=capabilities-bundle-landingpage&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)| |
|[User Interface](https://www.servicenow.com/docs/access?context=c_NavigationAndTheUserInterface&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)| |
|[Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-domain-separation&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Standard|
|[AI Search](https://www.servicenow.com/docs/access?context=ai-search-domain-separation&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|Searches respect domain restrictions from indexed records|
|[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-domain-sep&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|No support|
|[Application Management](https://www.servicenow.com/docs/access?context=app-management-domain-separation&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|No support|
|[Assessments](https://www.servicenow.com/docs/access?context=domain-separation-assessments&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Standard|
|[Automated Test Framework](https://www.servicenow.com/docs/access?context=domain-separation-auto-test-framework&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|Standard\*|
|[ServiceNow Voice](https://www.servicenow.com/docs/access?context=domain-separation-voice&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)| |
|[Code Signing](../../encryption/concept/code-signing-landing.md)|Basic support|
|[Contextual Search](https://www.servicenow.com/docs/access?context=domain-separation-contextual-search&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|Standard|
|[Configuration Management \(CMDB\)](https://www.servicenow.com/docs/access?context=domain-separation-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Standard|
|[Content Management System](https://www.servicenow.com/docs/access?context=domain-separation-content-management&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)|No support|
|[Credentials and Connections](../../../product/credentials/concept/domain-separation-credentials_conn.md)|Standard|
|[Data Certification](https://www.servicenow.com/docs/access?context=data-separation-data-certification&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Basic\*|
|[Data Classification](../../security/concept/domain-separation-data-classification.md)|Enhanced|
|Data Privacy|No support|
|[Data Management](https://www.servicenow.com/docs/access?context=domain-separation-data-management&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|Basic\*|
|[Delegated Development](https://www.servicenow.com/docs/access?context=domain-separation-delegated-development&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|No support|
|[Dependency Views](https://www.servicenow.com/docs/access?context=domain-separation-dependency-views&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Basic|
|[Document Services](https://www.servicenow.com/docs/access?context=domain-separation-document-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|No support|
|[Dynamic Translation](https://www.servicenow.com/docs/access?context=domain-sep-dynamic-translation&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|Basic|
|[Edge Encryption](../../edge-encryption/concept/edge-encryption-domain-separation.md)|Basic support|
|External Content Connectors|No support\*|
|[Field Encryption](../../encryption/concept/field-encryption.md)|No support|
|[Field Encryption Enterprise](../../now-platform-encryption/concept/now-platform-encryption.md)|No support|
|[Cloud Encryption with Key Management](../../encryption-dare/concept/dare-overview.md)|Basic support|
|[Field Normalization](https://www.servicenow.com/docs/access?context=domain-separation-field-normalization&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|No support|
|[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-domain-separation&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)|Standard\*|
|[Guided Setup](https://www.servicenow.com/docs/access?context=domain-separation-guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)|No support|
|[Domain separation and Integration Hub](https://www.servicenow.com/docs/access?context=domain-separation-integrationhub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|Standard\*|
|[Integrations with third-party applications and data sources](https://www.servicenow.com/docs/access?context=domain-separation-app-data-source-integration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|Basic+Standard|
|[Knowledge Management](https://www.servicenow.com/docs/access?context=domain-separation-knowledge&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Standard|
|Hermes Messaging Service|No support|
|[Managed Documents](https://www.servicenow.com/docs/access?context=domain-separation-managed-documents&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|No support|
|[MetricBase](https://www.servicenow.com/docs/access?context=domain-separation-metricbase&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Basic|
|Natural Language Understanding|Basic+Standard|
|[Notifications](https://www.servicenow.com/docs/access?context=domain-separation-notifications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|Standard|
|[ODBC Driver](https://www.servicenow.com/docs/access?context=domain-separation-odbc-driver&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|Basic\*|
|[Orchestration](https://www.servicenow.com/docs/access?context=domain-separation-orchestration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Standard\*|
|[Password Reset](https://www.servicenow.com/docs/access?context=domain-separation-pwd-reset&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Standard|
|[Platform Security](domain-sep-landing-page.md)|Domain separation landing page|
|Data Privacy|No support|
|[Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)|Standard|
|Proactive Triggers|Basic|
|[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer-domain-separation&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)|Basic|
|[Remote Tables](https://www.servicenow.com/docs/access?context=domain-separation-remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|No support|
|[Schedules](https://www.servicenow.com/docs/access?context=domain-support-for-schedules&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|Basic|
|[Script debugger](https://www.servicenow.com/docs/access?context=domain-separation-script-debugging&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|Basic|
|[Search Suggestions](https://www.servicenow.com/docs/access?context=domain-separation-search-suggestions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)|No support|
|[Service Portal](https://www.servicenow.com/docs/access?context=domain-separation-service-portal&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)|No support|
|Service Graph Connectors|No support|
|[Domain separation and Sidebar](https://www.servicenow.com/docs/access?context=sidebar-domain-separation&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)|Standard|
|[State Flows](https://www.servicenow.com/docs/access?context=domain-separation-state-flows&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|No support|
|Subscription Management|Basic\*|
|[Survey Management](https://www.servicenow.com/docs/access?context=domain-separation-surveys&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Basic\*|
|Task Intelligence|No support|
|[Domain separation and Time Card](https://www.servicenow.com/docs/access?context=domain-separation-time-card&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)|Basic\*|
|[UI Builder](https://www.servicenow.com/docs/access?context=uib-domain-sep&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)|Standard|
|[Virtual Agent](https://www.servicenow.com/docs/access?context=domain-separation-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)|Basic|
|[Visual Task Boards](https://www.servicenow.com/docs/access?context=domain-separation-visual-task-boards&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)|Basic|
|[Web Services](https://www.servicenow.com/docs/access?context=domain-separation-web-services&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)|Standard\*|
|[Workflow](https://www.servicenow.com/docs/access?context=c_WorkflowsAndDomainSeparation&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)|Standard\*|
|Workspace|Standard|
|[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)|[Configuration Compliance](https://www.servicenow.com/docs/access?context=domain-separation-config-compliance&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)|Standard|
|[Configuration Data Management](https://www.servicenow.com/docs/access?context=domain-separation-cdm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)|Basic|
|[IBM QRadar Offense Ingestion](https://www.servicenow.com/docs/access?context=qradar-ibm-domain-sep&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)|Basic|
|[Microsoft Graph Security API alert ingestion integration](https://www.servicenow.com/docs/access?context=ms-graph-domain-sep&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)|Basic|
|[Security Incident Response](https://www.servicenow.com/docs/access?context=domain-separation-security-incident-response&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)|Standard|
|[Threat Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-threat-intelligence&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)|Standard|
|[Vulnerability Response](https://www.servicenow.com/docs/access?context=domain-separation-vulnerability-response&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)|Standard|
|[Service Management](https://www.servicenow.com/docs/access?context=c_ServiceManagement&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)|[Facilities Service Management](https://www.servicenow.com/docs/access?context=domain-separation-facilities-service-mgt&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)|Standard|
|[Planned Maintenance](https://www.servicenow.com/docs/access?context=domain-separation-planned-maintenance&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US)|Standard\*|
|[Proactive Triggers](https://www.servicenow.com/docs/access?context=proactive-triggers&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)|Basic|
|NOW Code Editor|No support|
|Workforce Optimization for ITSM|Basic|
|Vendor Management Workspace|Basic|

**Parent Topic:**[Domain separation for service providers](domain-sep-landing-page.md)

