---
title: Create cases as a proxy contact
description: The proxy contact role enables employees to create cases for customer accounts and contacts. Employees can also be proxy case contacts on behalf of customers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create cases as a proxy contact

The proxy contact role enables employees to create cases for customer accounts and contacts. Employees can also be proxy case contacts on behalf of customers.

Assign the proxy contact role \(sn\_customerservice.proxy\_contact\) to employees in your company who are not fulfillers or do not have other CSM-specific roles.

**Note:** This role requires licensing for access to CSM applications. The proxy contact cannot co-exist with the contributor roles.

Install the [CSM Extension for Proxy Contacts](../task/csm-extension-for-proxy-contacts.md) to use this functionality.

Employees with the proxy contact role can do the following:

-   Create cases on behalf of customers by email, phone, chat, Virtual Agent, and from the Customer Service Portal.
-   Create requests on behalf of customers from the Customer Service Portal.

When creating a case, the employee can select a customer contact or a partner contact as the case contact. The employee is also added to the case as the internal contact.

From the Customer Service Portal, employees can do the following for the cases where they are the internal contact:

-   View a list of cases.
-   View case details.
-   Add comments or attachments to a case.
-   Accept or reject a case resolution.
-   View a list of related work orders.
-   Check the status of a case using Virtual Agent.

Customer service agents can create cases and designate an employee with the proxy contact role as the internal contact.

-   From Agent Workspace, agents can create cases for employees from interaction records.
-   From connect chat sessions with employees, agents can create cases that add the employee to the **Internal contact** field on the Case form.

## Plugin information

Activate the CSM Extension for Proxy Contacts \(com.snc.csm\_proxy\_contacts\) plugin to enable this feature. This plugin adds the following to Customer Service Management:

-   The sn\_customerservice.proxy\_contact role.
-   The ProxyContactHelper script include.
-   The **Internal contact** field on the Case form.
-   The **Opened for** field on the Interaction form.

**Note:** You need to configure the Interaction form to display the **Opened for** field and the Case form to display the **Internal contact** field.

## Configure the Customer 360 ribbon component in Agent Workspace

With the workspace administrator role \(workspace\_admin\), you can configure the Customer 360 ribbon component to display the internal contact for a case.

-   If the **Contact** field \(the primary field\) is populated on the Case form, the Customer 360 component displays the contact information.
-   If the **Consumer** field \(the secondary field\) is populated on the Case form, the Customer 360 component displays the consumer information.
-   If the **Internal contact** field \(the tertiary field\) is populated on the Case form, and the **Contact** and **Consumer** fields do not contain any data, the Customer 360 component displays the internal contact \(employee\) information.

## Internal contact field on Case form

When an employee with the sn\_customerservice.proxy\_contact role creates a case for a customer account, the **Internal contact** field on the Case form is populated with the employee's name. This field determines case visibility for the employee. From the Customer Service Portal, employees can see cases that they have created and are identified as the internal contact.

**Note:** This field appears on the Case form in both the platform interface and Agent Workspace.

When an agent creates a case, they can select an employee with the sn\_customerservice.proxy\_contact role in the **Internal contact** field.

## Creating a case from the Customer Service Portal

An employee with the proxy contact role can create a case for a customer from the Customer Service Portal. As part of creating a case, the employee:

-   Selects an account.
-   Selects a contact from the available contacts for the account.
-   Selects an asset or product for the account.
-   Enters a subject and description for the case.

When the case is created, the employee is added to the **Internal contact** on the Case form.

## Creating a case from an interaction record

An agent can create a case for an employee by clicking **Create Case** on the Interaction form. On the resulting Case form, the **Internal contact** field:

-   Is set to the value from the **Opened for** field if the employee has the proxy contact role.
-   Remains blank if the user in the **Opened for** field does not have the proxy contact role.

## Creating a case via email

Employees can create a case by sending an email to the inbound email address. When the email is received, the system checks to see if the user has the proxy contact role.

-   If yes, the case is created and the employee is added to the **Internal contact** field. The content of the email is logged in the case activity stream.
-   If no, the case is not created.

## Initiating a chat from the Customer Service Portal

Employees with the proxy contact role can initiate a chat with an agent directly from the Customer Service Portal or using Virtual Agent. This creates a chat request card with the employee's name in the agent's inbox.

-   **Agent Workspace**: when the agent accepts the chat, the interaction record displays the employee name in the **Opened for** field.
-   **Platform**: when the agent accepts the chat and creates a case a case from the chat session, the employee name is added to the Case form in the **Internal contact** field.

## Check the status of a case using Virtual Agent

Employees with the proxy contact role can use Virtual Agent to check the status of a case where they are the internal contact.

After logging in to the Customer Service Portal and initiating Virtual Agent, use the options available with the **Check Case Status** topic.

## Viewing work orders

From the Customer Service Portal, employees with the sn\_customerservice.proxy\_contact role can see work orders for the cases where they are the internal contact. Employees can also add attachments to the work orders.

In the portal header, click **Support** &gt; **Work Orders**.

## Employee notifications

The system sends an email notification to the employee in the **Internal contact** field on the Case form when:

-   The case is opened or closed.
-   Comments are added to the case.

