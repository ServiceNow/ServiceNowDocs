---
title: Complete procurement tasks using SPO MCP Server
description: View the status of your procurement tasks and complete approval, sourcing, and receipt tasks in your MCP client connect to SPO MCP Server. For tasks that require external interactions, such as signing a document or watching a video, the SPO MCP Server routes you to the Employee Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/task-completion-using-spo-mcp-server.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
keywords: [Task completion, Status visibility, SPO MCP Server, MCP client]
breadcrumb: [Use SPO MCP Server, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Complete procurement tasks using SPO MCP Server

View the status of your procurement tasks and complete approval, sourcing, and receipt tasks in your MCP client connect to SPO MCP Server. For tasks that require external interactions, such as signing a document or watching a video, the SPO MCP Server routes you to the Employee Center.

## Before you begin

Before you begin, confirm the following:

-   SPO MCP Server must be activated and connected to your MCP client.
-   You must have access to an MCP client such as Claude.

Role required: sn\_spend\_genai\_requester

## About this task

Manage procurement tasks directly in your MCP client without switching between multiple systems. You can view all tasks assigned to you based on your instance access control lists \(ACLs\). Some tasks, such as e-signature or document uploads, require you to navigate to Employee Center. Others, such as recording receipts and approvals, can be completed entirely in your MCP client.

|Task type|Completable in MCP client|Action|
|---------|-------------------------|------|
|Receipt|Yes|Enter full or partial received quantities for line items.|
|Approval|Yes|Approve or request cancellation or more information.|
|E-signature|No|Navigate to Employee Center to sign documents.|
|DocuSign|No|Navigate to Employee Center to upload and sign documents.|
|Off-catalog request|No|Navigate to Employee Center to submit the request.|

## Procedure

1.  Open your MCP client, such as Claude, that is connected to your ServiceNow instance using the SPO MCP Server.

    For more information on how to configure SPO MCP Server, see [Activate SPO MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-spo-mcp-server.md).

2.  In your MCP client, enter a prompt to view your assigned tasks.

    For example, enter `What are my procurement tasks`.

    Your MCP client displays all tasks assigned to you based on your user role and ACL permissions. Each task shows the task type, associated action, creation date, and current status.

3.  Select a task to complete.

    You can either select a task from the list or provide a specific task number if you already know which task you want to work on.

4.  Complete the task action.

    Different task types require different actions:

    -   For receipt tasks, enter the received quantities for one or more line items. You can select a full receipt or specify partial quantities. For example, if you ordered 20 items and received 3 today, you can specify the partial receipt of 3 units.
    -   For approval tasks, review the request details and approve or request cancellation or additional information.
    -   For other tasks, follow the prompts for your specific task type.
5.  For tasks requiring Employee Center, select the generated link to navigate to Employee Center to complete the action.

    Your MCP client supports the completion of receipt, approval, and sourcing tasks. For tasks such as e-signature, document uploads \(DocuSign\), or off-catalog requests, your MCP client provides a direct link to Employee Center. Select the link to navigate to Employee Center and complete the required action there, then return to your MCP client to continue managing additional tasks.


## Result

Your task is completed. If the task was completable in your MCP client, ServiceNow Otto for SPO updates the task status immediately. If the task required actions in Employee Center, the task is updated after you complete those actions. You can now select another task from your list to continue managing your procurement workflow in your MCP client.

