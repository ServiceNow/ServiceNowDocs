---
title: Configure Personal Lines Claims
description: Review the components that are installed with the Personal Lines Claims application and modify as needed for your organization's business needs.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Personal Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure Personal Lines Claims

Review the components that are installed with the Personal Lines Claims application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Personal Lines Claims application is installed. For more information, see [Install Personal Lines Claims](install-personal-lines-claims.md).

Role required: sn\_ins\_claim\_pers.admin and admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](../../fso-common/task/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

<table id="choicetable_jt1_44w_fvb"><thead><tr><th align="left" id="d36568e109">

Task

</th><th align="left" id="d36568e112">

Description

</th></tr></thead><tbody><tr><td id="d36568e118">

**Configure service definitions**

</td><td>

Configure service definitions to enable unique flows and views for service cases and tasks. For more information, see [Configure service definitions](../../fso-common/task/configure-service-definitions.md).You can add new case types and configure service definitions for each type.

</td></tr><tr><td id="d36568e140">

**Edit or create flows**

</td><td>

Edit or create flows using Workflow Studio. For more information, see [Edit or create flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md).

</td></tr><tr><td id="d36568e162">

**Configure playbook**

</td><td>

Create a playbook by using Playbooks. For more information, see [Edit or create a new playbook](../../fso-common/task/configure-playbooks-fso-apps.md).

</td></tr><tr><td id="d36568e184">

**Configure CSM Configurable Workspace**

</td><td>

Configure CSM Configurable Workspace to enable agents to interact with customers and create and work on cases.For more information, see [Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md).

</td></tr><tr><td id="d36568e218">

**Configure the Claim Workspace, Fraud score and Claim summary pages**

</td><td>

Configure Claim workspace, Fraud score, and Claim summary pages on claim cases and claim adjuster tasks. For more information, see [Enable Claim workspace, Fraud score, and Claim summary pages](../../fso-commercial-lines-claims/task/enable-fraud-score-and-claim-summary-pages.md).**Note:** The Claim workspace is accessible from an adjuster task. The Fraud score and Claim summary pages are accessible from both a claim case and an adjuster task.

</td></tr><tr><td id="d36568e236">

**Configure Service Level Agreements \(SLAs\)**

</td><td>

Configure the installed SLAs to configure SLA timings for claim service cases and tasks.For more information, see [Configure the installed SLAs](../../fso-common/task/configure-sla-definitions-fso-cases.md)

</td></tr><tr><td id="d36568e257">

**Configure user groups**

</td><td>

Configure user groups for assignment of cases and tasks. You can also assign roles to groups and users.For more information, see [Configure user groups](../../fso-common/task/configure-groups-fso.md).

</td></tr><tr><td id="d36568e279">

**Configure assignment rules**

</td><td>

Configure assignment rules to identify cases that meet certain conditions and then route those cases to agents. For more information, see [Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md).

</td></tr><tr><td id="d36568e295">

**Configure Document Processor**

</td><td>

Configure document processor for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.For more information, see [Configure Document Processor](../../fso-common/concept/configuring-fso-document-processor.md).

</td></tr><tr><td id="d36568e322">

**Configure archive rules**

</td><td>

The Archive Personal Auto Claim Case rule archives personal auto claim cases that are older than a year. This rule is inactive by default.To configure archive rules, navigate to **System Archiving** &gt; **Archive Rules** and enable the **Archive Personal Auto Claim Case** rule.

</td></tr></tbody>
</table>
