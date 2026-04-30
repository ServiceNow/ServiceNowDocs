---
title: Configure case management
description: Configure the Customer Service Management features and components that agents and managers use to create and resolve cases. This process includes setting up case forms, assignment workbench configurations, service level agreements \(SLAs\), and managing major issues and escalations. Additionally, it covers the use of special handling notes, case digests, and auto-close resolved cases to streamline customer service operations.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure case management

Configure the Customer Service Management features and components that agents and managers use to create and resolve cases. This process includes setting up case forms, assignment workbench configurations, service level agreements \(SLAs\), and managing major issues and escalations. Additionally, it covers the use of special handling notes, case digests, and auto-close resolved cases to streamline customer service operations.

## Before you begin

Role required: admin

## About this task

The customer service case is the primary entity of the customer service application. An agent creates a case to identify a customer's question or issue and to track the activities related to resolving the issue. An agent also uses a case to track all communication with the customer, including the communication channels used.

Case activities include any action that is taken to resolve an issue. These actions can include phone calls or emails, knowledge base research, conversations with subject matter experts, and dispatch requests to field service agents, as well as other activities.

From the case form, an agent can store related information such as the customer's name, contact details, company, account, product and asset information, service contract, entitlement details, and any associated SLAs.

**Note:** These steps also apply to case type configuration.

To configure case management, use the Customer Service-guided setup. The guided setup takes you through the entire setup and configuration process.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, select **Get Started**.

3.  In the Case Management category, view the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Cases and case tasks](../concept/csm-cases-case-tasks-overview.md)

</td><td>

Case records include detailed information about customers, their reported questions or issues, and the work performed to answer questions and resolve issues.

</td></tr><tr><td>

[Configure a case form view](configure-case-form.md)

</td><td>

The case form displays detailed information about a customer issue or problem. Configure a case form view to display the desired fields and related lists.

</td></tr><tr><td>

[Configure SLA definitions for customer service cases](t_DefineSLAForCustServiceCase.md)

</td><td>

Customer Service Management uses service level agreements \(SLAs\) with customer service cases. SLA can be attached to a service contract, to a company, and to a product and can be configured to start, pause, and stop based on any customer service case attributes.

 After creating the necessary SLAs, associate them with customer service cases related list on the case form.

</td></tr><tr><td>

[Configure case routing and assignment](configure-case-routing-assignment.md)

</td><td>

The case routing feature uses matching rules and assignment rules to identify cases that meet certain conditions and then route those cases to customer service agents.Create matching rules to identify cases and then create assignment rules to route cases to agents.

</td></tr><tr><td>

[Configure case routing and assignment](configure-case-routing-assignment.md)

</td><td>

The case routing feature uses matching rules and assignment rules to identify cases that meet certain conditions and then route those cases to customer service agents.

</td></tr><tr><td>

[Configure assignment workbench](configure-assignment-workbench.md)

</td><td>

The assignment workbench uses configurable criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking. Managers can view these results and select one button to assign a task.To configure the assignment workbench:

-   Create matching criteria.
-   Create an assignment workbench configuration.


</td></tr><tr><td>

[Configure major issue management](configure-major-issue-management.md)

</td><td>

Major issue management enables customer communication for issues that impact a wider audience. Use this feature for the impacted customers, create cases for these customers, provide information, and manage the resolution process.

</td></tr><tr><td>

[Targeted communications](../concept/c_TargetedCommunications.md)

</td><td>

The Targeted Communications application provides the ability to create and send articles and emails to internal and external customers.

</td></tr><tr><td>

[Configure special handling notes](configure-special-handling-notes.md)

</td><td>

Use special handling notes to bring important case information to an agent’s attention. Create a configuration for the case \[sn\_customerservice\_case\] table and then configure the form layout to display the notes in a pop-up window or a related list.

</td></tr><tr><td>

[Configure case action status](configure-case-action-status.md)

</td><td>

The case action status feature enables customer service agents to identify cases that need attention and quickly prioritize their work. Visual indicators in the **Action Status** column on the case list highlight case status.

</td></tr><tr><td>

[Create cases as a proxy contact](../concept/employee-create-case-for-customer.md)

</td><td>

The proxy contact role creates cases and requests on behalf of customers by email, phone, chat, Virtual Agent, and from the customer service portal.

</td></tr><tr><td>

[Configure auto close resolved cases](configure-auto-close-resolved-cases.md)

</td><td>

Automatically close cases in the Resolved state if customers do not take any action.

</td></tr><tr><td>

[Configure escalation management](configure-escalation-management.md)

</td><td>

Escalating a case or account raises awareness about important customer issues, facilitates communication, and enables you to track progress toward a resolution. Create escalation templates and severity definitions to control the escalation process.

</td></tr><tr><td>

[Configure case digests](configure-case-digests.md)

</td><td>

Case digests enable agents to communicate with customers and internal stakeholders about cases. -   Summaries: While a case is in progress, agents can send periodic case summaries that describe actions taken, next steps, and other case-related information.
-   Post case reviews: When the work on a case has been completed, agents can create a post case review that includes information such as the root cause, mitigation plan, and preventive actions.


</td></tr></tbody>
</table>4.  To perform a task, select **Configure**.

    This button opens the page in your instance where the configuration is completed.


