---
title: Configure Group Life Servicing
description: Review the components that are installed with the Group Life Servicing application and modify as needed for your organization's business needs.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up Group Life Servicing, Group Life Servicing, Life Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure Group Life Servicing

Review the components that are installed with the Group Life Servicing application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Group Life Servicing application is installed. For more information, see [Install Group Life Servicing](install-group-life-servicing.md).

Role required: sn\_ins\_group\_life.admin or admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](../../fso-common/task/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

<table><thead><tr><th align="left" id="d30673e102">

Task

</th><th align="left" id="d30673e105">

Description

</th></tr></thead><tbody><tr><td id="d30673e114">

**Configure service definitions**

</td><td>

[Configure service definitions](../../fso-common/task/configure-service-definitions.md) to enable unique flows and views for policy service case and task. You should configure service definitions for:-   Group Life and Disability Servicing
-   Group Life and Disability Underwriting


</td></tr><tr><td id="d30673e146">

**Configure record producers**

</td><td>

[Create or modify record producers](../../fso-common/task/create-modify-record-producers-fso-apps.md) to define request forms.

</td></tr><tr><td id="d30673e166">

**Create flows**

</td><td>

[Create flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.

</td></tr><tr><td id="d30673e188">

**Configure playbooks**

</td><td>

[Edit or create a new playbook](../../fso-common/task/configure-playbooks-fso-apps.md) using Playbooks.

</td></tr><tr><td id="d30673e210">

**Configure CSM Configurable Workspace**

</td><td>

[Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md) to enable requesters, contributors, and processors to interact with customers, and create and work on cases.

</td></tr><tr><td id="d30673e237">

**Modify interceptors and workspace record type selectors**

</td><td>

[Modify interceptors and workspace record type selectors](../../fso-common/concept/configure-request-types-fso.md) to configure policy request types.

</td></tr><tr><td id="d30673e256">

**Configure user groups**

</td><td>

[Configure user groups](../../fso-common/task/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.

</td></tr><tr><td id="d30673e275">

**Configure assignment rules**

</td><td>

[Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.

</td></tr><tr><td id="d30673e292">

**Configure Service Level Agreements \(SLAs\)**

</td><td>

[Configure the installed SLAs](../../fso-common/task/configure-sla-definitions-fso-cases.md) to configure SLA timings for policy service cases and tasks.

</td></tr><tr><td id="d30673e311">

**Configure Document Processor**

</td><td>

[Configure Document Processor](../../fso-common/concept/configuring-fso-document-processor.md) for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.

</td></tr></tbody>
</table>
