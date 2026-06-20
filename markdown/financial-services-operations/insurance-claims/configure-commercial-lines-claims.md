---
title: Configure Commercial Lines Claims
description: Review the components that are installed with the Commercial Lines Claims application and modify as needed for your organization's business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/insurance-claims/configure-commercial-lines-claims.html
release: zurich
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Commercial Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Configure Commercial Lines Claims

Review the components that are installed with the Commercial Lines Claims application and modify as needed for your organization's business needs.

## Before you begin

Make sure that the Commercial Lines Claims application is installed. For more information, see [Install Commercial Lines Claims](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/install_commercial_lines_claims.md).

Role required: sn\_ins\_claim\_cml.admin and admin

## Procedure

1.  Import your financial accounts, financial products, financial institutions, and transactions data into ServiceNow tables.

    For more information, see [Import your financial data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/import-financial-accounts-products-institutions.md).

2.  Review the installed components and modify them or add new ones as applicable.

<table><thead><tr><th align="left" id="d95693e115">

Task

</th><th align="left" id="d95693e118">

Description

</th></tr></thead><tbody><tr><td id="d95693e124">

**Configure service definitions**

</td><td>

Configure service definitions to enable unique flows and views for service cases and tasks. For more information, see [Configure service definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-service-definitions.md).You can add new case types and configure service definitions for each type.

</td></tr><tr><td id="d95693e146">

**Edit or create flows**

</td><td>

Edit or create flows using Workflow Studio. For more information, see [Edit or create flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-flow-designer-flows-fso-apps.md).

</td></tr><tr><td id="d95693e168">

**Configure playbook**

</td><td>

Create a playbook by using Playbooks. For more information, see [Edit or create a new playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-playbooks-fso-apps.md).

</td></tr><tr><td id="d95693e190">

**Configure CSM Configurable Workspace**

</td><td>

Configure CSM Configurable Workspace to enable agents to interact with customers and create and work on cases.For more information, see [Configure CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-csm-workspace-fso-apps.md).

</td></tr><tr><td id="d95693e224">

**Configure the Claim Workspace, Fraud score and Claim summary pages**

</td><td>

Configure Claim workspace, Fraud score, and Claim summary pages on claim cases and claim adjuster tasks. For more information, see [Enable Claim workspace, Fraud score, and Claim summary pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/insurance-claims/enable-fraud-score-and-claim-summary-pages.md).**Note:** The Claim workspace is accessible from an adjuster task. The Fraud score and Claim summary pages are accessible from both a claim case and an adjuster task.

</td></tr><tr><td id="d95693e242">

**Configure Service Level Agreements \(SLAs\)**

</td><td>

Configure the installed SLAs to configure SLA timings for claim service cases and tasks.For more information, see [Configure the installed SLAs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-sla-definitions-fso-cases.md)

</td></tr><tr><td id="d95693e263">

**Configure user groups**

</td><td>

Configure user groups for assignment of cases and tasks. You can also assign roles to groups and users.For more information, see [Configure user groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-groups-fso.md).

</td></tr><tr><td id="d95693e285">

**Configure assignment rules**

</td><td>

Configure assignment rules to identify cases that meet certain conditions and then route those cases to agents. For more information, see [Configure assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configure-assignment-rules-fso-applications.md).

</td></tr><tr><td id="d95693e301">

**Configure Document Processor**

</td><td>

Configure document processor for document categories, document types, inbound and outbound document rules, and approval rules for document deferments and exceptions.For more information, see [Configure Document Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configuring-fso-document-processor.md).

</td></tr><tr><td id="d95693e328">

**Configure Archive Rules**

</td><td>

The Archive Commercial Auto Claim Case rule archives commercial auto claim cases that are older than a year. This rule is inactive by default.To configure archive rules, navigate to **System Archiving** &gt; **Archive Rules** and enable the **Archive Commercial Auto Claim Case** rule.

</td></tr></tbody>
</table>
