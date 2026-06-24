---
title: Configure Individual Life Claims
description: Configure the components that are installed with the Individual Life Claims application to meet your organization's claims requirements. Examples include long-term care, disability, or critical illness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/insurance-claims/configure-individual-life-claims.html
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Configure, Individual Life Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure Individual Life Claims

Configure the components that are installed with the Individual Life Claims application to meet your organization's claims requirements. Examples include long-term care, disability, or critical illness.

## Before you begin

Make sure that the Individual Life Claims application is installed. For more information, see [Install Individual Life Claims](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/install-individual-life-claims.md).

Role required: admin

## About this task

Individual Life Claims includes a death benefit claim workflow that demonstrates the ability to work on multiple policy claims from a single case. It also includes a first-notice-of-loss \(FNOL\) playbook and a customizable workspace for claims adjusters. See [Individual Life Claims workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/individual-life-claims-workflows.md) for more information.

## Procedure

1.  Import your insurance policies, financial products, and financial institutions into ServiceNow tables.

    For more information, see [Import your financial data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them, or add new ones as applicable.

<table id="choicetable_oxg_nxp_4bc"><thead><tr><th align="left" id="d51251e128">

Task

</th><th align="left" id="d51251e131">

Description

</th></tr></thead><tbody><tr><td id="d51251e137">

**Configure roles and user groups**

</td><td>

Determine the roles of the individuals that you need to work on the claim cases for your line of business. Set up the roles to support the permissions that are required to adjudicate a claim. The roles should inherit the included roles from FSO core. For more information, see .

 Required roles include:

 -   Viewer: Included in the Individual Life Claims application and inherits the viewer role, and account or customer data viewer roles from FSO core. This role can view the customer, case, and policy information for your line of business.
-   Adjuster: Included in the Individual Life Claims application and inherits the core adjuster role, and document processor agent role, from FSO core. This role evaluates the claims for your line of business.
-   FNOL Agent: Included in the Individual Life Claims application and inherits the first-notice-of-loss \(FNOL\) representative core role. This FNOL agent role is shared across all lines of business.
-   Manager: Included in the Individual Life Claims application and inherits the death benefit claims adjuster role. This role contains the adjuster roles for all your lines of business. This role has the permission to view Performance Analytics dashboards. This role is shared across all lines of business.
-   Admin: Included in Individual Life Claims and inherits the service definition admin core role. This role performs the configurations that are required for the application. This role is shared across all your lines of business. You may not need to make any changes to this role.
 Next, configure the user groups for the assignment of cases and tasks. You can also assign roles to groups. For more information, see [Configure user groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-groups-fso.md).

</td></tr><tr><td id="d51251e216">

**Set up script includes**

</td><td>

Use script includes to store JavaScript that runs on the server. By using script includes in your claims flow, you enable reusability and inheritance from the base objects. Add the following for each table that was created for your line of business:

-   An Action layer script include contains the UI-level action functions.
-   A Service layer script include contains the middle layer business logic.
-   A DAO layer script include contains the methods to perform CRUD operations.
-   Any other script includes based on your requirements.
Modify the ClaimConstants script include to reuse the object names across functions.

For more information, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/scripts/c_ScriptIncludes.md).

</td></tr><tr><td id="d51251e249">

**Configure tables and ACLs**

</td><td>

Configure the tables by reviewing the existing tables that were provided in Insurance Claim Core and the tables included in this application, and make changes according to your requirements.Configure access control lists \(ACLs\) on these tables to give the appropriate permissions to the roles and personas who work on the cases and tasks.

**Note:** The claims data model supports working on a single case with either a single policy, or multiple policies, or beneficiaries.

For more information, see [Data Models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/data-models.md) and [Components installed with Individual Life Claims](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/components-installed-individual-life-claims.md).

</td></tr><tr><td id="d51251e281">

**Configure form views**

</td><td>

Set up any required views for any new tables according to your business requirements.You can use the included case views and task views in this application for reference.

</td></tr><tr><td id="d51251e293">

**Configure service definitions**

</td><td>

Configure service definitions to enable unique flows and views for your service cases and tasks. For example, the services for a claim could be reporting a new claim, appealing a claim, or reopening a claim.Define the new services for each case type table in your model.

You can also define the services for task tables to create different flows for your tasks. Examples include a claim validation task flow or a claim closure task flow.

For more information, see [Configure service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-service-definitions.md).

</td></tr><tr><td id="d51251e317">

**Set up UI actions**

</td><td>

Define the actions that the user can take on the table record in a form. Examples include New, Save, Update, Assign to me, and Cancel.-   The case tables inherit the UI actions from CSM.
-   The task tables inherit the UI actions from Financial Task.
Override or hide the actions according to your business requirements.

For more information, see  and [FSO Core Banking tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/fso-core-banking-tables.md).

</td></tr><tr><td id="d51251e351">

**Configure workspaces**

</td><td>

Configure the workspaces for your defined personas to interact with the customers and create and work on cases.Use the provided landing pages and workspaces as a reference, or create your own using UI Builder.

For more information, see [Enable the claim workspace for Individual Life Claims](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/enable-claim-workspace-for-individual-life-claims.md).**Note:** The claim workspace is accessible from an adjuster task.

For more information, see [Configure CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-csm-workspace-fso-apps.md) and [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder/ui-builder-overview.md).

</td></tr><tr><td id="d51251e400">

**Configure decision tables**

</td><td>

Set up the decision tables that are specific to your business requirements.Refer to the included claim triage decision table for the rules to triage the severity of a claim.

 If the input parameters, rules, and other elements vary, new tables may be needed for each line of business.

For more information, see .

</td></tr><tr><td id="d51251e419">

**Configure the approval engine**

</td><td>

Update the approval engine properties as required at **Insurance claim operations** &gt; **Properties**.For reserves and payments, review and update the Claim reserves and payments rules decision table with your desired parameters and values.

For more information, see [Insurance claims core properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims-core-roles-and-properties.md).

</td></tr><tr><td id="d51251e447">

**Configure assignment rules**

</td><td>

Configure the assignment rules to identify the cases that meet certain conditions and then route those cases to agents. For more information, see [Configure assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-assignment-rules-fso-applications.md).

</td></tr><tr><td id="d51251e464">

**Edit or create flows**

</td><td>

Edit or create flows by using Workflow Studio. For more information, see [Edit or create flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-flow-designer-flows-fso-apps.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Setting up Individual Life Claims](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/setting-up-individual-life-claims.md)

