---
title: AIOps AI Specialist
description: The AIOps Manager can create, configure, and manage an AI specialist. AI specialist is an AI-powered team member \(not human\) that works alongside your operators, handling routine alert triage so your people can focus on what requires human judgment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/ai-specialist-aiops-overview.html
release: australia
topic_type: concept
last_updated: "2026-11-01"
reading_time_minutes: 7
keywords: [AI specialist, AIOps, overview]
breadcrumb: [ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# AIOps AI Specialist

The AIOps Manager can create, configure, and manage an AI specialist. AI specialist is an AI-powered team member \(not human\) that works alongside your operators, handling routine alert triage so your people can focus on what requires human judgment.

The AIOps AI Specialist is an AI team member that takes the first pass on every in-scope alert. It triages the alert, reduces noise, identifies the likely cause, maps the impact, and suggests a next step.

Your operators review the findings and make the final decision. Nothing changes in your environment until an operator approves it.

## The problem it solves

Operations teams often lose time before they can fix anything. Alerts arrive faster than operators can read them, and real problems can hide in the noise.

Each investigation also means switching between monitoring tools, the CMDB, knowledge articles, and change records. Every minute spent gathering context adds to resolution time.

## What the specialist is

The specialist is onboarded the way you would onboard a new operator. It has a name, a team assignment, and the Operator role \(evt\_mgmt\_operator\). It works on the alerts that match the scope you define.

The specialist is deliberately limited. It cannot change team configurations, create other specialists, or modify system settings.

## Value to your team

The specialist moves the slowest part of an investigation, gathering context, from operators to the AI.

Benefits your team will notice

-   A queue that matches the work. Noise leaves the queue, so operators see the alerts that need judgment first.
-   Faster, more consistent investigations. Every in-scope alert gets the same checks, at any hour, on every shift.
-   Less tool switching. Telemetry, changes, knowledge and service data arrive in one summary.
-   Easier handoffs. Findings are written to the alert, so the next person does not start from zero.
-   Growth without extra hiring. The specialist absorbs rising alert volume, and operators spend their time on work that needs people.
-   Trust you can inspect. The AI Specialist records the reason for closing an alert, and the supervisor can choose to reopen it.

|Value|What changes for your team|
|-----|--------------------------|
|Alert deflection|Insignificant alerts close before an operator opens them. The queue holds the alerts that need judgment.|
|Faster resolution|Root cause, impact, and next steps are ready when an operator opens the alert.|
|Lower cost per alert|Routine triage and investigation run automatically, which reduces manual effort.|
|Capacity|The specialist absorbs alert growth, so operators spend more time on work that needs people.|

**Note:** Time-saved figures are estimates. They multiply the alerts that the specialist closes and analyzes by the minutes that you configure for each.

## What the AIOps specialist does

Each capability is a task module that you can turn on or off.

|Capability|What the specialist does|Task module|Operator action|
|----------|------------------------|-----------|---------------|
|Triage|Checks each alert against the scope conditions and assigns matching alerts to its queue.|Scoping|None, automatic|
|Noise reduction|Closes alerts that history or service impact shows need no action.|Noise reduction|Review closed alerts|
|Root cause analysis|Names a probable cause, with supporting evidence from related alerts, recent changes, and knowledge articles.|Investigation|Review findings|
|Impact analysis|Maps the alert to affected service instances, service offerings, and technical business services.|Investigation|Review findings|
|Knowledge lookup|Reads the knowledge bases that you select, so the investigation uses your playbooks and history.|Investigation|Review references|
|Remediation suggestions|Finds automation that is available as alert management rules and ranks the best actions.|Remediation|Activate the action|

## Specialist monitoring and value per role

The AIOps Manager \[evt\_aiops\_manager\] can create the AIOps specialist in Service Operations Workspace.

<table id="table_s4v_hkb_clc"><thead><tr><th>

Role

</th><th>

Role system name

</th><th>

What they do with the specialist

</th><th>

What they gain

</th></tr></thead><tbody><tr><td>

Admin

</td><td>

evt\_mgmt\_admin

</td><td>

-   Onboards and configures, tests, activates and deactivates the specialist.
-   Reviews metrics for all teams.

</td><td>

One place to prove impact and control scope.

</td></tr><tr><td>

AIOps manager

</td><td>

evt\_aiops\_manager

</td><td>

-   Creates, configures and tunes the specialist for the teams they run.
-   View metrics for the teams they manage

</td><td>

Control over what the AI handles, and proof it is working.

</td></tr><tr><td>

Operator or supervisor

</td><td>

evt\_mgmt\_operator

</td><td>

Reviews AI findings, checks closed alerts, activates remediations, handles only what needs a person.

</td><td>

A shorter queue and a head start on every alert that remains.

</td></tr></tbody>
</table>## Operator control

The specialist does the investigation. Your operators keep the decisions.

-   Fixed role. The specialist cannot change team configurations, create specialists, or modify system settings.

-   Defined scope. The specialist works only on alerts that match every active scope condition.

-   Visible work. Every action is logged on the alert. Operators can review closed alerts and reopen them.

-   Evidence behind closures. It closes an alert only when history, knowledge or service impact supports closing it. Otherwise, the alert stays open with the findings attached.
-   Staged autonomy. Noise reduction and remediation are separate settings, so you can grant autonomy one step at a time.

-   An operator must activate every remediation.

## How the specialist works

The specialist follows the same path on every alert. It checks the scope, investigates, decides whether to close, ranks a fix, and hands the result to a person. Every alert follows one path, and a person take the last step.

|Decision|Rule|What it protects|
|--------|----|----------------|
|In scope?|The alert must match every scope condition.|The AI works only on alert types it handles well. Everything else goes to operators.|
|Outcome?|An insignificant alert can be auto-closed when noise reduction is on. An error leaves the alert open. Anything else continues.|A failure never hides an alert.|
|Close or keep open?|It closes only when the evidence supports closing, and it cites that evidence. Otherwise, it keeps the alert open and says why.|No silent deflection.|
|Rank fixes|Runs only when **Suggest remediation** is on and linked automation exists. It ranks. It never runs.|No change to your environment without a person.|
|Final step|Every run ends the same way: findings written, state updated, run logged.|No alert is left half-handled.|

\[Omitted image "aiops-specialist-workflow.png"\] Alt text: The AIOps AI Specialist workflow from alert arrival to remediation suggestion

## How it decides to close an alert

The specialist closes an alert for one of two reasons, and both leave a record.

-   It is noise. Historical alerts have repeatedly resolved without action, or the alert has no meaningful effect on a service. Alerts that tend to be closed without human action, without escalation, or that follow a consistent trend tend to be noisy alerts.

-   The evidence says it is expected. The verification step gathers knowledge articles, related incidents, earlier AI insights and up to ten recent work notes. It then checks them against the alert.


For example, a knowledge article states that brief frame loss during a routing reconvergence is expected and clears on its own. The alert matches the device and the time window and shows no error counters. The specialist closes it and cites the article.

The specialist is just as careful in the other direction. If a known pattern almost fits, such as a nightly batch article for a different host, it keeps the alert open. It states exactly why the article does not apply.

## What it records

-   An insight on the alert. Overview, what is affected, probable cause, who should look, and the next step.

-   A work note summary. The AI summary is appended to the alert's work notes.

-   An investigation report. A sanitized report is stored on the alert.

-   Live processing steps. Progress labels, for example, `Analyzing alert` and `Summarizing impact`, show what is happening.

-   Activity stream entries. Each closure is logged so supervisors can review it.

-   A run record. One record per run with its objective, start and end time, duration, state and the full conversation, as an audit trail.


## Prerequisites

-   Platform version Brazil Patch 2 or later.
-   ServiceNow Otto for IT Operations Management \(ITOM\) application, version 2.10.0 or later.
-   AIOps Experience application, version 27.2.68 or later.
-   AIOps AI Specialist \(sn\_ai\_aiops\_force\) plugin, version 3.0.0 or later.

## Known limitation

Each instance supports only one AIOps AI Specialist. Your organization can use only one AI Specialist for AIOps.

## Domain separation support for AIOps AI Specialist

AIOps AI Specialist isn't supported on domain-separated instances. Only one AIOps AI Specialist can be active, so you can't set up a separate AI specialist with its own configuration for each domain.

-   **[AIOps AI Specialist use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/aiops-specialist-use-cases.md)**  
Three scenarios show how teams typically use the AIOps AI Specialist to reduce noise, speed up investigations, and turn runbooks into fixes.
-   **[Onboard the AIOps specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/onboard-ai-specialist.md)**  
Add the AIOps specialist to your team so it can start receiving and acting on alerts by assigning it a name, a role, and one or more teams.
-   **[Deactivate the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/deactivate-ai-specialist.md)**  
Deactivate the AIOps specialist to pause all its operations. Your configuration is preserved and you can reactivate it at any time.
-   **[Manage the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/manage-the-ai-specialist.md)**  
Use the AIOps home page to view and manage the alerts assigned to the AIOps AI Specialist. This page is the default home page of the Service Operations Workspace. Which view you see depends on your role.

**Parent Topic:**[ITOM AIOps specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/now-assist-itom-specialists.md)

**Previous topic:**[ITOM AIOps specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/now-assist-itom-specialists.md)

**Next topic:**[AIOps AI Specialist use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/aiops-specialist-use-cases.md)

**Related topics**  


[Autonomous Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-workforce.md)

[AI specialists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-ai-specialist.md)

