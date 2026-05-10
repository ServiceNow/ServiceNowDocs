---
title: Resolve a security incident
description: Chat with an AI agent in the Now Assist panel to resolve an incident.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Resolve security incidents, Use agentic workflows, Now Assist for Security Incident Response, Security Operations]
---

# Resolve a security incident

Chat with an AI agent in the Now Assist panel to resolve an incident.

## Before you begin

Role required: sn\_si.analyst

## About this task

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace**.

2.  Open the security incident that you want to resolve using the AI agent.

3.  Select the Now Assist \(![Now Assist panel for AI agent icon.](../image/ai-icon-now-assist.png)\) icon.

    The Resolve security incident agentic workflow is on-demand. You can enter a query in natural language to resolve a security incident by using this agentic workflow.

4.  On the Now Assist panel, ask the agent to resolve the security incident by entering `Resolve this incident`, `Resolve this security incident`, or `Resolve the security incident: SIR0012345`.

    The Now Assist panel provides all the actions that you can perform on the security incident.

5.  Select **Resolve security incident**.

    ![Sample resolution plan for a security incident.](../image/ai-agent-resolution-plan.png)

    The AI agent analyzes the security incident and provides a summary of the incident and its current state. Additionally, by using the incident details, knowledge articles, and similar closed security incidents, the AI agent provides a resolution plan.

6.  Enter positive responses such as `looks good` or `Ok` if you agree to the resolution plan.

    For a positive response, the AI agent investigates each step in the resolution plan and assists the analyst \(the user with the sn\_si.analyst role\) to resolve it. For each step, the AI agent provides feedback and requests for intervention from the analyst. For example, if the AI agent identifies the incident generated for a phishing email, the following agentic workflow occurs:

<table id="table_q2r_srk_52c"><thead><tr><th>

Tasks to resolve a security incident

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update the state of security incident

</td><td>

The AI agent updates the state of the security incident. For example, if the state of the security incident is Draft, the AI agent updates it to Analysis.

</td></tr><tr><td>

Run threat lookup and observable enrichment on observable

</td><td>

The AI agent initiates a threat lookup and observable enrichment process. When the analyst confirms with a positive input, the AI agent provides the Observable Analysis and Enrichment summary.

</td></tr><tr><td>

For malicious observables, send email to management

</td><td>

The analyst can ask the AI agent to send a mail to the management. The AI agent provides a draft email and asks for the recipients of the email.

**Note:** The analyst can verify the sent email in the **Other Records** tab.

</td></tr><tr><td>

Check with affected user if they interacted with the phishing email

</td><td>

The analyst manually checks with the affected user if they interacted with the phishing email.

</td></tr><tr><td>

If user interacted with the phishing email, reset its password credentials

</td><td>

If the affected user interacted with the phishing email, the analyst can ask the AI agent to create an incident to reset the user password.The AI agent provides a summary for the incident and creates an incident when the analyst approves the summary.

</td></tr><tr><td>

Block the sender/email/URL on the email gateway

</td><td>

The AI agent requests the analyst for blocking for sender/email/URL on the email gateway. The analyst can ask the AI agent to create a response task for blocking sender/email/URL on the email gateway.

The AI agent provides the information for the response tasks and creates a response task after the analyst approves it.

**Note:** The analyst can complete the response task and mark the response task as **Complete** on the **Response Tasks** tab.

The analyst confirms to the AI agent that the response task is complete.

</td></tr><tr><td>

Search and delete the phishing email from all user inboxes

</td><td>

The AI agent informs the analyst to delete the phishing email from all user inboxes.

 The analyst deletes the phishing email and confirms to the AI agent.

</td></tr><tr><td>

Enroll affected user in a mandatory phishing training

</td><td>

If the affected user has interacted with the phishing email, the AI agent informs the analyst to enroll the affected user in the mandatory phishing training.

</td></tr><tr><td>

Perform the audit of the security incident

</td><td>

The AI agent performs the audit of the security incident and provides the summary.

</td></tr><tr><td>

Close the security incident

</td><td>

The AI agent closes the incident. For more information, see [Close a security incident](close-sir-incident-aiagent.md).

</td></tr></tbody>
</table>
