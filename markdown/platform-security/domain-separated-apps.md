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
|App development and low-code|App Engine Studio|No support|
|Automation Center|Basic|
|Robotic Process Automation \(RPA\) Hub|Basic|
|ServiceNow Studio|No support|
|Table Builder|Basic|
|App Engine Management Center|No support|
|Decision Builder|Standard|
|Enterprise Resource Planning Integration|No support|
|Enterprise Resource Planning Customization Mining|No support|
|Next Experience UI Builder|Basic|
|Workflow Data Fabric Hub/Zero Copy Connectors|No support|
|Customer Service Management|Communities|No support|
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
|Procurement Service Management \(PSM\)|No support|
|Safe Workplace Suite|See application site for individual application support levels|
|SharePoint Online Search Connector|Basic|
|Universal Request|Basic|
|Universal Task|Basic|
|Workforce Optimization for HR|Basic|
|Environmental, Social, and Governance Management|Environmental, Social, and Governance Management|No support\*|
|Field Service Management|Field Service Management|Basic|
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
|GRC: Metrics|Basic|
|Now Assist for TPRM|No support\*|
|Now Assist for IRM|No support\*|
|Smart Assessment Engine|Basic|
|Industry Products|
|•Financial Services|Financial Services Card Operations|Basic|
|Financial Services Deposit Operations|Basic|
|Financial Services Loan Operations|Basic|
|Financial Services Payment Operations|Basic|
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
|• Healthcare and Life Sciences|EMR Help|Basic|
|Healthcare and Life Sciences Service Management Core|Basic|
|Pre-Visit Management|Basic|
|Patient Support Services|Basic|
|Vaccine Administration Management|Basic|
|Healthcare Operations Core|Basic|
|Care Team Operations for Healthcare IT|Basic|
|Care Team Operations for Biomed|Basic|
|Care Team Operations for Facilities|Basic|
|Care Team Operations for Environmental Services|Basic|
|Manufacturing Commercial Operations|Manufacturing Commercial Operations|Basic|
|Retail Core|Basic|
|Public Sector Digital Services \(PSDS\)|Public Sector Digital Services|Basic|
|Telecommunications, Media, and Technology \(TMT\)|Customer Success Management|Basic|
|Customer Service Problem Management|Basic|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|Basic \(Inherited from Domain separation in the Now Assist Admin console\).|
|Proactive Service Experience Workflows|Standard|
|Service Bridge|Standard|
|Exploring Technology Product Support Case|Basic \(Inherited from Customer Service Management\).|
|Telecommunications Network Inventory|Basic|
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
|Domain separation and Digital Product Release|Basic|
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
|Service Catalog|Standard|
|Service Level Management|Basic|
|Service Portfolio Management|Basic\*|
|Site Reliability Operations|Basic\*|
|Task outage|Basic|
||No support|
|Walk-up Experience|Basic|
|Configure Now Assist for IT Service Management \(ITSM\)|Basic|
|Mobile Configuration and Navigation|Mobile|Basic|
|Now Intelligence|Dashboards|Basic|
|Performance Analytics|Enhanced|
|Process Optimization|Basic|
|Reporting|Basic|
|Usage Insights|Basic|
|The ServiceNow AI Platform|Advanced Work Assignment|Standard|
|Agent Chat|Standard|
|AI Search/Now Assist in AI Search|Searches respect domain restrictions from indexed records|
|App Engine Studio|No support|
|Application Management|No support|
|Assessments|Standard|
|Automated Test Framework|Standard\*|
|ServiceNow Voice|Basic|
|[Code Signing](../../encryption/concept/code-signing-landing.md)|No support|
|Contextual Search|Standard|
|Configuration Management \(CMDB\)|Standard|
|Content Management System|No support|
|[Credentials and Connections](../../../product/credentials/concept/domain-separation-credentials_conn.md)|Standard|
|Data Certification|Basic\*|
|[Data Classification](../../security/concept/domain-separation-data-classification.md)|Enhanced|
|Data Privacy|No support|
|Data Management|Basic\*|
|Delegated Development|No support|
|Dependency Views|Basic|
|Document Services|No support|
|Dynamic Translation|Basic|
|[Edge Encryption](../../edge-encryption/concept/edge-encryption-domain-separation.md)|Basic support|
|External Content Connectors|No support\*|
|[Field Encryption](../../encryption/concept/field-encryption.md)|No support|
|[Encryption](../../security/concept/encryption-landing.md)|No support|
|[Cloud Encryption with Key Management](../../encryption-dare/concept/dare-overview.md)|Basic support|
|Field Normalization|No support|
|Flow Designer|Standard\*|
|Guided Setup|No support|
|Domain separation and Integration Hub|Standard\*|
|Integrations with third-party applications and data sources|Basic+Standard|
|Knowledge Management|Standard|
|Hermes Messaging Service|Basic|
|Managed Documents|No support|
|MetricBase|Basic|
|Natural Language Understanding|Basic+Standard|
|Notifications|Standard|
|ODBC Driver|Basic\*|
|Orchestration|Standard\*|
|Password Reset|Standard|
|[Platform Security](domain-sep-landing-page.md)|Domain separation landing page|
|Data Privacy|No support|
|Predictive Intelligence|Standard|
|Proactive Triggers|Basic|
|Process Automation Designer|Basic|
|Remote Tables|No support|
|Schedules|Basic|
|Script debugger|Basic|
|Search Suggestions|No support|
|Service Portal|No support|
|Service Graph Connectors|No support|
|Domain separation and Sidebar|Standard|
|State Flows|No support|
|Subscription Management|Basic\*|
|Survey Management|Basic\*|
|Task Intelligence|No support|
|Domain separation and Time Card|Basic\*|
|UI Builder|Standard|
|Virtual Agent|Basic|
|Visual Task Boards|Basic|
|Web Services|Standard\*|
|Workflow|Standard\*|
|Workspace|Standard|
|Platform Fundamentals|Impact|No support|
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
|Domain separation and Subscription Management|Basic\*|
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
|Security Operations|Subscription ManagementConfiguration Compliance|Standard|
|IBM QRadar Offense Ingestion|Basic|
|Microsoft Graph Security API alert ingestion integration|Basic|
|Security Incident Response|Standard|
|Threat Intelligence|Standard|
|Threat Intelligence Security Center|Standard|
|Vulnerability Response|Standard|
|Service Management|Facilities Service Management|Standard|
|Planned Maintenance|Standard\*|
|Structured Problem Analysis|No support|
|Workforce Optimization for ITSM|Basic|
|Vendor Management Workspace|Basic|
|Proactive Triggers|Basic|
|Employee Service Management|SharePoint Online Search Connector|Basic|
|Workforce Optimization for ITSM|Basic|
|Application Portfolio Management|Application Portfolio Management|Basic|
|Domain separation and Conversational Analytics|Basic|
|Sales Customer Relationship Management|Advanced Approval for Sales Management|Enhanced|

**Parent Topic:**[Domain separation for service providers](domain-sep-landing-page.md)

