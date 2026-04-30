---
title: Add security incident to shift handover report
description: Chat with an AI agent in the Now Assist panel to add a security incident details to a shift handover report.
locale: en-US
release: yokohama
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2025-08-21"
reading_time_minutes: 2
breadcrumb: [Generate SIR Shift Handover Report, Use agentic workflows, Now Assist for Security Incident Response, Security Operations]
---

# Add security incident to shift handover report

Chat with an AI agent in the Now Assist panel to add a security incident details to a shift handover report.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace**.

2.  Open the security incident that you want to add to a shift handover report using the AI agent.

3.  Select the Now Assist \(![Now Assist panel for AI agent icon.](../image/ai-icon-now-assist.png)\) icon.

    The Generate SIR Shift Handover Report agentic workflow is on-demand. You can enter a query in natural language to add a security incident to a shift handover report.

4.  On the Now Assist panel, ask the agent to add a security incident to a shift handover report `Add this security incident to shift handover`, or `Add this incident to shift handover: SIR0012345` and press the Enter key.

    The Now Assist panel triggers the "Add Security Incident for Shift Handover" workflow. This workflow fetches details of the security incident.

    The AI agent finds the in-progress shift handover record that the analyst has access to and adds the security incident details to it. If there are multiple in-progress shift handover records to which the analyst has access, the AI agent lists the top five shift handover records for the analyst to select.

    If there are no shift handover records in the "progress" state and assigned to the user’s group, or there are no shift handover records, then a notification message is displayed stating that there are no active shift handover records for the user.

5.  Provide the shift handover record number and press the Enter key.

    The AI agent validates the shift handover record to identify if the record is valid and in progress, the logged in analyst has access to the shift handover record. On a successful validation, the AI agent generates the content for the shift handover record and provides it for approval.

6.  Enter positive responses such as `looks good`, `approved`, or `Ok` if you agree to the content.

    The AI agent saves the approved content to the relevant section of the shift handover report.

    For each section of the shift handover report, the AI agent provides the content and requests feedback from the analyst. If required, you can skip to update any section.

    ![Content added to shift handover report.](../image/NA-shift-handover.png)


## Result

The AI agent displays the summary of all the updated and skipped sections.

![Shift handover wrokflow result](../image/shifthandover-report-update.png)

