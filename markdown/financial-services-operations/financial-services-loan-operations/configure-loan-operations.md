---
title: Configure Financial Services Loan Operations
description: Review the components that are installed with the Financial Services Loan Operations application and modify as needed for your organization's business needs.
locale: en-US
release: yokohama
product: Financial Services Loan Operations
classification: financial-services-loan-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting up Financial Services Loan Operations, Loan Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Configure Financial Services Loan Operations

Review the components that are installed with the Financial Services Loan Operations application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Financial Services Loan Operations application is installed. For more information, see [Install Financial Services Business Loan Operations](install-fso-business-loan-ops.md) and [Install Financial Services Personal Loan Operations](install-fso-personal-loan-ops.md).

Role required: sn\_bom\_loan\_b2b.admin, sn\_bom\_loan.b2c\_admin, and admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](../../fso-common/task/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

    |Task|Description|
    |----|-----------|
    |**Configure service definitions**|[Configure service definitions](../../fso-common/task/configure-service-definitions.md) to enable unique flows and views for loan service cases and tasks.|
    |**Configure record producers**|[Create or modify record producers](../../fso-common/task/create-modify-record-producers-fso-apps.md) to define request forms.|
    |**Edit or create new flows**|[Edit or create new flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.|
    |**Modify interceptors and workspace record type selectors**|[Modify interceptors and workspace record type selectors](../../fso-common/concept/configure-request-types-fso.md) to configure loan request types.|
    |**Configure playbook**|[Edit or create a new playbook](../../fso-common/task/configure-playbooks-fso-apps.md) using Playbooks.|
    |**Configure workspace**|[Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md) to enable agents to interact with customers and create and work on cases.|
    |**Configure Service Level Agreements \(SLAs\)**|[Configure the installed SLAs](../../fso-common/task/configure-sla-definitions-fso-cases.md) to configure SLA timings for loan service cases and tasks.|
    |**Configure user groups**|[Configure user groups](../../fso-common/task/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.|
    |**Configure assignment rules**|[Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.|
    |**Configure Document Processor**|[Configure Document Processor](../../fso-common/concept/configuring-fso-document-processor.md) for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.|


**Parent Topic:**[Setting up Financial Services Loan Operations](../concept/setting-up-fso-loan-ops.md)

