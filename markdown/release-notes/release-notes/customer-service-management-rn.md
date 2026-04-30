---
title: Case management for CSM release notes
description: The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Case management for CSM release notes

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Yokohama release.

## Case management for CSM highlights for the Yokohama release

-   Create cases for invoice-related services such as invoice disputes or requested corrections with the Case management for Invoice Operations application.
-   Use process mining to mine the configured base system project to investigate the causes of long resolution times.

See [Case management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-case-management&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Case Management for Invoice Operations](https://www.servicenow.com/docs/access?context=csm-invoice-operations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the Case Management for Invoice Operations application \(com.sn\_csm\_invoice\) to create cases for multiple invoices or for specific invoice lines. Agents can use these cases to process invoice-related services such as invoice disputes or requested corrections.

-   **[Process mining](https://www.servicenow.com/docs/access?context=process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Use the following features to find process improvement opportunities:

    -   Use work notes analysis to learn the operational reasons behind activity transitions. This feature is Now LLM based.
    -   Mine the configured base system project to investigate the causes and get a clear view of the long resolution times and delays.
-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


## Changed in this release

-   **[Process mining](https://www.servicenow.com/docs/access?context=process-config-builder&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Use the process mining enhancements to improve processes as needed:

    -   Removed the viewer role from all records in the Process Mining Content Pack for Customer Service Management \(CSM\).
    -   Set process configurations as read-only templates, deletable only by a process mining administrator. You can enable customers to copy the template or import specific parts into their custom configuration.
-   **[Case lines and workflows](https://www.servicenow.com/docs/access?context=case-line-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The Case Line table \(sn\_case\_line\) includes the **Install base** and **Asset** reference fields. These fields display information based on the selected account and product.


## Deprecations

Starting with the Yokohama release, Customer Service CTI Demo Data is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. ServiceNow Voice with Amazon Connect provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Customer Service Management is available with activation of the Customer Service plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist for CSM](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the ServiceNow® Now Assist for CSM application to summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes.

-   **[Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to connect, engage, and collaborate by using the ServiceNow® Communities application. Customer Service agents can create cases from the community discussion threads and resolve cases by using the community content.

-   **[Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Use ServiceNow® Continual Improvement Management to request improvement opportunities. You can implement phases and tasks to meet performance goals, track progress, and measure success. You can also view, create, and associate improvement initiatives from within the Process Mining application.

-   **[Integrating with Customer Project Management](https://www.servicenow.com/docs/access?context=csm-ppm-integration&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The Customer Project Management plugin \(com.snc.csm\_ppm\) enables you to create projects for a customer account by using the ServiceNow® Project Portfolio Suite with Financials application. It also gives end users visibility into their projects from the Customer Service Portal. This plugin requires the Project Portfolio Suite with Financials plugin \(com.snc.financial\_planning\_pmo\).

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Customer Service Management provides an integration with ServiceNow® IT Operations Management Event Management. This integration enables you to create cases proactively from alerts either manually or through automation. Customer service agents can track the accounts and the corresponding install base items that are affected by the alert. Agents can also track the operational status of an account's install base to better correlate customer issues and provide faster responses.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    Customer Service Management includes an integration with the ServiceNow® Field Service Management application. With this integration, you and your customers can perform the following tasks:

    -   Field service technicians can view customer account and contact information on work orders and work order tasks in the Field Service Management application.
    -   Customer service agents can create work orders from cases in the Customer Service Management application.
    -   Customers and consumers can view the case-related work orders from the Customer Service Portal and Consumer Service Portal.
-   **[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-components&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Workflow Studio components enable you to invoke flows or subflows that are designed as part of a workflow and to find out the output or execution status of the flows or subflows.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to search for shared information by using the ServiceNow® Knowledge Management application. Customer service agents can resolve cases with the knowledge content.

-   **[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Customer Service Management provides an integration with the ServiceNow® Playbooks application. This integration provides the ability to configure processes such as playbooks.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    ServiceNow® Process Mining helps analysts and process owners analyze the effectiveness of their business processes. Create automated business process flows from your data so that you can monitor and more quickly discover inefficiencies in your processes.

-   **[IT Service Management applications](https://www.servicenow.com/docs/access?context=integrating-with-it-service-management&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Customer Service Management includes integrations with the following ServiceNow® Service Management applications: [Incident Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-incident&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Problem Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-problem&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Change Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-change&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), and [Request Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-request&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US). With these integrations, you can create incident, problem, change, and request records from customer service cases. Customers can also submit requests from the Customer Service Portal.

-   **[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **[Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=configurable-wfo-cs&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Manage and maintain the productivity of your workforce from a single application using ServiceNow® Workforce Optimization for Customer Service. With this application, you can help to route work to members of your team, manage your team's skills and schedules, and monitor their performance.

-   **[Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace is a customer service-specific implementation that provides agents with the tools that they need to respond to customers and to resolve cases.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

