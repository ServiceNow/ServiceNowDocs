---
title: Scenario analysis entry points and flow configuration
description: Starting with Operational Resilience, version 22.3.1, the advanced scenario analysis flow \(sn\_oper\_res\_scenario\_analysis\_advance\) replaces the legacy scenario analysis flow \(sn\_oper\_res\_scenario\_analysis\) across different entry-point surfaces in the Operational Resilience Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/scenario-analysis-entry-points.html
release: australia
topic_type: concept
last_updated: "2026-05-14"
reading_time_minutes: 4
keywords: [Scenario Analysis, Operational Resilience, entry points, legacy flow, advanced flow, sn\_oper\_res\_scenario\_analysis\_advance, sn\_oper\_res\_scenario\_analysis]
breadcrumb: [Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Scenario analysis entry points and flow configuration

Starting with Operational Resilience, version 22.3.1, the advanced scenario analysis flow \(sn\_oper\_res\_scenario\_analysis\_advance\) replaces the legacy scenario analysis flow \(sn\_oper\_res\_scenario\_analysis\) across different entry-point surfaces in the Operational Resilience Workspace.

The advanced scenario analysis flow is enabled by default in the Operational Resilience Workspace. The legacy flow remains in the platform but is hidden from the four entry-point surfaces described in this topic. If your organization needs to continue using the legacy flow, an administrator can reactivate it on each surface.

**Note:** Administrator \(admin\) access is required to make the configuration changes described in this topic. Only one flow \(advanced or legacy\) must be active at a time on each surface.

## Entry points

The advanced scenario analysis flow is active by default on these entry points:

-   Scenario analysis \(legacy\) UX list record
-   Scenario analysis widget in the Home page
-   Vertical page layout
-   Source field on the Operational vulnerability record

To enable the legacy flow on any of these entry points, see [Enable the legacy scenario analysis flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/activate-scenario-analysis-legacy-flow.md).

## Scenario analysis list

The **Scenario analysis** list is rendered by a sys\_ux\_list record as shown in the example.

\[Omitted image "sca-ux-list.png"\] Alt text: sys\_ux\_list records.

The All scenario analysis is active by default. It sources records from the \[sn\_oper\_res\_scenario\_analysis\_advance\] table. The Scenario analysis \(Legacy\) is inactive and it sources records from the \[sn\_oper\_res\_scenario\_analysis\] table.

## Home page widget

The Operational Resilience Home page shows a progress widget summarizing scenario analysis status. Starting with Operational Resilience, version 22.3.1, by default, the scenario\_analysis\_progress \(advanced flow\) is visible and the scenario\_analysis\_legacy\_progress \(legacy flow\) is hidden.

The Data visualization report states are shown in the table.

|Report|State|
|------|-----|
|Scenario analysis in progress|Active|
|Scenario analysis completed|Active|
|Scenario analysis \(legacy\) in progress|Inactive|
|Scenario analysis \(legacy\) completed|Inactive|

|UI Component|Description|
|------------|-----------|
|scenario\_analysis\_progress|Widget that displays progress data for the advanced scenario analysis flow. It is visible on the Operational Resilience Home page by default.|
|Data visualization reports \(advanced flow\)|Two report records that source the **scenario\_analysis\_progress** widget. It is Active by default.|
|scenario\_analysis\_legacy\_progress|Widget that displays progress data for the legacy scenario analysis flow. It is hidden on the Operational Resilience Home page by default.|
|Data visualization reports \(legacy flow\)|Two report records that source the **scenario\_analysis\_legacy\_progress** widget. It is Inactive by default.|

## Vertical page layout

The Vertical page layout controls the Program Activities related list shown on Business Service, Service, and Offering records. Version 22.3.1 activates the related list pointing to the advanced flow and deactivates the one pointing to the legacy flow.

**Note:** The related lists display different columns. The advanced list shows limited columns; the legacy list includes additional columns such as State distribution and Impact tolerance.

|UI Component|Description|
|------------|-----------|
|**Program Activities** \(advanced\)|Related list that surfaces records from the **sn\_oper\_res\_scenario\_analysis\_advance** table on the Business Service, Service, and Offering records. It is active by default.|
|**Program Activities** \(legacy\)|Related list that surfaces records from the **sn\_oper\_res\_scenario\_analysis** table on the Business Service, Service, and Offering records. It is inactive by default.|

## Operational vulnerability Source field

The **Source** field \(**sn\_oper\_res\_vulnerability.source**\) on the Operational vulnerability record identifies where a vulnerability originated. The list has multiple choices; this release toggles only the two Scenario analysis entries.

When configured for the legacy flow, the Source drop-down on an Operational vulnerability record displays **Scenario analysis \(legacy\)** instead of Scenario analysis.

|UI Component|Description|
|------------|-----------|
|**Scenario analysis**|Choice that links a vulnerability to the advanced scenario analysis flow. Active by default on the **sn\_oper\_res\_vulnerability.source** list.|
|**Scenario analysis \(legacy\)**|Choice that links a vulnerability to the legacy scenario analysis flow. Inactive by default on the **sn\_oper\_res\_vulnerability.source** list.|

## Default flow

The advanced scenario analysis flow is active across all four entry points by default. For information on building an advanced scenario analysis using simulation or manual method, see [Building a scenario analysis using simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/scenario-analysis-playbook-experience.md). For legacy scenario analysis, see [Legacy scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/legacy-scenario-analysis-ov.md).

To enable the legacy scenario analysis, see [Enable the legacy scenario analysis flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/activate-scenario-analysis-legacy-flow.md).

