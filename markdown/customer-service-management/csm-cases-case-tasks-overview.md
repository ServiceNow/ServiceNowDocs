---
title: Cases and case tasks
description: Customer service cases store information about customers, their questions and issues, and related information. Case tasks are created and assigned to users to complete the work necessary to resolve cases.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Cases and case tasks

Customer service cases store information about customers, their questions and issues, and related information. Case tasks are created and assigned to users to complete the work necessary to resolve cases.

## Cases

A case record is the main type of record used by the Customer Service Management application. Case records include detailed information about customers, their reported questions or issues, and the work performed to answer questions and resolve issues. The system stores case records in the Case \[sn\_customerservice\_case\] table.

Customer service agents create cases to identify questions or issues, gather information, and track the activities related to resolution. Agents also use cases to communicate with customers and other users.

<table id="table_d4c_hqs_nvb"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Case details

</td><td>

The Details tab includes the following information:-   Customer information such as the customer's name, phone number, and email address.
-   Product information such as the products, assets, and services owned by the customer.
-   Case information, such as the priority, assignment group, and assigned agent.
-   Service contracts, entitlements, and associated service level agreements \(SLAs\).

</td></tr><tr><td>

Case activities

</td><td>

The Activity pane enables communication between:-   Agents and customers.
-   Agents and other employees within the organization.

The Activity pane also shows the communication history, case notes and updates, and attachments.

</td></tr><tr><td>

Related tasks

</td><td>

Related tasks include tasks that result from the case, such as case tasks, work orders, and requests. These tasks can be internal to the organization or they can involve the customer.

</td></tr><tr><td>

Information

</td><td>

Information that is gathered as part of resolving a case can be included in the knowledge base and used to help resolve similar cases. Agents can also search knowledge bases and attach useful articles.

</td></tr></tbody>
</table>For more information about cases and case records, see the following topics:

-   [Create a customer service case](../task/t_CreateACaseFromCustServApp.md)
-   [Create a customer service case of a specific type](../task/create-case-of-specific-case-type.md)
-   [Customer service case form](../reference/r_CustomerServiceCaseForm.md)

## Case tasks

Case tasks are created for additional work that must be completed as part of resolving a customer service case. These tasks are frequently assigned to users such as middle or back-office agents. Case tasks are stored in the Case Task \[sn\_customerservice\_task\] table.

Agents can manually create case tasks from cases or have them automatically generated from case playbooks. When a case task is created, the system uses information from the case to automatically populate some fields on the case task record. This includes the case number in the **Parent case** field and customer information in the **Account**, **Contact**, or **Consumer** fields, if available in the case record.

**Note:** Case tasks can also be created from other records. If a task is created from a non-case record, such as an incident, problem, change, or request, the **Parent** field is updated with the number of the parent record. The **Account**, **Contact**, or **Consumer** fields aren’t updated.

If the value in the **Parent case** or **Parent** fields is updated, the customer information in the **Account**, **Contact**, or **Consumer** fields is also updated.

Depending on a user's assigned roles, case tasks appear in a number of different Case Task lists in the application navigator in CSM Configurable Workspace, including:

-   My Case Task
-   My Open
-   Unassigned for my groups
-   All
-   My Contributing Tasks
-   My Accessible Tasks

For more information about case tasks and case task records, see the following topics:

-   [Create a task for a customer service case](../task/create-task-for-cust-service-case.md)
-   [Case task form](../reference/csm-case-task-form.md)

## Cases, case tasks and related parties

The Customer Service Management application enables you to support multiple contacts and consumers on cases and sold products and provide these contacts with varying levels of case access. These additional contacts and consumers are called related parties. Related parties are added to the Related Parties related list on the case record.

Customer service agents can also add related parties to case tasks. Customers that can be added to a case task are limited to the following:

-   Customers that are related parties on the parent case.
-   Customers that the agent has access to.

Users with the admin role can remove related parties from cases. When an admin attempts to remove a related party from a case, the system checks to see if that related party is associated with any open case tasks.

-   If no, the related party is removed from the case.
-   If yes, the related party isn’t removed from the case and the system displays a message that lists the associated case tasks.

## Case task integration with Service Definitions

The [service definitions](csm-service-definitions.md) feature enables you to create connections between products, services, and case types.

-   Agents can use configured service definitions to create cases of the correct type based on the selected product or service.
-   Customers can use configured service definitions to discover and request the services that they need .

<table id="table_mng_1wj_tvb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin\[admin\]

</td><td>

When creating and updating case tasks, users with the admin role can select service definitions in the **Service definition** field on case task records.

</td></tr><tr><td>

Case task agent\[case\_task\_agent\]

</td><td>

-   Contains the service definition viewer role \(sn\_csm\_case\_types.service\_definition\_viewer\). This role gives users access to the service definitions that are mapped to case task tables.
-   Can create case tasks and update the **Service definition** field on the case task record.

</td></tr><tr><td>

Case task viewer\[case\_task\_viewer\]

</td><td>

-   Contains the service definition viewer role \(sn\_csm\_case\_types.service\_definition\_viewer\).
-   Can view case tasks and service definitions.

</td></tr></tbody>
</table>## Case tasks and user roles

<table id="table_dgb_vwt_nvb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Admin role

</td></tr><tr><td>

Admin\[admin\]

</td><td>

This user can:-   Create and assign case tasks.
-   Update the **Account**, **Contact**, and **Consumer** fields after the case task is created.

**Note:** The admin can change the values of these fields to one of the related parties associated with the parent case.

-   Delete case tasks.

</td></tr><tr><td class="sub-head" colspan="2">

Agent roles

</td></tr><tr><td>

Customer service agent\[sn\_customerservice\_agent\]

</td><td>

This user can do the following for account cases:-   Create and assign case tasks.
-   Update all case task fields.
-   Delete case tasks.

</td></tr><tr><td>

Consumer service agent\[sn\_customerservice.consumer\_agent\]

</td><td>

This user can do the following for consumer and household cases:-   Create and assign case tasks.
-   Update all case task fields.
-   Delete case tasks.

</td></tr><tr><td>

Case task agent\[sn\_customerservice.case\_task\_agent\]

</td><td>

This user can work on case tasks that they’ve created and that are assigned to them or to their assignment groups.Case task agents have read access to the **Account**, **Contact**, **Consumer**, and **Parent case** fields for case tasks that are assigned to them or to their assignment groups.

 This user can:

-   View and update assigned tasks.
-   View and update created case tasks.
-   Create case tasks and assign those tasks to other users.
-   Add work notes, comments, and attachments to case tasks.
-   Update the status of case tasks.
-   Perform additional actions from case tasks such as sending email.

</td></tr><tr><td>

Relationship agent\[sn\_customerservice.relationship\_agent\]

</td><td>

This user can view, create, update, and delete case tasks for the customers they have relationships with.

</td></tr><tr><td>

Location agent\[sn\_customerservice.svc\_location\_agent\]

</td><td>

This user can view, create, update, and delete case tasks for the business locations they have access to.

</td></tr><tr><td>

Consumer location agent\[sn\_customerservice.svc\_location\_consumer\_agent\]

</td><td>

This user can view, create, update, and delete case tasks for the business locations they have access to.

</td></tr><tr><td>

Outsourced agent\[sn\_csm\_ocs.ext\_agent\]

</td><td>

This user can view, create, update, and delete case tasks based on the outsourcing criteria for the cases they have access to.

</td></tr><tr><td>

Account consumer\[sn\_acct\_consumer.consumer\]

</td><td>

Can view the **Account**, **Contact** and **Consumer** fields for the case tasks they have access to.

 An user with this role can work on the following case tasks:

-   Tasks that have been created by an user and tasks that are visible to them based on their access to the case.
-   Tasks that are assigned to the user or to the user's assignment groups.

 This user can:

-   View and update assigned tasks.
-   Create case tasks and assign those tasks to other users.
-   View and updated created case tasks.
-   Add work notes, comments, and attachments to case tasks.
-   Update the status of case tasks.
-   Perform additional actions from case tasks such as sending email.

**Note:** Available with the Customer data models for B2B2C plugin \(com.sn\_csm\_b2b\_consumers\).

</td></tr><tr><td class="sub-head" colspan="2">

Contributor roles

</td></tr><tr><td>

Account contributor\[sn\_customerservice.account\_contributor\]

</td><td>

This user can: -   View and update case tasks and the fields on the case task record that they have access to.
-   View the **Parent case**, **Account**, **Contact** and **Consumer** fields on the case task record

</td></tr><tr><td>

Consumer contributor\[sn\_customerservice.consumer\_contributor\]

</td><td>

This user can: -   View and update case tasks and the fields on the case task record that they have access to.
-   View the **Parent case**, **Account**, **Contact** and **Consumer** fields on the case task record

</td></tr><tr><td>

Service organization contributor\[sn\_customerservice.service\_organization\_contributor\]

</td><td>

This user can: -   View and update case tasks and the fields on the case task record that they have access to.
-   View the **Parent case**, **Account**, **Contact** and **Consumer** fields on the case task record

</td></tr><tr><td>

Self contributor\[sn\_customerservice.self\_contributor\]

</td><td>

This user can: -   View and update case tasks and the fields on the case task record that they have access to.
-   View the **Parent case**, **Account**, **Contact** and **Consumer** fields on the case task record

</td></tr><tr><td class="sub-head" colspan="2">

Related parties roles

</td></tr><tr><td>

Case authorized contact\[sn\_customerservice.case\_authorized\_contact\]

</td><td>

This user can:-   View and update case tasks and the fields that they have access to.
-   View the **Parent case**, **Account**, **Contact** and **Consumer** fields.

</td></tr><tr><td>

Case authorized consumer\[sn\_customerservice.case\_authorized\_consumer\]

</td><td>

This user can:-   View and update case tasks and the fields that they have access to.
-   View the **Parent case**, **Account**, **Contact** and **Consumer** fields.

</td></tr></tbody>
</table>## Case tasks and external user roles

End users and requesters can access case tasks from the Customer and Consumer Service Portals by selecting **My Lists** &gt; **My Case Tasks**.

End users and requesters can view and update case tasks and the fields that they have access to \(case tasks that have the **Visible to customer** field enabled\). You get read access to the **Parent case**, **Account**, **Contact** and **Consumer** fields.

-   sn\_customerservice.customer
-   sn\_customerservice.consumer
-   customer\_case\_manager
-   sn\_customerservice.partner
-   sn\_customerservice.consumer

The users can see the following fields on the Case Task lists and forms: **Account**, **Contact** and **Consumer**. If an end user is viewing a case task from a list of case tasks, the Case Task form also displays the **Parent case** field.

## Scheduled job for case tasks

Case task enhancements in the Zurich release add several fields to the case task record. After upgrading to the Zurich release, you can run a scheduled job that populates these fields for active case tasks.

**Note:** Make sure to run the scheduled job during planned downtime.

If the parent case is an active record in the Case table \(sn\_customerservice\_case\) or a table that extends the Case table, the **Update case task fields** scheduled job does the following:

-   Copies the parent case number to the **Parent case** field.
-   Copies the account and contact or consumer information to the **Account** and **Contact** or **Consumer** fields, if this information is present in the case record.

To run this scheduled job:

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.
2.  Select **Update case task fields** in the **Name** field.
3.  Select **Execute Now**.

