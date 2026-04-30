---
title: Configure Financial Services Complaint Management
description: Review the components that are installed with the Financial Services Complaint Management application and modify as needed for your organization's business needs.
locale: en-US
release: xanadu
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Setting up Financial Services Complaint Management, Financial Services Complaint Management, Common applications, Financial Services Operations \(FSO\)]
---

# Configure Financial Services Complaint Management

Review the components that are installed with the Financial Services Complaint Management application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Financial Services Complaint Management application is installed. For more information, see [Install Financial Services Complaint Management](install-fso-complaints-management.md).

Role required: sn\_bom\_compl.admin and admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](../../fso-common/task/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

    |Task|Description|
    |----|-----------|
    |**Configure service definitions**|[Configure service definitions](../../fso-common/task/configure-service-definitions.md) to enable unique flows and views for complaint service cases and tasks.|
    |**Configure record producers**|[Create or modify record producers](../../fso-common/task/create-modify-record-producers-fso-apps.md) to define request forms.|
    |**Modify interceptors and workspace record type selectors**|[Modify interceptors and workspace record type selectors](../../fso-common/concept/configure-request-types-fso.md) to configure complaint request types.|
    |**Edit or create flows**|[Edit or create flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.|
    |**Configure playbook**|[Edit or create a new playbook](../../fso-common/task/configure-playbooks-fso-apps.md) using Playbooks.|
    |**Configure workspace**|[Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md) to enable agents to interact with customers and create and work on cases.|
    |**Define response templates**|[Define response templates](configure-response-templates-fso-complaints.md) for complaint service case for a quick and consistent messaging to customers.|
    |**Configure regulation categories and subcategories**|[Configure regulation categories and subcategories](configure-regulation-categories-fso-complaint-mgmt.md) to be used in complaint cases that have regulatory impact.|
    |**Configure Service Level Agreements \(SLAs\)**|[Configure the installed SLAs](../../fso-common/task/configure-sla-definitions-fso-cases.md) to configure SLA timings for complaint service cases and tasks.|
    |**Configure user groups**|[Configure user groups](../../fso-common/task/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.|
    |**Configure assignment rules**|[Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.|


