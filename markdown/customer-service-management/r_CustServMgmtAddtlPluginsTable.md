---
title: Additional plugins for Customer Service Management
description: After Customer Service Management is activated, you can activate additional plugins that provide demo data and enable various features.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Getting started with Customer Service Management, Set up your environment, Configure, Customer Service Management]
---

# Additional plugins for Customer Service Management

After Customer Service Management is activated, you can activate additional plugins that provide demo data and enable various features.

You must have the admin role to activate these additional plugins. For details, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_wp2_h15_2v"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agent Schedule\[com.snc.agent\_schedule\]

</td><td>

Enables customer service agents and field service technicians to see work schedules and assignments and also add personal events such as meetings or appointments.

</td></tr><tr><td>

Case Assignment Workbench Demo\[com.snc.case\_assignment\_workbench\_demo\]

</td><td>

Provides demo data, such as sample cases and users, so that the Assignment Workbench product features can be demonstrated on a non-production instance.

</td></tr><tr><td>

Case Digests\[com.sn\_csm\_case\_digest\]

</td><td>

Enable you to send case status updates and root cause analysis to customers and key internal stakeholders.

</td></tr><tr><td>

Consumer Service Portal\[com.glide.service-portal.consumer-portal\]

</td><td>

This plugin enables the Consumer Service Portal, a web-based portal based on the Service Portal application that you can use to provide information and support to consumers.

</td></tr><tr><td>

CSM Configurable Workspace\[sn\_csm\_wrkspc\]

</td><td>

Enables CSM Configurable Workspace, the UI Builder version of the configurable service desk application, that provides agents with an integrated and intuitive user experience.

</td></tr><tr><td>

Customer data models for B2B2C \[com.sn\_csm\_b2b\_consumers\]

</td><td>

Enables business-to-business \(B2B\) consumers to raise a case and track the services they’re subscribed to. In a B2B model, consumers represent individuals who can be customers or employees of your customer.**Note:** You must activate the Customer Service Install Base Management \[com.snc.install\_base\] plugin before installing Customer data models for business-to-business-to-consumer \(B2B2C\) \[com.sn\_csm\_b2b\_consumers\] plugin.

</td></tr><tr><td>

CSM Contributor User\[com.snc.csm\_contributor\_user\]

</td><td>

Enable contributors to report and collaborate on cases created for customers, service organizations, or themselves.**Note:** This plugin is moved to the App Store beginning with Australia release.

</td></tr><tr><td>

CSM Data Classification\[sn\_csm\_dataprivacy\]

</td><td>

Package the CSM Data Privacy templates in a new store application called CSM Data Classification. The CSM Data Classification plugin depends on the base Customer Service \[com.sn\_customerservice\] plugin and Data Privacy \(com.glide.data\_privacy\) platform plugin.

</td></tr><tr><td>

CSM Extension for Proxy Contacts\[com.snc.csm\_proxy\_contacts\]

</td><td>

Enable users who are internal to an organization to be the proxy case contact on behalf of customers.

</td></tr><tr><td>

CTI Softphone\[com.snc.cti\]

</td><td>

This plugin is a demo application that enables Twilio integration using the Notify application and OpenFrame to provide soft phone functions and call center capabilities. The application includes the capabilities to make, receive, transfer, hold, and mute calls. The Customer Service Management and Incident Management applications provide Computer Telephony Integration \(CTI\) demo workflows. Activate the respective applications to run the workflows.If the related plugins aren’t already active, the CTI Softphone plugin activates them:

-   Resource Matching Engine \(com.snc.matching\_rule\): Provides a tool for rule-based task-to-resource matching.
-   Notify \(com.snc.notify\): Provides platform features for workflow-driven voice calls, conference calls, and SMS messages.
-   Notify-Twilio Driver \(com.snc.notify.twilio\): Provides Notify support for the Twilio product. Requires a separate contract with Twilio for SMS/Voice capabilities.
-   OpenFrame \(com.sn\_openframe\): Provides an interface that can be used to integrate external communication systems with the ServiceNow AI Platform.

</td></tr><tr><td>

Customer Central\[com.sn\_csm\_customer\_central\]

</td><td>

Enables customer service agents to access all customer information and activity in a single, centralized view on Agent Workspace.

</td></tr><tr><td>

Customer Communities\[com.sn\_customer\_communities\]

</td><td>

Enable you to connect, engage, and collaborate with employees, customers, partners, and prospects. Available to customers who are licensed for Customer Service Management.

</td></tr><tr><td>

Customer Project Management\[com.snc.csm\_ppm\]

</td><td>

Provides the ability to create and manage projects for a customer account and gives end users visibility into their projects via the portal. This plugin requires the Customer Service plugin and the PPM Standard plugin.

</td></tr><tr><td>

Customer Service Case Action Status\[com.snc.csm\_action\_status\]

</td><td>

Provides a Customer Service-specific application of the Action Status Automation feature. Use this plugin to display and track blocking tasks for customer service cases.

</td></tr><tr><td>

Customer Service Case Types\[com.snc.csm\_case\_types\]

</td><td>

Enables customers to manage complex case processes by defining new case types. A case type represents an individual business process and is a collection of diverse inputs and tasks that an agent performs to resolve customer requests.

</td></tr><tr><td>

Customer Service CTI Demo Data\[com.snc.customerservice\_cti\_demo\]

</td><td>

Provides demo data for the CTI Softphone application.**Note:** Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It’s hidden and no longer activated on new instances but it continues to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Customer Service Document Template\[com.sn\_csm\_doc\_template\]

</td><td>

Enables you to configure the fields from a table record that are included in an output document.

</td></tr><tr><td>

Customer Household Data Model\[com.snc.household\]

</td><td>

Enables managing customer service for consumers belonging to the same household. Provides the ability to define the members of a household and relationships between them.

</td></tr><tr><td>

Customer Service Install Base Management \[com.snc.install\_base\]

</td><td>

Enables customers to capture the current state of a customer's install base and establish the relationship to any downstream entities that might impact their functioning.

</td></tr><tr><td>

Customer Service Management Demo Data\[com.snc.customerservice.demo\]

</td><td>

Provides demo data for the Customer Service Management application.

</td></tr><tr><td>

Customer Service Mobile\[com.sn\_csm\_mobile\]

</td><td>

Enables the mobile user interface for Customer Service Management.

</td></tr><tr><td>

Customer Service NLU Model for Virtual Agent Conversations\[com.sn\_csm.nlu\]

</td><td>

This plugin contains Natural Language Understanding \(NLU\) models used in the VA topics for Customer Service related use cases.

</td></tr><tr><td>

Customer Service Virtual Agent Conversations\[com.sn\_csm.virtualagent\]

</td><td>

This plugin contains prebuilt template conversation topics for CSM-related use cases. They’re intended to be copied and configured.

</td></tr><tr><td>

Customer Service with Field Service Management\[com.snc.csm\_fsm\_integration\]

</td><td>

This plugin provides an integration between the Customer Service Management and Field Service Management applications. Customers and consumers can view case-related work orders from the Customer Service and Consumer Service Portals. In the Field Service Management application, you can view account and contact information on work orders and work order tasks.

</td></tr><tr><td>

Customer Service with Request Management\[com.sn\_cs\_sm\_request\]

</td><td>

Provides an integration between Customer Service Management and the Request Management application. Enable you to create request records from a Customer Service case.

</td></tr><tr><td>

Customer Service with Service Management\[com.sn\_cs\_sm\]

</td><td>

Provides an integration between Customer Service Management and the Incident, Problem, and Change Management applications. Enable you to create incident, problem, and change records from a Customer Service case.

</td></tr><tr><td>

Customer Service with Service Portfolio Management\[sn\_csm\_spm\]

</td><td>

Provides an integration between the Customer Service Management and the Service Portfolio Management \(SPM\) application. This integration gives customer service managers, customer service agents, and service owners visibility into sold products and their service offerings.

</td></tr><tr><td>

Incident Assignment Workbench Demo\(com.snc.incident\_assignment\_workbench\_demo\)

</td><td>

Intelligent agent recommendation through dynamic matching rules/criteria.

</td></tr><tr><td>

Guided Decisions\[com.snc.guided\_decisions\]

</td><td>

Enables the framework and execution engine for creating guided decisions.

</td></tr><tr><td>

Guided Decisions - Guidance\[com.snc.guided\_decisions\_guidance\]

</td><td>

Enables the framework for creating guidance for guided decisions.

</td></tr><tr><td>

Guided Decisions for Playbook in Workspace\[com.snc.guided\_decisions\_playbook\_experience\]

</td><td>

Enables activity types, definitions, and UI components for the display of guided decisions in a playbook on Workspace.

</td></tr><tr><td>

Knowledge Product Entitlements\[com.snc.kb\_product\_entitlements\]

</td><td>

This plugin enables customer service administrators to restrict customer access to designated knowledge bases and knowledge articles on the customer self-service portal. This plugin adds the Knowledge Product Entitlements menu to the application navigator.

</td></tr><tr><td>

Major Issue Management\[com.sn\_majorissue\_mgt\]

</td><td>

A set of capabilities used to manage customer-facing communications and resolution processes for common issues.

</td></tr><tr><td>

Outsourced Customer Service\(com.snc.csm\_ocs\)

</td><td>

Enables organizations to outsource customer service to external service providers.**Note:** This plugin is moved to the App Store beginning with Australia release.

</td></tr><tr><td>

Performance Analytics - Content Pack - Customer Service\[com.snc.pa.customer\_service\]

</td><td>

Performance Analytics content pack that includes Customer Service base system KPIs.

</td></tr><tr><td>

Performance Analytics - Content Pack - Customer Service Management - Advanced\[com.snc.pa.customer\_service\_advanced\]

</td><td>

Updates the Customer Service dashboard and incorporates indicators for the following plugins:-   Major Issue Management
-   Customer Service Case Action Status
-   Customer Service with Request Management
-   Customer Service with Service Management
-   Agent Chat
-   Advanced Work Assignment for CSM
-   Performance Analytics - Content Pack - Advanced Work Assignment

Activate these plugins to view the related indicators. Without these plugins, indicators might not display correctly.

</td></tr><tr><td>

Performance Analytics - Context Sensitive Analytics for Customer Service\[com.snc.pa.cs.context\_sensitive\_analytics\]

</td><td>

This plugin enables you to open context-sensitive dashboards in customer service forms based on UI actions.**Note:** You can activate Performance Analytics solutions on instances that don’t have Performance Analytics to evaluate the functionality. However, to collect scores for indicators you must license Performance Analytics.

</td></tr><tr><td>

Performance Analytics Premium for Customer Service\[com.snc.pa.premium.cs\]

</td><td>

This plugin extends the capabilities of baseline Performance Analytics.

</td></tr><tr><td>

Playbooks for Customer Service Management\[sn\_csm\_playbook\]

</td><td>

Provides step-by-step guidance for customer service cases.

</td></tr><tr><td>

Predictive Intelligence for Customer Service Management \[com.snc.csm\_ml\]

</td><td>

Enables customers to leverage machine learning algorithms for searching related cases in Customer Service Management. Activation of this plugin on production instances might require a separate license. Contact ServiceNow for details.If they aren’t already active, the Predictive Intelligence for Customer Service Management plugin activates these related plugins:

 -   Customer Service plugin \(com.sn\_customerservice\)
-   Predictive Intelligence for Contextual Search plugin \(com.snc.contextual\_search\_ml\)
-   Email Notification Script for Contextual Search Results plugin \(com.snc.adv\_cxs\_results\_email\_script\)

</td></tr><tr><td>

Self-Service Analytics for Customer Service\[com.snc.pa.self\_service\_analytics\_csm\]

</td><td>

Tracks case reduction \(deflection\) metrics and self-service KPIs using performance analytics dashboards. Activation of this plugin on production instances might require a separate Performance Analytics license. Contact ServiceNow for details.If they aren’t already active, the Self-Service Analytics for Customer Service plugin activates these related plugins:

 -   Customer Service plugin \(com.sn\_customerservice\)
-   Self-Service Analytics Core plugin \(com.snc.self\_service\_analytics\_core\)
-   Self-Service Analytics PA plugin \(com.snc.pa.self\_service\_analytics\)

</td></tr><tr><td>

Self Service Password Reset\[com.snc.password\_reset\]

</td><td>

This plugin enables locally authenticated users to request a temporary password if they forget their current one. Customer contacts can request a new password from the customer self-service portal.If it isn’t already active, the Self Service Password Reset plugin activates the Password Reset plugin \(com.glideapp.password\_reset\).

</td></tr><tr><td>

Special Handling Notes Demo Data\[com.snc.shn\_demo\]

</td><td>

Provides demo data for the Special Handling Notes application.

</td></tr><tr><td>

Targeted Communications\[com.sn\_publications\]

</td><td>

Provides a tool for publishing and distributing content and articles to both internal and external customers.

</td></tr><tr><td>

Targeted Communications Demo Data\[com.snc.publications\_demo\]

</td><td>

Provides demo data for the Targeted Communications application.

</td></tr><tr><td>

Time Recording for Customer Service\[com.snc.csm\_time\_recording\]

</td><td>

Extends the functionality of the Time Card Management and Cost Management applications to Customer Service Management.

</td></tr><tr><td>

Walk-Up for CSM\[com.snc.walkup\_for\_csm\]

</td><td>

Walk-up experience for Customer Service enables in-store support to assist onsite check-ins, managing queues, and customer interactions.

</td></tr><tr><td>

UI Components for Customer Portals \[sn\_ciwf\_ui\_cmpnt\]

</td><td>

This plugin enables you to configure the behavior, content, and layout of a portal using a Configurable Portal Widgets.

</td></tr></tbody>
</table>**Parent Topic:**[Customer Service Management](../concept/c_CustomerServiceManagement.md)

