---
title: Application support for domain separation
description: Many ServiceNow applications support domain separation in the base system but not all. Some supported applications include limitations on the data and administrative settings that can be domain-separated. These definitions delineate the domain separation support levels from the perspective of actual use cases and the people who use them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-security/domain-separated-apps.html
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
|[App development and low-code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/hyperautomation-low-code/hyperautomation-low-code-landing-page.md)|App Engine Studio|No support|
|Automation Center|Basic|
|Robotic Process Automation \(RPA\) Hub|Basic|
|ServiceNow Studio|No support|
|Table Builder|Basic|
|App Engine Management Center|No support|
|[Exploring Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/decision-designer-overview.md)|Standard|
|Enterprise Resource Planning Integration|No support|
|Enterprise Resource Planning Customization Mining|No support|
|Next Experience UI Builder|Basic|
|[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/c_CustomerServiceManagement.md)|Communities|No support|
|Customer Service Management|Basic|
|Release Management|Basic\*|
|Order Management for Customer Service Management|Basic|
|Post-Sales Support|Basic|
||Basic|
|DevOps||No support|
||
|Employee Service Management|HR Service Delivery|Basic\*|
|Health and Safety|No support|
||Basic|
|Legal Service Delivery|Basic|
|[Procurement Service Management \(PSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/sourcing-and-procurement-operations/psm-domain-separation.md)|No support|
|Safe Workplace Suite|See application site for individual application support levels|
|SharePoint Online Search Connector|Basic|
|Universal Request|Basic|
|Universal Task|Basic|
|Workforce Optimization for HR|Basic|
|Environmental, Social, and Governance Management|Environmental, Social, and Governance Management|Basic|
||Field Service Management|Basic|
|Governance, Risk, and Compliance|Business Continuity Management|Basic|
|Governance, Risk, and Compliance \(GRC\)|Basic|
|Operational Resilience|Basic|
|[Industry Products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/industry-products/industry-products-landing.md)|
|•|Financial Services Card Operations|Basic|
|Financial Services Deposit Operations|
|Financial Services Payment Operations|
|Intelligent Servicing for Fraud|
|Property and Casualty Insurance Servicing|
|Life Insurance Servicing|
|Insurance Claims|
|Financial Services Know Your Customer|
|Financial Services Credit Operation|
|[Financial Services Document Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/domain-separated-apps.md)|
|• [Healthcare and Life Sciences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/healthcare-life-sciences/healthcare-and-life-sciences/hcls-overview.md)|[EMR Help](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/healthcare-life-sciences/emr-help/emr-help-domain-sep.md)|Basic|
|[Healthcare and Life Sciences Service Management Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-domain-sep-serv-mgmt-core.md)|Basic|
|[Pre-Visit Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/healthcare-life-sciences/pre-visit-domain-sep.md)|Basic|
|[Patient Support Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/healthcare-life-sciences/pss-domain-sep.md)|Basic|
|[Vaccine Administration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/healthcare-life-sciences/vaccine-administration-management/VAM-domain-separation.md)|Basic|
|Manufacturing Commercial Operations|[Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/manufacturing/manufacturing-commercial-operations/mco-domain-separation.md)|Standard|
|Retail Core|Basic|
|Retail Task Management|Basic|
|• [Manufacturing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/manufacturing-domain-separation.md)|[Industrial Process Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/industrial-process-manager/industrial-process-manager-overview.md)|Standard|
|[Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/operational-technology-manager.md)|Standard|
|[Operational Technology Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-vulnerability-response/oper-tech-vulnerability-response-landing-page.md)|Standard|
|[Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager/operational-technology-manager.md)|Standard|
|[Telecommunications, Media, and Technology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/telecom-media-tech-landing.md)|[Account Lifecycle Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-domain-separation.md)|Basic|
|[Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/proactive-service-exp-workflows/domain-separation-cspm.md)|Basic|
|[Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spmc.md)|Basic \(Inherited from [Domain separation in the Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-ai-experiences/domain-separation-in-the-now-assist-admin-console.md)\).|
|[Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/proactive-service-exp-workflows/product-support-for-technology/domain-separation-assurance-workflows.md)|Standard|
|[Service Bridge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-exchange/service-bridge-v2-domain-separation.md)|Standard|
|[Technology Product Support Case application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/proactive-service-exp-workflows/product-support-for-technology/tech-product-support-case-app.md)|Basic \(Inherited from Customer Service Management\).|
|[Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-network-inventory/telecommunications-network-inventory/domain-seperation-telecommunication-network-inventory.md)|Basic|
|IT Asset Management|Cloud Insights|No support|
|Hardware Asset Management|Enhanced|
|Software Asset Management|Enhanced|
|Enterprise Asset Management|Standard|
|Strategic Portfolio Management|Agile Development|Basic\*|
|Alignment Planner Workspace|Basic|
|[Application Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/enterprise-architecture/domain-separation-app-portfolio-mgt.md)|Basic|
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
|Cloud Provisioning and Governance Terraform|Basic|
|Cloud Operation Workspace|Basic|
|Cloud Discovery|Standard|
|IT Service Management|Benchmarks|No support|
|Change Management|Basic|
|Coaching|Basic|
|Continual Improvement Management|Basic|
|Contract Management|No support|
||Basic|
|Expense Line|No support|
|Incident Communications Management|Standard|
|Incident Management|Standard|
|[Facilities Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-management-for-the-enterprise/service-management-legacy/domain-separation-facilities-service-mgt.md)|Standard|
|Incident Management|Standard|
|On-Call Scheduling|Standard|
|Asset Management|Basic|
|Problem Management|Standard|
|Procurement|Standard\*|
|Product Catalog|Standard|
|Request Management|Standard|
|Service Catalog|Standard|
|Service Level Management|Basic|
|[Service Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/service-portfolio-management/SPM2-landing-page.md)|Basic\*|
|Site Reliability Operations|Basic\*|
|Task outage|Basic|
||No support|
|Walk-up Experience|Basic|
|[Mobile Configuration and Navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/mobile/mobile-platform/mobile-config-navigation.md)|[Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/mobile/mobile-platform/mobile-domain-separation.md)|Basic|
|Now Intelligence|Dashboards|Basic|
|Performance Analytics|Enhanced|
|Process Optimization|Basic|
|Reporting|Basic|
|User Experience Analytics|Basic|
|[The ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/now-platform/servicenow-ai-platform/now-platform-landing.md)|Administration| |
|[Domain separation and Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/agent-chat/ci-agent-chat-reference.md)|Standard|
|ServiceNow AI Platform Capabilities| |
|User Interface| |
|Advanced Work Assignment|Standard|
|AI Search|Searches respect domain restrictions from indexed records|
|App Engine Studio|No support|
|Application Management|No support|
|Assessments|Standard|
|Automated Test Framework|Standard\*|
|ServiceNow Voice| |
|[Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/code-signing-landing.md)|Basic support|
|Contextual Search|Standard|
|Configuration Management \(CMDB\)|Standard|
|Content Management System|No support|
|[Credentials and Connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/connections-and-credentials/domain-separation-credentials_conn.md)|Standard|
|Data Certification|Basic\*|
|[Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/data-classification/domain-separation-data-classification.md)|Enhanced|
|Data Privacy|No support|
|Data Management|Basic\*|
|Delegated Development|No support|
|Dependency Views|Basic|
|Document Services|No support|
|Dynamic Translation|Basic|
|[Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/edge-encryption/edge-encryption-domain-separation.md)|Basic support|
|External Content Connectors|No support\*|
|[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/field-encryption.md)|No support|
|[Field Encryption Enterprise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/now-platform-encryption.md)|No support|
|[Cloud Encryption with Key Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/cloud-encryption/dare-overview.md)|Basic support|
|Field Normalization|No support|
|[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/flow-designer-domain-separation.md)|Standard\*|
|Guided Setup|No support|
||Standard\*|
|Integrations with third-party applications and data sources|Basic+Standard|
|Knowledge Management|Standard|
|Hermes Messaging Service|No support|
|Managed Documents|No support|
|MetricBase|Basic|
|Natural Language Understanding|Basic+Standard|
|Notifications|Standard|
|[ODBC Driver](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/web-services/domain-separation-odbc-driver.md)|Basic\*|
|Orchestration|Standard\*|
|Password Reset|Standard|
|[Platform Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/domain-sep-landing-page.md)|Domain separation landing page|
|Data Privacy|No support|
|Predictive Intelligence|Standard|
|Proactive Triggers|Basic|
|[Process Automation Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/process-automation-designer-domain-separation.md)|Basic|
|Remote Tables|No support|
|Schedules|Basic|
|[Script debugger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/domain-separation-script-debugging.md)|Basic|
|Search Suggestions|No support|
|Service Portal|No support|
|Service Graph Connectors|No support|
|[Domain separation and Sidebar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/sidebar/sidebar-domain-separation.md)|Standard|
|State Flows|No support|
|Subscription Management|Basic\*|
|Survey Management|Basic\*|
|Task Intelligence|No support|
||Basic\*|
|UI Builder|Standard|
|[Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/virtual-agent/domain-separation-virtual-agent.md)|Basic|
|Visual Task Boards|Basic|
|[Web Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/web-services/domain-separation-web-services.md)|Standard\*|
|[Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/legacy-workflow/c_WorkflowsAndDomainSeparation.md)|Standard\*|
|Workspace|Standard|
||Configuration Compliance|Standard|
|Configuration Data Management|Basic|
|IBM QRadar Offense Ingestion|Basic|
|Microsoft Graph Security API alert ingestion integration|Basic|
|Security Incident Response|Standard|
|Threat Intelligence|Standard|
|Vulnerability Response|Standard|
|[Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-management-for-the-enterprise/service-management-legacy/c_ServiceManagement.md)|[Facilities Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-management-for-the-enterprise/service-management-legacy/domain-separation-facilities-service-mgt.md)|Standard|
|[Planned Maintenance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/service-management-for-the-enterprise/planned-maintenance-family/domain-separation-planned-maintenance.md)|Standard\*|
|Proactive Triggers|Basic|
|NOW Code Editor|No support|
|Workforce Optimization for ITSM|Basic|
|Vendor Management Workspace|Basic|

**Parent Topic:**[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-security/domain-sep-landing-page.md)

