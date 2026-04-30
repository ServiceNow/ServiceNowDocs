---
title: Close a security incident
description: Chat with an AI agent in the Now Assist panel to help you close a security incident.
locale: en-US
release: xanadu
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2025-02-25"
reading_time_minutes: 2
keywords: [AI Agents, agentic AI]
breadcrumb: [Security Incident Response AI agent collection close security incident use case, Using AI agentic workflows in Now Assist for Security Incident Response, Now Assist for Security Incident Response, Security Operations]
---

# Close a security incident

Chat with an AI agent in the Now Assist panel to help you close a security incident.

## Before you begin

Role required: sn\_si.analyst or sn\_si.manager

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace**.

2.  Open the security incident that you want to close by using the AI agent.

3.  Select the Now Assist \(![Now assist panel for AI agent icon.](../image/ai-icon-now-assist.png)\) icon.

    The Now Assist panel is displayed.

4.  Close the security incident by using one of the following options.

<table id="choicetable_ytr_35h_m2c"><thead><tr><th align="left" id="d36783e112">

Option

</th><th align="left" id="d36783e115">

Description

</th></tr></thead><tbody><tr><td id="d36783e121">

**Close a security incident**

</td><td>

On the Now Assist panel, ask the agent to close the security incident in natural language by entering `Close this incident`, `Close this security incident` or `Close the security incident: SIR0012345`. **Note:**

-   When you enter `Close this incident` or `Close this security incident`, the Now Assist panel picks the security incident in context. When you provide a specific security incident number, such as `Close the security incident: SIR0012345`, the use case takes action for the suggested security incident.
-   You can close any security incident from the Now Assist panel by providing the security incident number in your text.
-   When you request a security incident closure, the Close security incident use case cancels the mandatory post incident assessment, flow actions, playbook actions, workflow actions, and response tasks. However, you can close actions manually before initiating the security incident closure request.
 The Close security incident use case provides content for each of the following fields and asks for your feedback. The use case populates your accepted feedback. After you accept the content for a field, the use case provides content for the next field.

-   **Post Incident Analysis**: You can accept the suggested content by replying with a positive response such as `looks good` or `Ok`.

You can ask the use case to refine the content and can also suggest the changes you require.

-   **Close notes**: You can accept the suggested content by replying with a positive response such as `looks good` or `Ok`.

You can ask the use case to refine the content and can also suggest the changes you require.

-   **Close code**: On the basis of the security incident details, the use case suggests a close code. You can accept the close code or suggest an alternative close code for the security incident.
The AI agent closes the security incident.

**Note:** When a field is changed, the activity stream appends the words "AI AGENT:" with a description of the update made by the AI agent. For example, `AI AGENT: Close code is updated`.

</td></tr><tr><td id="d36783e224">

**Close a security incident as false positive**

</td><td>

On the Now Assist panel, you can ask the AI agent to close the security incident as false positive. For example, `Close this incident as false positive` or `close this security incident as false positive`.The use case provides the summary of the security incident. To close the security incident, type in positive responses such as `looks good` or `Ok`.

The AI agent closes the security incident. It also updates the Close notes as `Closed by AI Agent as false positive` and the Close code as **False positive** and cancels all active response tasks.

</td></tr></tbody>
</table>
