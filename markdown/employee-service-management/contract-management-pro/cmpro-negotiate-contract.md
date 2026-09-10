---
title: Contract review using external AI tool
description: Review a contract document in a connected external AI tool that retrieves the applicable contract analysis playbook from Contract Management Pro and proposes redlines based on that guidance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-negotiate-contract.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 4
keywords: [Contract negotiation, Negotiate contract document, Contract analysis playbook, Claude for Microsoft Word, AI contract review]
breadcrumb: [Review contract documents, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Contract review using external AI tool

Review a contract document in a connected external AI tool that retrieves the applicable contract analysis playbook from Contract Management Pro and proposes redlines based on that guidance.

## Before you begin

Before you review and redline a contract document using an external AI tool:

-   An administrator must set up the Contract Management Pro MCP Server. For more information, see [Set up the Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-conf-mcp-server.md).
-   A configurator must create at least one active playbook for the contract type. For more information, see [Create a contract analysis playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-create-negotiation-playbook.md).
-   You must have a connected AI tool configured to access the MCP Server.

Role required: sn\_cm\_gen\_ai.ai\_contract\_fulfiller

## About this task

The Contract Management Pro MCP Server connects MCP-compatible external AI tools to Contract Management Pro so that it can retrieve contract analysis playbooks. The external AI tool uses the playbook guidance to propose redlines in the document.

-   Contract fulfillers \(Assigned to, Collaborator, or Group manager\) can retrieve playbooks when the contract is in the Work in Progress state.
-   Contract reviewers can retrieve playbooks when the contract is in the Awaiting Review state and review task is in Work in Progress state.
-   The exact steps depend on the AI tool you use. For example, in the Claude Desktop application, you can provide the contract document as a DOCX for context. To receive tracked redlines directly in the document, use the Claude for Microsoft Word add-in with the Word document.
-   Depending on the contract request and the document, the AI tool might ask you to provide more information before it returns guidance. For example, if the company cannot be determined from the contract request or the document refers to more than one company, the tool asks you to specify the company.

For the full set of messages that the playbook tool can return, see [Contract analysis playbook tool messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-negotiation-tool-messages.md).

**Important:**

Review the proposed redlines in the external AI tool against the playbook guidance and your organization's requirements before accepting them.

Contract Management Pro includes a sample playbook named Sample Non disclosure agreement playbook. This playbook is active and uses the Non Disclosure Agreement contract type. The sample content is for testing and does not constitute legal advice.

## Procedure

1.  Log in to your ServiceNow instance as a user with the AI contract fulfiller or contract reviewer role.

2.  Open your MCP client application that is connected to your ServiceNow instance using the Contract Management Pro MCP Server.

    For example, open the Claude Desktop application or the Claude for Microsoft Word add-in. If you use the Claude for Microsoft Word add-in, open the contract document in the add-in. If you use the Claude Desktop application, attach the contract document as a PDF when you enter your prompt.

3.  Request contract analysis help by entering a prompt in the MCP client application using natural language.

    Examples:

    -   `Get contract analysis playbook for CMR0001005 using Contract Management Pro MCP Server`
    -   `Perform redlining using Contract Management Pro MCP Server`
    -   Attach contract document and give the prompt `Analyze Contract for negotiation using CM Pro MCP Server`.
4.  Enter the contract request number when prompted.

    -   The playbook tool retrieves the contract type from the contract request.
    -   If the contract request has multiple contract types, select the contract type for the document you're negotiating when prompted.
5.  If the external party can't be determined or the document references multiple parties, select the party on whose behalf the redlining should be performed when prompted.

6.  If multiple playbooks match but none is selected automatically, select a playbook manually when prompted.

    The playbook tool returns the active playbook that matches the contract type and any configured conditions. The MCP client application proposes redlines in the document based on the playbook guidance.

7.  Review the proposed redlines and accept or reject each change.

8.  Upload the redlined document into the contract request.

    -   As Contract fulfiller, upload the redlined document into the contract request by creating a revision and further review. For more information, see [Create a document revision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-create-doc-rev.md).
    -   As Contract reviewer, share the redlined document with the contract fulfiller while completing the internal review task. For more information, see [Work on internal review task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-int-review-doc.md).

**Parent Topic:**[Review contract document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-review-methods-land.md)

