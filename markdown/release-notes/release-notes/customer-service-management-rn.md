---
title: Case management for CSM release notes
description: The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
---

# Case management for CSM release notes

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Zurich release.

## Case management for CSM highlights for the Zurich release

-   Sharing task plan templates ensures that only authorized users can access, edit, or share templates based on their role and location, preventing misuse and maintaining operational integrity.
-   View the most relevant services that are available for customers when creating customer service cases.
-   View and select from the available entitlements that are associated with the customer, product, and contract information to associate multiple entitlements with customer service cases.
-   Filter the service definitions that are displayed to agents based on such criteria as the assigned role or group, or entity criteria.

See [Case management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-case-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) for more information.

## New in the Case management for CSM release

-   **[Task plan templates](https://www.servicenow.com/docs/access?context=task-plan-templates&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Create templates that define the repeatable tasks and records that need to be created for business processes. Define the tasks, set the task order, and create conditions that determine when these tasks and records are created.

-   **[Add multiple entitlements to a case](https://www.servicenow.com/docs/access?context=add-entitlement-to-case&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    View the available entitlements on a customer service case and associate the multiple entitlements to the case. Available entitlements are associated with the account or consumer, product, and contract selected on the case record.

-   **[Recommend service definitions based on case context](https://www.servicenow.com/docs/access?context=csm-service-definitions&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Recommend the most relevant services to an agent based on the record context, such as the short description or description of the interaction.

-   **[Customer Service Case Types - Enable the service selector to launch record producers](https://www.servicenow.com/docs/access?context=csm-service-definition-catalog-items&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Use the Service Portal record producers when your agents are creating cases in CSM Configurable Workspace. Agents can select the service definitions from the case type selector and launch the record producers.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   ****

    Sharing task plan templates ensures that only authorized users can access, edit, or share templates based on their role and location, preventing misuse and maintaining operational integrity. Sharing task plant template features include:

    -   Access control: Users can now provide access to task plan templates at various levels, including user, group, and service organization.
    -   Ownership Management: The Owner or an Admin can change the ownership of a Template by updating the Owner field.
    -   Global template: Task plan templates can be marked as global, making them visible to all users with read access.
    -   Form and List Layouts: Admins can view and edit form and list layouts for sharing, displaying all relevant fields.
    -   Notifications: In-app notifications are sent when access is granted, Selecting the notification opens the shared template directly.
-   **[Task plan template configurations](https://www.servicenow.com/docs/access?context=task_plan_template_configurations&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Admins can create configurations for task plan templates that pre-fill information when creating a new task plan template.


-   **[Filtering service definitions](https://www.servicenow.com/docs/access?context=csm-service-definitions&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Enable agents to filter the service definitions that are shown on the service selector in the following ways:

    -   By user, role, group, or agent
    -   By entity critera such as location, customer level, or related entities
-   **[Case lines for Case Management - Add multiple entitlements to case lines](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    View the available entitlements on a case line and associate the multiple entitlements to that case line. Available entitlements are associated with the contracts and entitlements that are purchased by the customer.

-   **[Targeted Communications](https://www.servicenow.com/docs/access?context=targeted-comm-publication-workflows&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) and [Case Digests](https://www.servicenow.com/docs/access?context=customer-service-case-digests&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US#section_ast_r2k_qfc) workflows**

    Legacy workflows for the Targeted Communications \(com.sn\_publications\) and Case Digests \(com.sn\_csm\_case\_digest\) applications have been migrated to low-code flows in Workflow Studio. The functionality of the flows remains the same.

-   **[Classifying sensitive data](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Fields in the Customer Service Management and Targeted Communications tables are mapped to the Data Privacy data classes. For more information, see the [Data privacy overview](https://www.servicenow.com/docs/access?context=dps-data-privacy-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.

-   **Deny-Unless ACLs implemented on CSM tables**

    Deny-Unless access control lists \(ACLs\) were implemented on CSM tables for non-authenticated users, such as users with public roles. With this minimum-security setting, only authenticated users can perform read, write, delete, or create actions on these tables. For more information about Deny-Unless ACLs, see the [Deny-Unless ACL](https://www.servicenow.com/docs/access?context=acl-denial-behavior&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) topic in the ServiceNow® Platform Security documentation.

-   **[Customer Service Case Types moved from family to store release](https://www.servicenow.com/docs/access?context=customer-service-case-types&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Starting with the Zurich release, the Customer Service Case Types application \(sn\_csm\_case\_types\) has moved to the ServiceNow Store. Any new enhancements to this application are delivered through the Customer Service Case Types store app.


## Deprecations

-   Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.
-   Starting with the Zurich release, the Customer Service Case Types plugin is available as a store plugin and, as such, the family version of the plugin is being prepared for future deprecation. Upon upgrading, customers will automatically move to the store version of the plugin. It will be hidden from the family plugins and no longer installed on new instances but will continue to be supported as a store plugin. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist for CSM](https://www.servicenow.com/docs/access?context=now-assist-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Use the ServiceNow® Now Assist for CSM application to summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes.

-   **[Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to connect, engage, and collaborate by using the ServiceNow® Communities application. Customer Service agents can create cases from the community discussion threads and resolve cases by using the community content.

-   **[Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-landing-page&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    Use ServiceNow® Continual Improvement Management to request improvement opportunities. You can implement phases and tasks to meet performance goals, track progress, and measure success. You can also view, create, and associate improvement initiatives from within the Process Mining application.

-   **[Integrating with Customer Project Management](https://www.servicenow.com/docs/access?context=csm-ppm-integration&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    The Customer Project Management plugin \(com.snc.csm\_ppm\) enables you to create projects for a customer account by using the ServiceNow® Project Portfolio Suite with Financials application. It also gives end users visibility into their projects from the Customer Service Portal. This plugin requires the Project Portfolio Suite with Financials plugin \(com.snc.financial\_planning\_pmo\).

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Customer Service Management provides an integration with ServiceNow® IT Operations Management Event Management. This integration enables you to create cases proactively from alerts either manually or through automation. Customer service agents can track the accounts and the corresponding install base items that are affected by the alert. Agents can also track the operational status of an account's install base to better correlate customer issues and provide faster responses.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)**

    Customer Service Management includes an integration with the ServiceNow® Field Service Management application. With this integration, you and your customers can perform the following tasks:

    -   Field service technicians can view customer account and contact information on work orders and work order tasks in the Field Service Management application.
    -   Customer service agents can create work orders from cases in the Customer Service Management application.
    -   Customers and consumers can view the case-related work orders from the Customer Service Portal and Consumer Service Portal.
-   **[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-components&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Workflow Studio components enable you to invoke flows or subflows that are designed as part of a workflow and to find out the output or execution status of the flows or subflows.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to search for shared information by using the ServiceNow® Knowledge Management application. Customer service agents can resolve cases with the knowledge content.

-   **[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Customer Service Management provides an integration with the ServiceNow® Playbooks application. This integration provides the ability to configure processes such as playbooks.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    ServiceNow® Process Mining helps analysts and process owners analyze the effectiveness of their business processes. Create automated business process flows from your data so that you can monitor and more quickly discover inefficiencies in your processes.

-   **[IT Service Management applications](https://www.servicenow.com/docs/access?context=integrating-with-it-service-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Customer Service Management includes integrations with the following ServiceNow® Service Management applications: [Incident Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-incident&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US), [Problem Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-problem&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US), [Change Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-change&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US), and [Request Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-request&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US). With these integrations, you can create incident, problem, change, and request records from customer service cases. Customers can also submit requests from the Customer Service Portal.

-   **[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **[Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=configurable-wfo-cs&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Manage and maintain the productivity of your workforce from a single application using ServiceNow® Workforce Optimization for Customer Service. With this application, you can help to route work to members of your team, manage your team's skills and schedules, and monitor their performance.

-   **[Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace is a customer service-specific implementation that provides agents with the tools that they need to respond to customers and to resolve cases.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

