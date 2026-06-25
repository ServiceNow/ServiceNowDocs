---
title: Configure Individual Life Servicing
description: Review the components that are installed with the Individual Life Servicing application and modify as needed for your organization's business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/financial-services-operations/configure-individual-life-servicing.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Setting up Individual Life Servicing, Individual Life Servicing, Life Insurance Servicing, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Configure Individual Life Servicing

Review the components that are installed with the Individual Life Servicing application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Individual Life Servicing application is installed. For more information, see [Install Individual Life Servicing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/install-individual-life-servicing.md).

Role required: sn\_ins\_indiv\_life.admin or admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

<table><thead><tr><th align="left" id="d29238e98">

Task

</th><th align="left" id="d29238e101">

Description

</th></tr></thead><tbody><tr><td id="d29238e110">

**Configure service definitions**

</td><td>

[Configure service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-service-definitions.md) to enable unique flows and views for policy service case and task. You should configure service definitions for:-   Individual Life Servicing
-   Individual Life Underwriting


</td></tr><tr><td id="d29238e142">

**Configure record producers**

</td><td>

[Create or modify record producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/create-modify-record-producers-fso-apps.md) to define request forms.

</td></tr><tr><td id="d29238e162">

**Create flows**

</td><td>

[Create flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-flow-designer-flows-fso-apps.md) using Workflow Studio.

</td></tr><tr><td id="d29238e184">

**Configure playbooks**

</td><td>

[Edit or create a new playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-playbooks-fso-apps.md) using Playbooks.

</td></tr><tr><td id="d29238e206">

**Configure CSM Configurable Workspace**

</td><td>

[Configure CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-csm-workspace-fso-apps.md) to enable requesters, contributors, and processors to interact with customers, and create and work on cases.

</td></tr><tr><td id="d29238e233">

**Modify interceptors and workspace record type selectors**

</td><td>

[Modify interceptors and workspace record type selectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-request-types-fso.md) to configure policy request types.

</td></tr><tr><td id="d29238e252">

**Configure user groups**

</td><td>

[Configure user groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-groups-fso.md) for assignment of cases and tasks. You can also assign roles to groups and users.

</td></tr><tr><td id="d29238e271">

**Configure assignment rules**

</td><td>

[Configure assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-assignment-rules-fso-applications.md) to identify cases that meet certain conditions and then route those cases to agents.

</td></tr><tr><td id="d29238e288">

**Configure Service Level Agreements \(SLAs\)**

</td><td>

[Configure the installed SLAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configure-sla-definitions-fso-cases.md) to configure SLA timings for policy service cases and tasks.

</td></tr><tr><td id="d29238e307">

**Configure Document Processor**

</td><td>

[Configure Document Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/configuring-fso-document-processor.md) for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.

</td></tr></tbody>
</table>
