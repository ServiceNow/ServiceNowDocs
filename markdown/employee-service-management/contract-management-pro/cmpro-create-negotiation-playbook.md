---
title: Create a contract analysis playbook
description: Create a contract analysis playbook that provides the negotiation guidance an external AI tool uses to propose redlines for a contract type. Add the playbook content by uploading a file or by entering it manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-create-negotiation-playbook.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 2
keywords: [Contract analysis playbook, Create playbook, Contract negotiation, Negotiation playbook]
breadcrumb: [Configure Contract Management Pro MCP Server, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create a contract analysis playbook

Create a contract analysis playbook that provides the negotiation guidance an external AI tool uses to propose redlines for a contract type. Add the playbook content by uploading a file or by entering it manually.

## Before you begin

-   The Contract Management Pro MCP server must be enabled. The **Contract Analysis Playbooks** menu appears only when the MCP server is enabled. For more information, see [Set up the Contract Management Pro MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-conf-mcp-server.md).
-   The application must be in Global or ServiceNow Otto for Contract Management Pro scope.

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin or sn\_cm\_gen\_ai.ai\_contract\_config

## About this task

A contract analysis playbook defines the policy with clause level organizational positions guidance for a contract type. When an external AI tool requests guidance for a contract, the MCP server returns the active playbook that matches the contract type and conditions. Create one playbook to define the guidance that you want the AI tool to apply.

**Note:**

Contract Management Pro includes a sample playbook named Sample Non disclosure agreement playbook. This playbook is active, uses the Non Disclosure Agreement contract type.The sample content is for testing and does not constitute legal advice.

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Analysis Playbooks**.

2.  Set the application scope to ServiceNow Otto for Contract Management Pro or Global.

3.  Select **New**.

4.  On the Contract Analysis Playbook form, fill in the fields.

    For a description of the fields, see [Contract Analysis Playbook form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-negotiation-playbook-form.md).

5.  In the **Content source** field, select how to provide the playbook content.

    |Content source|Description|
    |--------------|-----------|
    |**Upload file**|Attach a document that contains the playbook content. After you select this option, the **Document** field appears so that you can attach the file. Supported formats are PDF, Word, Excel, PowerPoint, and Markdown, with a maximum file size of 800 KB.|
    |**Enter manually**|Enter the playbook content directly. After you select this option, the **Playbook content** field appears so that you can enter the guidance.|

6.  Select **Submit**.


## Result

The playbook is created. If the playbook is active, the MCP server can return it to an external AI tool when a contract matches the contract type and conditions.

**Note:**

To activate or deactivate the playbook later, open the playbook record and select or clear the **Active** check box. The playbook tool returns only active playbooks. Deactivating a playbook removes it from playbook tool selection.

