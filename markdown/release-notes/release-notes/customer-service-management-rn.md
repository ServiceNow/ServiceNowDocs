---
title: Case management for CSM release notes
description: The ServiceNow Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-10-17"
reading_time_minutes: 6
---

# Case management for CSM release notes

The ServiceNow® Case management for CSM application enables customer service organizations and support teams to collaborate on customer problems proactively to resolve issues. Case management for CSM was enhanced and updated in the Xanadu release.

## Case management for CSM highlights for the Xanadu release

-   Create pages and page variants that contain horizontal or vertical playbooks by using playbook templates.
-   Use playbook record pages in CSM Configurable Workspace to guide users through the stages and activities of a playbook and resolve cases.
-   Identify common inefficiencies in customer operations by using process mining definitions.

See [Case management for Customer Service Management](https://www.servicenow.com/docs/access?context=csm-case-management&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) for more information.

## Important information for upgrading Case management for CSM to Xanadu

The customer service manager role \[sn\_customerservice\_manager\] includes the approver user role \[approver\_user\]. The approver user role replaces the approval admin role \[approval\_admin\]. Users with the customer service manager role can approve the approval requests that are assigned to them.

## New in the Xanadu release

-   **[Playbooks](https://www.servicenow.com/docs/access?context=customer-service-case-playbooks&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Use updated playbook templates in UI Builder that incorporate generative AI feature parity and Agent Experience modernization features such as the modeless dialogs, activity stream, lookup cards, and related items.

-   **[Order Operations Case Management](https://www.servicenow.com/docs/access?context=csm-case-mgmt-order-ops&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Use the Order Operations Case Management application \(com.sn\_order\_case\) to create order cases that reference multiple line items, including orders and order lines. Agents can use these cases to process order-related services such as order changes, inquiries, and disputes.

-   **[Case lines and workflows](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Use the Case lines and workflows application \(com.sn\_case\_line\) to reference multiple line items on a case record, including orders or order lines, invoices or invoices lines, contracts, and sold products.

-   **[Quick start tests for Customer Service Management](https://www.servicenow.com/docs/access?context=quick-start-tests-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that Customer Service Management works as expected. If you customized Customer Service Management, copy the quick start tests and configure them for your customizations.


## Changed in this release

-   **[Case type selector configuration](https://www.servicenow.com/docs/access?context=csm-case-type-select-modals-product-service&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Configure the Product Service select version of the case type selector to hide the product filter.

-   **[Roles included with the customer service manager role](https://www.servicenow.com/docs/access?context=r_RolesInstalledWithCustomerService&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The customer service manager role \[sn\_customerservice\_manager\] includes the approver user role \[approver\_user\]. For upgrade customers, the approver user role replaces the approval admin role \[approval\_admin\]. Users with the customer service manager role can approve the approval requests that are assigned to them.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=improve-opportunities&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    Added different variants of the two enhanced types of base system opportunities that you can use on a project to identify and address common inefficiencies in customer operations:

    -   Rule-based finding definitions: Execute one or more finding rule chains in sequence according to the definitions. The records that match the logic of these specifications are classified as a match for improvement opportunities.
    -   Automated finding definitions: Show improvement opportunities by using the default patterns that are already available for selection.

## Deprecations

Starting with the Xanadu release, CSM Agent Workspace is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. [CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=csm-workspaces-configure&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) provides the latest experience for this functionality.

## Activation information

Customer Service Management is a ServiceNow AI Platform feature that is available with activation of the Customer Service Management plugin \(com.sn\_customerservice\). For details, see [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

Additional Customer Service Management features are available with the activation of other plugins. For details, see [Additional plugins for Customer Service Management](https://www.servicenow.com/docs/access?context=r_CustServMgmtAddtlPluginsTable&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

## Browser requirements

ServiceNow workspaces don’t support mobile devices, Internet Explorer, or Microsoft Edge. Instead, use Microsoft Edge - Chromium or one of the other supported browsers listed in [Browser support](https://www.servicenow.com/docs/access?context=browser-support&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

## Accessibility information

The following templates were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

-   [Case playbook: horizontal stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [Case playbook: vertical stages template](https://www.servicenow.com/docs/access?context=csm-playbook-templates&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)

## Related ServiceNow applications and features

-   **[Now Assist for CSM](../analytics-intelligence-reporting/now-assist-rn.md)**

    Use the ServiceNow® Now Assist for CSM application to summarize customer chat conversations on interactions, summarize case details, and generate case resolution notes.

-   **[Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to connect, engage, and collaborate by using the ServiceNow® Communities application. Customer Service agents can create cases from the community discussion threads and resolve cases by using the community content.

-   **[Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    Use ServiceNow® Continual Improvement Management to request improvement opportunities. You can implement phases and tasks to meet performance goals, track progress, and measure success. You can also view, create, and associate improvement initiatives from within the Process Mining application.

-   **[Integrating with Customer Project Management](https://www.servicenow.com/docs/access?context=csm-ppm-integration&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The Customer Project Management plugin \(com.snc.csm\_ppm\) enables you to create projects for a customer account by using the ServiceNow® Project Portfolio Suite with Financials application. It also gives end users visibility into their projects from the Customer Service Portal. This plugin requires the Project Portfolio Suite with Financials plugin \(com.snc.financial\_planning\_pmo\).

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Customer Service Management provides an integration with ServiceNow® IT Operations Management Event Management. This integration enables you to create cases proactively from alerts either manually or through automation. Customer service agents can track the accounts and the corresponding install base items that are affected by the alert. Agents can also track the operational status of an account's install base to better correlate customer issues and provide faster responses.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Customer Service Management includes an integration with the ServiceNow® Field Service Management application. With this integration, you and your customers can perform the following tasks:

    -   Field service technicians can view customer account and contact information on work orders and work order tasks in the Field Service Management application.
    -   Customer service agents can create work orders from cases in the Customer Service Management application.
    -   Customers and consumers can view the case-related work orders from the Customer Service Portal and Consumer Service Portal.
-   **[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-components&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Workflow Studio components enable you to invoke flows or subflows that are designed as part of a workflow and to find out the output or execution status of the flows or subflows.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to search for shared information by using the ServiceNow® Knowledge Management application. Customer service agents can resolve cases with the knowledge content.

-   **[Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Customer Service Management provides an integration with the ServiceNow® Playbooks application. This integration provides the ability to configure processes such as playbooks.

-   **[Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    ServiceNow® Process Mining helps analysts and process owners analyze the effectiveness of their business processes. Create automated business process flows from your data so that you can monitor and more quickly discover inefficiencies in your processes.

-   **[IT Service Management applications](https://www.servicenow.com/docs/access?context=integrating-with-it-service-management&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Customer Service Management includes integrations with the following ServiceNow® Service Management applications: [Incident Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-incident&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US), [Problem Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-problem&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US), [Change Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-change&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US), and [Request Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-request&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US). With these integrations, you can create incident, problem, change, and request records from customer service cases. Customers can also submit requests from the Customer Service Portal.

-   **[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **[Workforce Optimization for Customer Service](https://www.servicenow.com/docs/access?context=configurable-wfo-cs&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Manage and maintain the productivity of your workforce from a single application using ServiceNow® Workforce Optimization for Customer Service. With this application, you can help to efficiently route work to members of your team, manage your team's skills and schedules, and monitor their performance.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace is a customer service-specific implementation that provides agents with the tools that they need to respond to customers and to resolve cases.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

