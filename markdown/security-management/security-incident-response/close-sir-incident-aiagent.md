---
title: Close a security incident
description: Use the Wrap up security incident agentic workflow in the ServiceNow Otto panel to cancel open response tasks, generate close notes and post-incident analysis, and close a security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/close-sir-incident-aiagent.html
release: brazil
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 3
keywords: [AI Agents, agentic AI]
breadcrumb: [Close security incidents, Use agentic workflows, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Close a security incident

Use the Wrap up security incident agentic workflow in the ServiceNow Otto panel to cancel open response tasks, generate close notes and post-incident analysis, and close a security incident.

## Before you begin

Role required: sn\_si.analyst or sn\_si.manager

## About this task

**Important:** This agentic workflow is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

You can't use this agentic workflow to close a security incident that's in the Closed or Cancelled state. If you request a closure for such a security incident, the AI agent informs you and takes no action.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace**.

2.  Open the security incident that you want to close by using the AI agent.

3.  In the header, select the ServiceNow Otto icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: AI Sparkle icon.\).

4.  In the ServiceNow Otto panel, enter the closure request for the type of closure that you want.

    |Option|Description|
    |------|-----------|
    |**Close the security incident with generated closure details**|Enter `Close this incident`, `Close this security incident`, or `Close the security incident: SIR0012345`.|
    |**Close the security incident as a false positive**|Enter `Close this incident as false positive` or `Close this security incident as false positive`.|

    If you enter `Close this incident` or `Close this security incident`, the AI agent uses the security incident that's open. If no security incident is open, include the security incident number in your request.

5.  If the AI agent warns that the security incident has open response tasks or mandatory assessments, select **Yes** to continue with the closure.

    When it closes the security incident, the AI agent cancels the open response tasks and ignores any mandatory assessments. Nothing changes on the security incident or its tasks until the closure is complete. If you want to keep the response tasks, select **No** and close the tasks manually before you request the closure.

6.  If you're closing the security incident with generated closure details, review the post-incident analysis and close notes that the AI agent generates, and then select **Approve**.

    If you want to change the content, select **Revise** and describe the changes, or paste the exact wording that you want. The AI agent shows the revised content and asks for your approval again.

    If the AI agent can't generate the post-incident analysis, it informs you. You can approve the closure without a post-incident analysis, or select **Revise** and enter the post-incident analysis that you want to save. If the AI agent can't generate the close notes, it asks you to provide them.

7.  If you're closing the security incident with generated closure details, accept the close code that the AI agent suggests or choose a different close code.

    The AI agent suggests a close code based on the security incident details, post-incident analysis, and close notes. Depending on how the AI agent presents the suggestion, select **Approve** or select the suggested close code to accept it. To use a different close code, select **Revise** and name the close code, or select it from the list. After you accept a close code, the AI agent closes the security incident without asking for further confirmation.

8.  If you're closing the security incident as a false positive, confirm the closure by selecting **Yes**.

    The AI agent shows a summary of the security incident before it asks you to confirm the closure.


## Result

-   The security incident is in the Closed state.
-   The open response tasks are in the Cancelled state.
-   For a closure with generated closure details, the **Close notes**, **Close code**, and **Post-incident analysis** fields contain the content that you approved. The **Post-incident analysis** field is empty if you approved the closure without it.
-   For a false-positive closure, the **Close notes** field is set to `Closed by AI Agent as false positive.` and the **Close code** field is set to **False positive**.
-   The panel shows a summary of the actions that the AI agent completed.
-   The activity stream records the changes as AI entries made on behalf of your user, for example, `Security incident closed.`

**Parent Topic:**[Close security incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/now-assist-sir-close-incident-usecase.md)

