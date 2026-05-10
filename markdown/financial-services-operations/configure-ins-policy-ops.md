---
title: Configure Personal Lines Servicing
description: Review the components that are installed with the Personal Lines Servicing application and modify as needed for your organization's business needs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Personal Lines Servicing, Property and Casualty Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure Personal Lines Servicing

Review the components that are installed with the Personal Lines Servicing application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Personal Lines Servicing application is installed. For more information, see [Install Personal Lines Servicing](install-ins-policy-ops.md).

Role required: sn\_ins\_policy\_b2c.admin or admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](../../fso-common/task/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

<table id="choicetable_ajc_kk5_z4b"><thead><tr><th align="left" id="d131012e123">

Task

</th><th align="left" id="d131012e126">

Description

</th></tr></thead><tbody><tr><td id="d131012e135">

**Configure service definitions**

</td><td>

[Configure service definitions](../../fso-common/task/configure-service-definitions.md) to enable unique flows and views for policy service case and task. You should configure service definitions for:-   Personal Lines Servicing
-   Insurance Underwriting Operations


</td></tr><tr><td id="d131012e168">

**Configure record producers**

</td><td>

[Create or modify record producers](../../fso-common/task/create-modify-record-producers-fso-apps.md) to define request forms.

</td></tr><tr><td id="d131012e188">

**Create flows**

</td><td>

[Create flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.

</td></tr><tr><td id="d131012e210">

**Configure playbooks**

</td><td>

[Edit or create a new playbook](../../fso-common/task/configure-playbooks-fso-apps.md) using Playbooks.

</td></tr><tr><td id="d131012e232">

**Configure CSM Configurable Workspace**

</td><td>

[Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md) to enable requesters, contributors, and processors to interact with customers, and create and work on cases.

</td></tr><tr><td id="d131012e259">

**Modify interceptors and workspace record type selectors**

</td><td>

[Modify interceptors and workspace record type selectors](../../fso-common/concept/configure-request-types-fso.md) to configure policy request types.

</td></tr><tr><td id="d131012e278">

**Configure user groups**

</td><td>

[Configure user groups](../../fso-common/task/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.

</td></tr><tr><td id="d131012e297">

**Configure assignment rules**

</td><td>

[Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.

</td></tr><tr><td id="d131012e314">

**Configure Service Level Agreements \(SLAs\)**

</td><td>

[Configure the installed SLAs](../../fso-common/task/configure-sla-definitions-fso-cases.md) to configure SLA timings for policy service cases and tasks.

</td></tr><tr><td id="d131012e333">

**Configure Document Processor**

</td><td>

[Configure Document Processor](../../fso-common/concept/configuring-fso-document-processor.md) for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.

</td></tr></tbody>
</table>
**Parent Topic:**[Personal Lines Servicing](../concept/fso-ins-personal-policy-ops-landing-page.md)

