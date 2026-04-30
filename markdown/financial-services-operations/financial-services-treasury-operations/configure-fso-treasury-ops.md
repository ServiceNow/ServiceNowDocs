---
title: Configure Financial Services Treasury Operations
description: Review the components that are installed with the Financial Services Treasury Operations application and modify as needed for your organization's business needs.
locale: en-US
release: yokohama
product: Financial Services Treasury Operations
classification: financial-services-treasury-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting up Financial Services Treasury Operations, Treasury Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Configure Financial Services Treasury Operations

Review the components that are installed with the Financial Services Treasury Operations application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Financial Services Treasury Operations application is installed. For more information, see [Install Financial Services Treasury Operations](install-fso-treasury-operations.md).

Role required: sn\_bom\_treasury.admin and admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](../../fso-common/task/import-financial-accounts-products-institutions.md).

2.  Review the installed components.

    Modify them or add new ones as applicable.

<table id="choicetable_ajc_kk5_z4b"><thead><tr><th align="left" id="d89308e107">

Task

</th><th align="left" id="d89308e110">

Description

</th></tr></thead><tbody><tr><td id="d89308e116">

**Configure service definitions**

</td><td>

[Configure service definitions](../../fso-common/task/configure-service-definitions.md) to enable unique flows and views for treasury service cases and tasks. You can add new case types and configure service definitions for each type.

</td></tr><tr><td id="d89308e138">

**Edit or create flows**

</td><td>

[Edit or create flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.

</td></tr><tr><td id="d89308e160">

**Configure playbook**

</td><td>

[Edit or create a new playbook](../../fso-common/task/configure-playbooks-fso-apps.md) using Playbooks.

</td></tr><tr><td id="d89308e182">

**Configure CSM Configurable Workspace**

</td><td>

[Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md) to enable agents to interact with customers and create and work on cases.

</td></tr><tr><td id="d89308e210">

**Configure Service Level Agreements \(SLAs\)**

</td><td>

[Configure the installed SLAs](../../fso-common/task/configure-sla-definitions-fso-cases.md) to configure SLA timings for treasury service cases and tasks.

</td></tr><tr><td id="d89308e229">

**Configure user groups**

</td><td>

[Configure user groups](../../fso-common/task/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.

</td></tr><tr><td id="d89308e248">

**Configure assignment rules**

</td><td>

[Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.

</td></tr><tr><td id="d89308e264">

**Configure Document Processor**

</td><td>

[Configure Document Processor](../../fso-common/concept/configuring-fso-document-processor.md) for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.

</td></tr></tbody>
</table>
**Parent Topic:**[Setting up Financial Services Treasury Operations](../concept/setting-up-fso-treasury-operations.md)

