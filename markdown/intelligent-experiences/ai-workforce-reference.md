---
title: Reference for Autonomous Workforce
description: Reference for Autonomous Workforce provides additional information about the roles and performance metrics associated with AI specialists.The AI Specialist Manager role enables editing, testing, and monitoring AI specialists in AI Agent Studio and Service Operations Workspace.Performance metrics in AI Agent Studio track how an AI specialist routes, resolves, and communicates on incidents. Use them to find where an AI specialist needs tuning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-workforce-reference.html
release: australia
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 4
keywords: [ai specialist reference, ai specialist roles, ai specialist metrics, AI specialist role, AI specialist performance, AI specialist metrics, ai specialist auto-resolve rate, ai specialist coverage rate, ai specialist KB article usage]
breadcrumb: [Autonomous Workforce, AI Agent Studio \(legacy\), AI agents and agentic workflows, Enable AI Experiences]
---

# Reference for Autonomous Workforce

Reference for Autonomous Workforce provides additional information about the roles and performance metrics associated with AI specialists.

## AI Specialist Manager role

The AI Specialist Manager role enables editing, testing, and monitoring AI specialists in AI Agent Studio and Service Operations Workspace.

### Contains Roles

List of roles contained within the role.

-   sn\_aia.viewer
-   skill\_manager

## AI specialist performance metrics

Performance metrics in AI Agent Studio track how an AI specialist routes, resolves, and communicates on incidents. Use them to find where an AI specialist needs tuning.

You can filter all performance metrics by date and assignment group.

### Overview metrics

|Group|Metric|Description|
|-----|------|-----------|
|At a glance|Durable auto-resolve rate \(%\)|Percentage of incidents that the AI specialist resolved without reassigning to a human agent and that weren't reopened.|
|At a glance|Coverage rate \(%\)|Percentage of assigned incidents that the AI specialist attempted to resolve.|
|Routing journey|1. Closed incidents in eligible assignment group\(s\)|All closed incidents in the assignment groups that the AI specialist belongs to.|
|Routing journey|2. Closed incidents assigned to AI specialist|Incidents assigned to the AI specialist for triage through assignment rules or AWA.|
|Routing journey|3. Closed incidents attempted by AI specialist|Incidents where the AI specialist was confident enough to propose a solution or take autonomous action.|
|Incident outcomes|All incident outcomes|Percentage and count of each outcome of the AI specialist's attempts: resolved, reassigned to a human agent, reopened, generated a new ticket, or in progress.|
|Incident outcomes|Incident outcomes over time|Trend of the AI specialist's incident outcomes.|
|Resolution details|Mean time to resolution|Average time between an incident being assigned to the AI specialist and the generation of a response that was later accepted.|
|Resolution details|Mean time to first response|Average time between an incident being assigned to the AI specialist and the generation of its first response.|
|Reassignment reasons|Reasons for reassignment|Percentage and count of incidents reassigned to a human agent, broken down by cause.|
|Reassignment reasons|Reasons for reassignment over time|Trend of reassignments to a human agent, broken down by cause.|
|Follow-ups|Follow up rate \(%\)|Percentage of attempted incidents where the AI specialist needed to ask the requester for more information.|
|Follow-ups|Count of incidents that required a follow up|Number of incidents that required at least one additional message from the AI specialist.|

### Quality metrics

|Metric|Description|
|------|-----------|
|Assessments for closed incidents|Quality assessments generated for completed AI specialist tasks.|
|Quality score trend|Trend of quality scores based on assessments.|
|All opportunities|Coaching opportunities identified for the AI specialist.|

### Detailed view metrics

|Group|Metric|Description|
|-----|------|-----------|
|AI-handled incidents by service|Incident outcomes \(%\) by service|Percentage of each outcome of the AI specialist's attempts \(resolved, reassigned, new, and reopened\), broken down by service.|
|AI-handled incidents by service|Incident outcomes by service|Count of each AI specialist outcome, broken down by service. Selecting a number in the Count field opens the ZTSD Task Execution list filtered by that service and outcome.|
|AI-handled incidents by service|Reassignment reasons for unresolved incidents by service|Percentage and count of incidents reassigned to a human agent, broken down by cause and service.|
|AI-handled incidents by service|Average exchanges for resolved incidents by service|Average number of AI specialist responses before a final outcome, for each service.|
|Proposed solution similarity by service|Average proposed solution similarity by service|Average AI judge score comparing the AI specialist's proposed solutions with the final resolutions, for each service.|

### Value and feedback metrics

|Metric|Description|
|------|-----------|
|Aggregated sentiment analysis|Overall tone, from negative to positive, of user messages in incidents handled by the AI specialist.|
|Adoption coverage|Number of relevant assignment groups that have used the AI specialist to handle incidents.|
|Direct user feedback|Chart of the feedback that requesters gave on incidents the AI specialist resolved.|

### KB article metrics

|Group|Metric|Description|
|-----|------|-----------|
|KB article usage summary|KB articles used|Number of distinct KB articles the AI specialist referenced during the selected period.|
|KB article usage summary|Total records|Number of records, such as incidents, problems, and interactions, resolved using at least one retrieved KB article.|
|KB article usage summary|Shown in citations|KB articles that the AI specialist included in a response to the user. A higher count suggests that the AI specialist is surfacing relevant content.|
|KB article usage summary|Retrieved only|KB articles that the AI specialist retrieved but didn't include in a response. A high count can indicate retrieval quality issues.|
|KB article usage summary|Unused articles|KB articles that weren't retrieved or cited during the selected period. Review these to find outdated or hard-to-discover content.|
|KB article list|All used articles|List of KB articles the AI specialist used, with usage frequency \(how often each article was cited after retrieval\) and reopen rate \(percentage of incidents resolved using the article that were later reopened\).|
|KB article list|Unused articles|List of KB articles with no references during the selected period.|

