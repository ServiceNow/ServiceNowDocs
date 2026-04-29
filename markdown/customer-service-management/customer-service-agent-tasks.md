---
title: Customer service agent tasks
description: A customer service agent can view customer projects and create cases for customer projects and tasks.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with Customer Project Management, Integrate, Customer Service Management]
---

# Customer service agent tasks

A customer service agent can view customer projects and create cases for customer projects and tasks.

An agent must have the following roles to perform the tasks described in the following table:

-   sn\_customerservice\_agent
-   sn\_customerservice.projectstakeholder

<table id="table_b1k_hvy_gkb"><thead><tr><th>

Task

</th><th>

Details

</th></tr></thead><tbody><tr><td>

View customer projects

</td><td>

Customer service agents can view a list of customer projects by navigating to **Customer Service** &gt; **Projects** &gt; **All**. Click a project in this list to view project details on the Customer Project form, including project tasks, project contacts, and sub projects. **Note:** Agents have read-only access to project details.

</td></tr><tr><td>

View the projects and project tasks created for an account

</td><td>

Customer service agents can see projects that are linked to customer accounts. From a customer account record, agents can see the projects for that account in the **Projects** related list. Click a project in this list to view project details on the Customer Project form, including project tasks, project contacts, and sub projects.

 **Note:** Agents have read-only access to project details.

</td></tr><tr><td>

See the projects and project tasks associated with a contact

</td><td>

Customer service agents can see the projects and project tasks that are associated with a contact. Navigate to **Customer Service** &gt; **Customer** &gt; **Contacts** and select a contact. -   Click the **Projects** related list to see projects.
-   Click the **Project Tasks** related list to see tasks.

 **Note:** If necessary, configure the Contact form to add these related lists.

</td></tr><tr><td>

Create a case for a project

</td><td>

Customer service agents and agent managers can create cases for customer projects. When creating a case, the agent selects a project in the **Project** field on the Case form.

-   If an account has been selected in the **Account** field, the agent can select from the projects that are associated with that account.
-   If the **Account** field is empty, the agent can select from all projects that have been created for an account. Upon selection, the **Account** field is populated with the associated account.

 When created from a project, these fields are automatically set on the Case form.

 Cases created for a project appear in the **Cases** related list on the Customer Project form.

</td></tr><tr><td>

Create a case for a project task

</td><td>

Customer service agents and agent managers can create cases for customer project tasks.When creating a case, the agent selects a task in the **Project Task** field on the Case form.

-   If a project has been selected in the **Project** field, the agent can select from the project tasks that have been created for that project.
-   If the **Project** field is empty, the agent can select from the project tasks for all projects that have been created for an account. Upon selection, the **Project** and **Account** fields are populated with the associated project and account.

 When created from a project task, these fields are automatically set on the Case form.

 Cases created for a project task appear in the **Cases** related list on the Customer Project form and the Customer Project Task form.

</td></tr></tbody>
</table>