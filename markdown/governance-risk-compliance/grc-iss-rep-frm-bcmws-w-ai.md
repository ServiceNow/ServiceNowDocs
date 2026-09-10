---
title: Reporting an issue from Business Continuity Workspace
description: Report compliance gaps and control deficiencies by associating issues with plans or events in Business Continuity Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-iss-rep-frm-bcmws-w-ai.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [GRC, business continuity, issue tracking, compliance, Otto AI]
breadcrumb: [Managing issues from Business Continuity Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Reporting an issue from Business Continuity Workspace

Report compliance gaps and control deficiencies by associating issues with plans or events in Business Continuity Workspace.

During business continuity management \(BCM\) events, teams often identify gaps between documented controls and actual operations. GRC issue reporting formalizes these findings into actionable work items that your compliance team can track, analyze, and resolve.

## How issue reporting works

When you discover a control deficiency, non-compliance, or gap during a BCM event, you can report it directly using ServiceNow Otto for IRM AI-guided workflows. ServiceNow Otto for IRM prompts you for essential context and automatically performs the following tasks:

-   Classifies the issue by risk severity
-   Assigns it to the compliance team
-   Tracks its progress through analysis, response, review, and closure

## Roles required for reporting issues in a BCM instance

BCM viewers \(sn\_bcm.viewer\) and managers \(sn\_bcm.manager\) with the sn\_grc\_genai.issue\_aiagent\_user role can invoke issue AI agents.

## Why report issues

Structured issue reporting creates an audit trail that demonstrates your organization's commitment to governance and continuous control improvement. It also prevents compliance gaps from going unaddressed and helps leadership understand risk exposure across business units.

## Issue workflow states

Each reported issue progresses through a five-stage workflow:

-   New: Issue submitted and awaiting triage
-   Analyze: Compliance team validates scope and risk rating
-   Respond: Remediation actions assigned and tracked
-   Review: Completion and control effectiveness verified
-   Closed: Issue resolved and approved for closure

\[Omitted image "ai-issue-not-classified-as-bcm.png"\] Alt text: Issue reported showing a classification and an issue source of Ad-Hoc.

If the issue relates to business continuity, update the **Classification** field on the issue to **Business continuity management**, and link the issue to the relevant plan, event, or exercise manually. For the steps, see [Add or create an issue from a plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-or-create-issue-from-plan-uib-ws.md) or [Add or create an issue from an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-or-create-issue-from-event-uib-ws.md).

An issue that you report through ServiceNow Otto for IRM isn't automatically classified as a BCM issue, and isn't automatically linked to the plan, event, or exercise it relates to. ServiceNow Otto for IRM classifies the issue based on the description you provide and marks the issue source as **Ad-Hoc**.

**Related topics**  


[Report an issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/report-grc-issue-frm-plan.md)

[Managing issues from Business Continuity Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/managing-issues-in-bcm.md)

[Add or create an issue from a plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-or-create-issue-from-plan-uib-ws.md)

[Add or create an issue from an exercise](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/add-or-create-issue-from-event-uib-ws.md)

