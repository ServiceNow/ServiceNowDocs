---
title: Configure Financial Services Card Operations
description: Review the components that are installed with the Financial Services Card Operations application and modify as needed for your organization's business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/financial-services-card-operations/set-up-card-operations.html
release: zurich
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2025-07-31"
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

    For more information, see [Import your financial data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

    |Task|Description|
    |----|-----------|
    |**Configure service definitions**|[Configure service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-service-definitions.md) to enable unique flows and views for card service cases and tasks.|
    |**Configure record producers**|[Create or modify record producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/create-modify-record-producers-fso-apps.md) to define request forms.|
    |**Edit or create new flows**|[Edit or create new flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.|
    |**Modify interceptors and workspace record type selectors**|[Modify interceptors and workspace record type selectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-request-types-fso.md) to configure payment request types.|
    |**Configure Service Level Agreements \(SLAs\)**|[Configure the installed SLAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-sla-definitions-fso-cases.md) to configure SLA timings for card service cases and tasks.|
    |**Configure user groups**|[Configure user groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.|
    |**Configure assignment rules**|[Configure assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.|
    |**Configure properties**|[Configure properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services-card-operations/properties-installed-card-ops.md) for card operations.|


