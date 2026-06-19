---
title: Configure Financial Services Deposit Operations
description: Review the components that are installed with the Financial Services Deposit Operations application and modify as needed for your organization's business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/financial-services-deposit-operations/configure-fso-deposit-ops.html
release: zurich
product: Financial Services Deposit Operations
classification: financial-services-deposit-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Deposit Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Configure Financial Services Deposit Operations

Review the components that are installed with the Financial Services Deposit Operations application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Financial Services Deposit Operations application is installed. For more information, see [Install Financial Services Business Deposit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-deposit-operations/install-fso-business-deposit-ops.md) and [Install Financial Services Personal Deposit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-deposit-operations/install-fso-personal-deposit-ops.md).

Role required:

-   For Financial Services Business Deposit Operations: sn\_bom\_deposit\_b2b.admin and admin
-   Financial Services Personal Deposit Operations: sn\_bom\_deposit\_b2c.admin and admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/import-financial-accounts-products-institutions.md).

2.  Review the installed components.

    Modify them or add new ones as applicable.

<table id="choicetable_ajc_kk5_z4b"><thead><tr><th align="left" id="d46080e162">

Task

</th><th align="left" id="d46080e165">

Description

</th></tr></thead><tbody><tr><td id="d46080e171">

**Configure service definitions**

</td><td>

[Configure service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-service-definitions.md) to enable unique flows and views for deposit service cases and tasks. You can add new case types and configure service definitions for each type.

</td></tr><tr><td id="d46080e193">

**Edit or create flows**

</td><td>

[Edit or create flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.

</td></tr><tr><td id="d46080e215">

**Configure playbooks**

</td><td>

[Edit or create a new playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-playbooks-fso-apps.md) using Playbooks.

</td></tr><tr><td id="d46080e237">

**Configure CSM Configurable Workspace**

</td><td>

[Configure CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-csm-workspace-fso-apps.md) to enable agents to interact with customers and create and work on cases.

</td></tr><tr><td id="d46080e265">

**Configure Service Level Agreements \(SLAs\)**

</td><td>

[Configure the installed SLAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-sla-definitions-fso-cases.md) to configure SLA timings for deposit service cases and tasks.

</td></tr><tr><td id="d46080e284">

**Configure user groups**

</td><td>

[Configure user groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.Configure agent connector and contributor roles for the groups, if required. For more information, see [Roles and Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/fso-combine-csm-industry-roles.md).

</td></tr><tr><td id="d46080e321">

**Configure assignment rules**

</td><td>

[Configure assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.

</td></tr><tr><td id="d46080e337">

**Configure Document Processor**

</td><td>

[Configure Document Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configuring-fso-document-processor.md) for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.

</td></tr></tbody>
</table>
