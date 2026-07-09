---
title: Firewall rule requests using agentic workflows
description: The Firewall Management Task Creation agentic workflow provides a path to request one or more firewall rules through natural language prompts in the Now Assist panel.Use the Firewall Management Task Creation agentic workflow to request one or more firewall rules through natural language prompts in the Now Assist panel.Review AI-generated firewall rule requests, evaluate risk analysis, and approve or reject requests with device group assignment.Automatically implement approved firewall rules on Panorama servers through the change management process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/firewall-rule-requests-ai-workflow.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-07-03"
reading_time_minutes: 7
keywords: [firewall, agentic workflow, Now Assist, Panorama, firewall, agentic workflow, Now Assist, rule request, firewall, approval, rule request, device group, firewall, implementation, Panorama, change management]
breadcrumb: [Using Firewall Audits and Reporting, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Firewall rule requests using agentic workflows

The Firewall Management Task Creation agentic workflow provides a path to request one or more firewall rules through natural language prompts in the Now Assist panel.

## Multiple rule configuration support

You can request multiple firewall rule configurations in a single conversation with the agentic workflow. The workflow parses each rule individually, evaluates conformance for each one, and creates one parent firewall task with individual configuration tasks for all rules. This approach reduces the number of tasks to track and simplifies the approval process.

## Risk analysis and conformance checking

The workflow reads your natural-language request, extracts the required parameters—source IP, destination IP, protocol, traffic direction, action, and conformance type—and prompts you for any values you did not provide. Before creating a rule task, the workflow runs a risk analysis based on the request data and the specified conformance framework. When you request multiple rules, the workflow provides individual conformance feedback for each rule, such as "Out of 3 rules, 2 are non-conforming, 1 is conforming." The risk analysis returns one of three levels:

-   **Low:** The workflow creates the rule task and attaches the risk analysis.
-   **Medium or High:** The workflow reports the risk level in the Now Assist panel and asks whether you want to continue. You can choose to proceed with all rules or select specific ones. If you confirm, the workflow creates the rule task and attaches the risk analysis. If you decline, the workflow skips task creation. The created task includes the AI assessment so the approver can evaluate the risk.

**Note:** The agentic workflow provides conformance checking and risk analysis. Rule verification and creation on Panorama servers is handled through REST API calls as part of the Firewall Audits and Reporting application.

## Workflow process

\[Omitted image "firewall-rule-request-ai-workflow.png"\] Alt text: Firewall rule request workflow

**Parent Topic:**[Using Firewall Audits and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/firewall-audit-report-use.md)

## Request firewall rules using agentic workflow

Use the Firewall Management Task Creation agentic workflow to request one or more firewall rules through natural language prompts in the Now Assist panel.

### Before you begin

-   Install and configure the Firewall Audits and Reporting application.
-   Install the AI Agents for Discovery plugin. This plugin is part of the AI Agent Bundle and requires a separate subscription.
-   Discover the Panorama firewall managers and devices, and verify that Discovery has populated the Panorama Firewall Address Objects table.

Role required: firewall\_admin

### About this task

You can request multiple firewall rule configurations in a single conversation. The workflow creates one parent firewall task with individual configuration tasks for each rule. For information about how the workflow evaluates risk and determines whether to create a rule task, see [Firewall rule requests using agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/firewall-rule-requests-ai-workflow.md).

**Note:** Starting with version 1.12.0 of Firewall Audits and Reporting, all new firewall rule tasks are created in the Panorama-specific table and display the task type as Panorama.

\[Omitted image "firewall-rule-request-now-assist.png"\] Alt text: Now Assist agentic workflow

### Procedure

1.  Open the Now Assist panel.

    The Now Assist panel is available from the header bar of your instance. Select the Now Assist icon to open the chat window.

2.  In the Now Assist chat, type `Create a firewall rule` or a similar phrase to trigger the Firewall Management Task Creation agentic workflow.

3.  Enter your firewall rule request in natural language, including the source IP, destination IP, protocol, traffic direction, and action.

    You can specify multiple rule configurations in the same conversation. The workflow parses each rule individually and treats them as separate configuration tasks under one parent firewall task.

4.  Respond to the workflow prompts for any missing information.

5.  Review the workflow response in the Now Assist chat.

    The response includes the rule task number, the extracted request data, and the risk-analysis summary for each rule configuration. When you request multiple rules, the workflow provides conformance feedback for each rule individually, such as "Out of 3 rules, 2 are non-conforming, 1 is conforming." If any rule has a medium or high risk level, the workflow asks whether you want to continue. You can choose to proceed with all rules or select specific ones. Select **Yes** to create the rule task or **No** to cancel.

6.  Verify the rule task by navigating to **Rule Requests** &gt; **Rule Requests Task**.

    Your request appears in the list with the task type set to Panorama and the AI risk analysis attached as work notes. Open the parent task to view all individual rule configuration tasks.


## Approve firewall rule requests

Review AI-generated firewall rule requests, evaluate risk analysis, and approve or reject requests with device group assignment.

### Before you begin

Role required: none. Approval access is granted to members of the approval group specified on the rule task. The admin user can edit the approver list on the rule task.

### About this task

A firewall rule task can contain multiple rule configurations, each represented as an individual configuration task under the parent task. Requests created from the agentic workflow include an AI assessment that summarizes each rule request and indicates whether the request is good to approve. Approvers can use this assessment instead of manually evaluating each parameter. Before approval, the workflow posts a chat message indicating that the device group can't be automatically determined. A device group is a logical bundle of devices on which the rule is created. The approver, who is familiar with the firewall infrastructure, must specify the device group on which to apply the rule.

### Procedure

1.  Navigate to **All** &gt; **Self Service** &gt; **My Approvals**.

2.  Open the parent rule task and review the individual rule configuration tasks.

    Each configuration task includes the AI assessment in the work notes. The status **Good to Approve** indicates that the AI risk analysis returned low risk for that specific rule.

3.  In the chat prompt, specify the device group on which to create the rule.

    For example, `test1`.

4.  Approve or reject each configuration task.

    -   Select the green checkmark to approve the configuration task. The workflow calls the Panorama REST API to check whether the rule already exists. If the rule exists, the configuration task is marked as Closed Incomplete with a work note indicating the rule was not recreated. If the rule doesn't exist, the workflow proceeds to implementation.

        **Note:** A background subflow creates a change request after all configuration tasks are processed and the parent rule task reaches the **Close Complete** state. The change request is created only if the change management plugin is activated.

    -   Select the red X to reject the configuration task. The request is returned to the requester for revision.

### Result

If the configuration tasks are approved:

-   The Firewall Audits and Reporting application verifies whether each requested rule already exists on Panorama.
-   For rules that don't exist, the assignment group works on the request and marks the configuration tasks **Close Complete**.
-   A change request is created with an implementation plan that contains the source IP, destination IP, traffic flow, action, port, protocol, and device group for all approved rules.

## Implement firewall rules on Panorama

Automatically implement approved firewall rules on Panorama servers through the change management process.

### Before you begin

Role required: none. Implementation access is granted to members of the assignment group on the change request.

### About this task

When a firewall rule task contains multiple rule configurations, each configuration is validated individually as a subtask. If a rule already exists on the Panorama server, the configuration task is marked as Closed Incomplete with a work note indicating the rule was not recreated. If a rule does not exist, the configuration task proceeds to the approval and implementation process.

The instance calls a REST API to create and commit the rule, so the assignment group does not have to log in to Panorama manually. When the request is created from the Service Catalog instead of the agentic workflow, the implementation step is not automated. In that case, a member of the assignment group must log in to Panorama, create the rule manually, and mark the change request as **Review**.

### Procedure

1.  Navigate to the change request created from the parent rule task.

    The change request includes all approved rule configurations from the parent task.

2.  Progress the change request through the standard change management states to **Implement**.

    Update the **State** field on the change request form in sequence: **Assess**, **Authorize**, **Scheduled**, then **Implement**. Each state may require review and approval by the relevant stakeholders before you can advance to the next.

    When the state reaches **Implement**, the workflow calls the Panorama REST API to create and commit each approved rule on the device group specified during approval.

3.  Review the rules on the change request.

    The work notes show whether each rule was created and committed successfully, along with the rule names. For rules that already existed on the Panorama server, the work notes indicate that the rule was not recreated.

4.  If all rules were processed as expected, close the change request.


### Result

All approved rules are created and committed on the Panorama server for the specified device group. The work notes on the change request confirm the result for each rule and include the rule names.

**Note:** Create saves the rule on the Panorama server without applying it to devices. Commit applies the rule to all relevant devices. The automation performs both actions in a single API call for each rule.

