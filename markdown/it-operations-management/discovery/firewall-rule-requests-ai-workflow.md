---
title: Firewall rule requests using agentic workflows
description: The Firewall Management Task Creation agentic workflow provides a path to request new firewall rules through natural language prompts in the Now Assist panel.Use the Firewall Management Task Creation agentic workflow to request new firewall rules through natural language prompts.Review AI-generated firewall rule requests, evaluate risk analysis, and approve or reject requests with device group assignment.Automatically implement approved firewall rules on Panorama servers through the change management process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/firewall-rule-requests-ai-workflow.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-05-04"
reading_time_minutes: 6
keywords: [firewall, agentic workflow, Now Assist, Panorama, firewall, agentic workflow, Now Assist, rule request, firewall, approval, rule request, device group, firewall, implementation, Panorama, change management]
breadcrumb: [Using Firewall Audits and Reporting, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Firewall rule requests using agentic workflows

The Firewall Management Task Creation agentic workflow provides a path to request new firewall rules through natural language prompts in the Now Assist panel.

The workflow reads your natural-language request, extracts the required parameters—source IP, destination IP, protocol, traffic direction, action, and conformance type—and prompts you for any values you did not provide. Before creating a rule task, the workflow runs a risk analysis based on the request data and the specified conformance framework. The risk analysis returns one of three levels:

-   **Low:** The workflow creates the rule task and attaches the risk analysis.
-   **Medium or High:** The workflow reports the risk level in the Now Assist panel and asks whether you want to continue. If you confirm, the workflow creates the rule task and attaches the risk analysis. If you decline, the workflow skips task creation. The created task includes the AI assessment so the approver can evaluate the risk.

\[Omitted image "firewall-rule-request-ai-workflow.png"\] Alt text: Firewall rule request workflow

**Parent Topic:**[Using Firewall Audits and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/firewall-audit-report-use.md)

## Request firewall rules using agentic workflow

Use the Firewall Management Task Creation agentic workflow to request new firewall rules through natural language prompts.

### Before you begin

-   Install and configure the Firewall Audits and Reporting application.
-   Install the AI Agents for Discovery plugin. This plugin is part of the AI Agent Bundle and requires a separate subscription.
-   Discover the Panorama firewall managers and devices, and verify that Discovery has populated the Panorama Firewall Address Objects table.

Role required: firewall\_admin

### About this task

For information about how the workflow evaluates risk and determines whether to create a rule task, see [Firewall rule requests using agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/firewall-rule-requests-ai-workflow.md).

\[Omitted image "firewall-rule-request-now-assist.png"\] Alt text: Now Assist agentic workflow

### Procedure

1.  Open the Now Assist panel.

    The Now Assist panel is available from the header bar of your instance. Select the Now Assist icon to open the chat window.

2.  In the Now Assist chat, type `Create a firewall rule` or a similar phrase to trigger the Firewall Management Task Creation agentic workflow.

3.  Enter your firewall rule request in natural language, including the source IP, destination IP, protocol, traffic direction, and action.

4.  Respond to the workflow prompts for any missing information.

5.  Review the workflow response in the Now Assist chat.

    The response includes the rule task number, the extracted request data, and the risk-analysis summary. If the risk level is medium or high, the workflow asks whether you want to continue. Select **Yes** to create the rule task or **No** to cancel.

6.  Verify the rule task by navigating to **Rule Requests** &gt; **Rule Requests Task**.

    Your request appears in the list with the **AI Resolution Plan** field set to true and the AI risk analysis attached as work notes.


## Approve firewall rule requests

Review AI-generated firewall rule requests, evaluate risk analysis, and approve or reject requests with device group assignment.

### Before you begin

Role required: none. Approval access is granted to members of the approval group specified on the rule task. The admin user can edit the approver list on the rule task.

### About this task

Requests created from the agentic workflow include an AI assessment that summarizes the request and indicates whether the request is good to approve. Approvers can use this assessment instead of manually evaluating each parameter. Before approval, the workflow posts a chat message indicating that the device group cannot be automatically determined. A device group is a logical bundle of devices on which the rule is created. The approver, who is familiar with the firewall infrastructure, must specify the device group on which to apply the rule.

### Procedure

1.  Navigate to **All** &gt; **Self Service** &gt; **My Approvals**.

2.  Open the rule task and review the AI assessment in the work notes.

    The status **Good to Approve** indicates that the AI risk analysis returned low risk.

3.  In the chat prompt, specify the device group on which to create the rule.

    For example, `test1`.

4.  Approve or reject the request.

    -   Select the green checkmark to approve the request. The workflow calls the Panorama REST API to check whether the rule already exists. If the rule exists, the workflow reports the result in the work notes and no further action is required. If the rule does not exist, the workflow proceeds to implementation.

        **Note:** A background sub-flow creates a change request after the rule task reaches the **Close Complete** state with **AI Resolution Plan** set to true. The change request is created only if the change management plugin is activated.

    -   Select the red X to reject the request. The request is returned to the requester for revision.

### Result

If the request is approved:

-   The Firewall Audits and Reporting application verifies whether the requested rule already exists on Panorama.
-   If the rule does not exist, the assignment group works on the request and marks it **Close Complete**.
-   A change request is created with an implementation plan that contains the source IP, destination IP, traffic flow, action, port, protocol, and device group.

## Implement firewall rules on Panorama

Automatically implement approved firewall rules on Panorama servers through the change management process.

### Before you begin

-   Verify that the **AI Resolution Plan** field on the rule task is set to true. This field is set automatically when the request is created from the Now Assist panel.

Role required: none. Implementation access is granted to members of the assignment group on the change request.

### About this task

The instance calls a REST API to create and commit the rule, so the assignment group does not have to log in to Panorama manually. The implementation step is not automated if the **AI Resolution Plan** field is empty, for example when the request is created from the Service Catalog instead of the agentic workflow. In that case, a member of the assignment group must log in to Panorama, create the rule manually, and mark the change request as **Review**.

### Procedure

1.  Navigate to the change request created from the rule task.

2.  Progress the change request through the standard change management states to **Implement**.

    Update the **State** field on the change request form in sequence: **Assess**, **Authorize**, **Scheduled**, then **Implement**. Each state may require review and approval by the relevant stakeholders before you can advance to the next.

    When the state reaches **Implement**, the workflow calls the Panorama REST API to create and commit the rule on the device group specified during approval.

3.  Review the rule on the change request.

    The work notes show whether the rule was created and committed successfully, along with the rule name.

4.  If the rule was created as expected, close the change request.


### Result

The rule is created and committed on the Panorama server for the specified device group. The work notes on the change request confirm the result and include the rule name.

**Note:** Create saves the rule on the Panorama server without applying it to devices. Commit applies the rule to all relevant devices. The automation performs both actions in a single API call.

