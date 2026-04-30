---
title: Procurement Case Management
description: With the Procurement Case Management application, you can enable your employees to submit procurement cases and access your organization's knowledge base. You can also enable your procurement teams to automate their fulfillment processes so that they can manage and monitor the progress of their tasks.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Procurement Case Management

With the Procurement Case Management application, you can enable your employees to submit procurement cases and access your organization's knowledge base. You can also enable your procurement teams to automate their fulfillment processes so that they can manage and monitor the progress of their tasks.

The Procurement Case Management \(PCM\) application enables you to manage the complete life cycle of the procurement process.

By using the PCM application, your organization gets the following benefits:

-   Procurement process optimization for task routing and tracking the progress of your tasks.
-   Knowledge article publish and performance workflows.
-   Visibility into the processes, progress, and overall efficiency of the procurement process.
-   Integration with IT Asset Management, Software Asset Management, and Contract Management.

## Installed plugins

Install Procurement Case Management from the ServiceNow Store.

The Procurement Case Management \(sn\_spend\_psd\) application installs the following dependent plugins:

-   Common Service Delivery \(sn\_spend\_sdc\)

-   Source-to-Pay Workspace \(sn\_spend\_workspace\)


## Required roles

You can configure the following roles and tasks:

-   sn\_spend\_psd.psd\_admin: Configure and make changes to the system properties, such as creating request types and categories.

    **Note:** An application-specific admin role enables a user to manage application-level configurations, roles, and access controls. Your system-level admin on the production instance must grant the application-specific admin role to the appropriate users, and then remove the application-specific admin role from all users with the system-level admin role to help prevent system-level admins from viewing sensitive application data via forms, lists, and the UI. For more information, see [Application administration](https://www.servicenow.com/docs/access?context=application-administration&version=australia&pubname=australia-application-development&ft:locale=en-US).

-   sn\_spend\_psd.manager: View, create, and update procurement cases and tasks.
-   sn\_spend\_psd.agent: Manage the workflows for fulfilling requests and knowledge articles.
-   sn\_spend\_psd.procurement\_task\_owner: Access and complete task assignments to fulfill the requests.
-   sn\_spend\_psd.requestor: Create procurement cases.

-   **[Work prioritization](../reference/work-prioritization.md)**  
Work prioritization automatically assigns a priority level to purchase requisitions, sourcing requests, and procurement cases so that procurement specialists can work the most urgent items first.
-   **[Supplier qualification](../reference/supplier-qualification.md)**  
As a procurement specialist or Procurement Case Management \(PCM\) agent, you would want to engage with suppliers who are qualified to fulfill your organization's purchasing needs.
-   **[Process Automation Designer flows for playbook](process-automation-designer-flows-psm.md)**  
The Source-to-Pay Workspace helps you automate the entire process, right from tracking the requests, fulfillment, and to order revision flows.
-   **[Email notifications from Playbook](../reference/email-notifications-workspace.md)**  
Several email notifications are triggered from Playbook. This may be a result of your action, an assignment for you, or to keep you updated on the status of your purchases, including purchase revisions.
-   **[Email composer with quick messages and response templates in Source-to-Pay Workspace](email-composer-with-quick-messages-and-response-templates-psm.md)**  
Insert predefined content into the message body of emails that you send from the email client in Source-to-Pay Workspace.
-   **[Agent assist in Source-to-Pay Workspace](agent-assist-procurement-workspace.md)**  
Agent assist in Source-to-Pay Workspace automatically displays relevant search results based on the search text, which is defaulted with the short description of the procurement case you’re working on. You can edit the search text as required. These search results help you to work on the record.
-   **[Interaction Management in Source-to-Pay Workspace](interaction-management-in-procurement-operations-workspace.md)**  
Interactions are a centralized location for all communication channels available in Source-to-Pay Workspace. Interaction Management involves managing procurement related queries from different sources such as an email, chat, message, or SMS.
-   **[Procurement Case Management Dashboard](procurement-service-delivery-dashboard.md)**  
The Procurement Case Management Dashboard helps you to track, analyze, and manage your procurement services.

**Parent Topic:**[Explore Sourcing and Procurement Operations](exploring-spo.md)

**Related topics**  


[My purchases on Shopping Hub](my-purchases.md)

[Shopping Hub Mobile](shoppinghub-mobile.md)

[Performance Analytics for Sourcing and Procurement Operations](performance-analytics-for-spo.md)

[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

[Source-to-Pay Workspace](procurement-specialist-workspace.md)

[Spend and Savings Management](spo-spend-mgmt.md)

[Sourcing Pipeline Management](spo-sourcing-pipeline-mgmt.md)

[Understanding Punchout](punchout-overview.md)

[AI Search for Sourcing and Procurement Operations](ai-search-sourcing-procurement-operations.md)

[Procurement Case Management Dashboard](procurement-service-delivery-dashboard.md)

[Using Procurement Case Management](using-pcm.md)

[Install Sourcing and Procurement Operations](../task/activate-finance-spend-central.md)

[Application plugin installation sequence in Sourcing and Procurement Operations](../reference/application-plugin-list.md)

