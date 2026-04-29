---
title: Configure Financial Services Card Operations
description: Review the components that are installed with the Financial Services Card Operations application and modify as needed for your organization's business needs.
locale: en-US
release: australia
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Configure Financial Services Card Operations

Review the components that are installed with the Financial Services Card Operations application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Financial Services Card Operations application is installed.

Role required: sn\_bom\_credit\_card.admin and admin

## About this task

You can set up your implementation for Financial Services Card Operations by installing the Financial Services Card Operations application, importing financial services data, and reviewing and configuring the components installed with the application.

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](../../fso-common/task/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

    |Task|Description|
    |----|-----------|
    |**Configure service definitions**|[Configure service definitions](../../fso-common/task/configure-service-definitions.md) to enable unique flows and views for card service cases and tasks.|
    |**Configure record producers**|[Create or modify record producers](../../fso-common/task/create-modify-record-producers-fso-apps.md) to define request forms.|
    |**Edit or create new flows**|[Edit or create new flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.|
    |**Modify interceptors and workspace record type selectors**|[Modify interceptors and workspace record type selectors](../../fso-common/concept/configure-request-types-fso.md) to configure payment request types.|
    |**Configure Service Level Agreements \(SLAs\)**|[Configure the installed SLAs](../../fso-common/task/configure-sla-definitions-fso-cases.md) to configure SLA timings for card service cases and tasks.|
    |**Configure user groups**|[Configure user groups](../../fso-common/task/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.|
    |**Configure assignment rules**|[Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.|
    |**Configure properties**|[Configure properties](../reference/properties-installed-card-ops.md) for card operations.|


