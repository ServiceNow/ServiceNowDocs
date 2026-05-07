---
title: Firewall rule requests using agentic workflows
description: Use the Firewall Management Task Creation agentic workflow to request new firewall policies and rules from the Now Assist panel.Use the Firewall Management Task Creation agentic workflow to request new firewall rules through natural language prompts.Review AI-generated firewall rule requests, evaluate risk analysis, and approve or reject requests with device group assignment.Automatically implement approved firewall rules on Palo Alto Panorama servers through the change management process.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 4
keywords: [firewall, agentic workflow, Now Assist, Panorama, firewall, agentic workflow, Now Assist, rule request, firewall, approval, rule request, device group, firewall, implementation, Panorama, change management]
breadcrumb: [Using Firewall Audits and Reporting, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Firewall rule requests using agentic workflows

Use the Firewall Management Task Creation agentic workflow to request new firewall policies and rules from the Now Assist panel.

![Firewall rule request workflow](../image/firewall-rule-request-ai-workflow.png "Firewall rule request workflow")

**Parent Topic:**[Using Firewall Audits and Reporting](firewall-audit-report-use.md)

## Request firewall rules using agentic workflow

Use the Firewall Management Task Creation agentic workflow to request new firewall rules through natural language prompts.

### Before you begin

-   Install and configure the Firewall Audits and Reporting application.
-   Install the AI Agents for Discovery plugin. This plugin is part of the AI Agent Bundle and requires a separate subscription.
-   Discover the Panorama firewall managers and devices, and verify that Discovery has populated the Panorama Firewall Address Objects table.

Role required: firewall\_admin

### About this task

The agentic workflow reads your natural-language request, extracts the required parameters such as source IP, destination IP, protocol, traffic direction, action, and conformance type, and prompts you for values that you did not provide. The workflow runs a risk analysis based on the request data and specified conformance framework before creating the rule task. The risk analysis returns one of three levels:

-   **Low:** The workflow creates the rule task and attaches the analysis.
-   **Medium or High:** The workflow does not create the task. The workflow reports the violation in the chat and asks whether to proceed. If you confirm, the workflow creates the task and attaches the risk analysis.

![Now Assist agentic workflow](../image/firewall-rule-request-now-assist.png "Now Assist agentic workflow")

### Procedure

1.  Open the Now Assist panel.

2.  Trigger the Firewall Management Task Creation agentic workflow.

3.  In the chat, enter your firewall rule request in natural language and include the source IP, destination IP, protocol, traffic direction and action.

4.  Respond to the workflow's prompts for missing information.

5.  Review the workflow's response.

    The response includes the rule task number, the extracted request data, and the risk-analysis summary.


### Result

To verify the rule task, navigate to **Rule Requests** &gt; **Rule Requests Task**. Your request appears in the list with the **AI Resolution Plan** field set to true and the AI risk analysis attached as work notes.

## Approve firewall rule requests

Review AI-generated firewall rule requests, evaluate risk analysis, and approve or reject requests with device group assignment.

### Before you begin

Role required: Members of the approval group specified on the rule task. The admin user can edit the approver list on the rule task.

### About this task

Requests created from the agentic workflow include an AI assessment that summarizes the request and indicates whether the request is good to approve. Approvers can use this assessment instead of manually evaluating each parameter. Before approval, the workflow posts a chat message indicating that the device group cannot be automatically determined. A device group is a logical bundle of devices on which the rule is created. The approver, who is familiar with the firewall infrastructure, must specify the device group on which to apply the rule.

### Procedure

1.  Navigate to **All** &gt; **Self Service** &gt; **My Approvals**.

2.  Open the rule task and review the AI assessment in the work notes.

    The status good to approve indicates that the AI risk analysis returned low risk.

3.  In the chat prompt, specify the device group on which to create the rule.

    For example, `test1`.

4.  Select the green checkmark to approve the request.


### Result

The Firewall Audits and Reporting application calls the Panorama REST API to verify whether the requested rule already exists. If the rule exists, the workflow reports the result in the chat and no further action is required. If the rule does not exist, the workflow proceeds to the next step. The assignment group works on the request and marks it **Close Complete**. A background sub-flow creates a change request after the rule task is marked **Close Complete** with **AI Resolution Plan** set to true. The implementation plan contains the source IP, destination IP, traffic flow, action, port, protocol, and device group.

**Note:** The change request is created only if the rule task is **Approved** and in the **Close Complete** state, and the change request plugin is activated.

## Implement firewall rules on Palo Alto Panorama

Automatically implement approved firewall rules on Palo Alto Panorama servers through the change management process.

### Before you begin

-   Verify that the **AI Resolution Plan** field on the rule task is set to true. This field is set automatically when the request is created from the Now Assist panel.

Role required: Members of the assignment group on the change request.

### About this task

The instance calls a REST API to create and commit the rule, so the assignment group does not have to log in to Panorama manually. The implementation step is not automated if the **AI Resolution Plan** field is empty, for example when the request is created from the Service Catalog instead of the agentic workflow. In that case, a member of the assignment group must log in to Panorama, create the rule manually, and mark the change request as **Review**.

### Procedure

1.  Navigate to the change request that was created from the rule task.

2.  Move the change request through the standard change-management states: **Assess**, **Authorize**, **Scheduled**, and **Implement**.

3.  Select **Implement**.

    The workflow calls a REST API to create and commit the rule on the device group specified during approval.

4.  Review the rule on the change request.

    The work notes show whether the rule was created and committed successfully, along with the rule name.

5.  If the rule was created as expected, close the change request.


### Result

The rule is created and committed on the Panorama server for the specified device group.

**Note:** Commit applies the rule to all relevant devices on the Panorama server. Create saves the rule without applying it. The automation performs both create and commit in a single API call.

