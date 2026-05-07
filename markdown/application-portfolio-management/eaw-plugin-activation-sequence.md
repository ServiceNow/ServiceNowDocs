---
title: Application plugin installation sequence for Enterprise Architecture Workspace
description: The following table provides the list of plugins for Enterprise Architecture Workspace, a high-level description of each plugin, and the dependencies that are required before installing each plugin.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-23"
reading_time_minutes: 6
breadcrumb: [Install Enterprise Architecture Workspace, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Application plugin installation sequence for Enterprise Architecture Workspace

The following table provides the list of plugins for Enterprise Architecture Workspace, a high-level description of each plugin, and the dependencies that are required before installing each plugin.

**Warning:** type="warning"&gt;Before activating a plugin listed in the Plugin name column, verify that you activate all corresponding dependencies listed in the Plugin dependencies column from the [ServiceNow Store](https://store.servicenow.com).

## Enterprise Architecture Workspace application plugin list

When you activate Enterprise Architecture Workspace \(`com.snc.apm_workspace`\), ServiceNow automatically activates several dependent plugins. These are listed as **Automatic** in the Activation column. The remaining plugins must be activated manually in the order shown in the [Enterprise Architecture Workspace plugin activation sequence](eaw-plugin-activation-sequence.md#install_sequence) section.

**Tip:** The auto-activated plugin list may vary depending on your instance version. To confirm the exact dependencies for your version, check the Plugin Manager before activation.

<table id="table_ys3_v1g_1jc"><thead><tr><th>

Sequence

</th><th>

Plugin name

</th><th>

Description

</th><th>

Activation

</th><th>

Plugin dependencies

</th></tr></thead><tbody><tr><td>

1

</td><td>

Enterprise Architecture Core

 `[com.snc.apm_core]`

</td><td>

Provides the core data model and foundation tables for Enterprise Architecture.

</td><td>

Automatic

</td><td>

—

</td></tr><tr><td>

2

</td><td>

Enterprise Architecture

 `[com.snc.apm]`

</td><td>

Provides application portfolio management capabilities for tracking business applications, capabilities, and services. All other EA plugins depend on this plugin.

</td><td>

Automatic

</td><td>

Enterprise Architecture Core \(`com.snc.apm_core`\)

</td></tr><tr><td>

3

</td><td>

Read-only Roles for EA

 `[com.snc.apm_read_roles]`

</td><td>

Provides read-only access roles for Enterprise Architecture data and records. Activate this plugin before activating Enterprise Architecture Workspace.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\)

</td></tr><tr><td>

4

</td><td>

Four-Quadrant Bubble Chart

 `[sn_4_q_bubble]`

</td><td>

Provides the bubble chart visualization component used in EA Workspace rationalization views.

</td><td>

Automatic

</td><td>

—

</td></tr><tr><td>

5

</td><td>

Enterprise Architecture Workspace

 `[com.snc.apm_workspace]`

</td><td>

Provides the primary workspace interface for Enterprise Architecture, including dashboards, rationalization views, and Now Assist. Activating this plugin triggers automatic activation of all dependent plugins.

</td><td>

Manual

</td><td>

Enterprise Architecture Core \(`com.snc.apm_core`\), Enterprise Architecture \(`com.snc.apm`\), Read-only Roles for EA \(`com.snc.apm_read_roles`\), Four-Quadrant Bubble Chart \(`sn_4_q_bubble`\)

</td></tr><tr><td>

6

</td><td>

Value Stream

 `[sn_value_stream]`

</td><td>

Provides value stream integration capabilities for mapping business value flows within Enterprise Architecture.

</td><td>

Automatic

</td><td>

Enterprise Architecture Workspace \(`com.snc.apm_workspace`\)

</td></tr><tr><td>

7

</td><td>

Product Capability Core

 `[sn_prod_cap_core]`

</td><td>

Provides product capability mapping components used within Enterprise Architecture Workspace.

</td><td>

Automatic

</td><td>

Enterprise Architecture Workspace \(`com.snc.apm_workspace`\)

</td></tr><tr><td>

8

</td><td>

Enterprise Architecture – TRM

 `[com.snc.apm_trm]`

</td><td>

Provides Technology Reference Model capabilities for tracking and managing the technology landscape across the enterprise.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\)

</td></tr><tr><td>

9

</td><td>

Technology Portfolio Management

 `[com.snc.apm_tpm]`

</td><td>

Provides technology lifecycle management, software model mapping, and capability scoring for enterprise applications.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\), Enterprise Architecture – TRM \(`com.snc.apm_trm`\)

</td></tr><tr><td>

10

</td><td>

Total Cost of Ownership

 `[com.snc.apm_tco]`

</td><td>

Provides cost tracking and reporting for enterprise applications.

</td><td>

Automatic

</td><td>

Enterprise Architecture \(`com.snc.apm`\)

</td></tr><tr><td>

11

</td><td>

Digital Integration Management

 `[com.snc.apm_digital_integration]`

</td><td>

Provides digital integration and interface management capabilities, including entity shapes for architecture diagrams. This plugin activates automatically, but must be active before Enterprise Modeling Common activates for diagram entity shapes to load correctly.

</td><td>

Automatic

</td><td>

Enterprise Architecture \(`com.snc.apm`\)

</td></tr><tr><td>

12

</td><td>

Cloud Readiness Assessment

 `[com.snc.apm_cloud_readiness]`

</td><td>

Provides cloud readiness scoring and assessment capabilities for enterprise applications.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\)

</td></tr><tr><td>

13

</td><td>

Advanced Risk Management

 `[com.sn_risk_advanced]`

</td><td>

Provides advanced risk management capabilities. Required by Risk Assessment for EA.

</td><td>

Manual

</td><td>

—

</td></tr><tr><td>

14

</td><td>

Risk Assessment for EA

 `[com.snc.apm_risk_assessment]`

</td><td>

Provides risk assessment capabilities within the Enterprise Architecture context.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\), Advanced Risk Management \(`com.sn_risk_advanced`\)

</td></tr><tr><td>

15

</td><td>

Compliance

 `[com.sn_compliance]`

</td><td>

Provides compliance management capabilities. Required by Control Management for EA.

</td><td>

Manual

</td><td>

—

</td></tr><tr><td>

16

</td><td>

Control Management for EA

 `[com.snc.apm_control_management]`

</td><td>

Provides control management capabilities within the Enterprise Architecture context.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\), Compliance \(`com.sn_compliance`\)

</td></tr><tr><td>

17

</td><td>

APM Diagram Builder

 `[com.sn_apm_diagram_builder]`

</td><td>

Provides the diagram builder component used by Enterprise Modeling and Visualization.

</td><td>

Manual

</td><td>

Enterprise Architecture Workspace \(`com.snc.apm_workspace`\)

</td></tr><tr><td>

18

</td><td>

Enterprise Modeling Common

 `[com.snc.apm_modelling_tool_common]`

</td><td>

Provides the base data model and shared components for Enterprise Modeling and Visualization.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\), APM Diagram Builder \(`com.sn_apm_diagram_builder`\)

</td></tr><tr><td>

19

</td><td>

Enterprise Modeling and Visualization

 `[com.snc.apm_modelling_tool]`

</td><td>

Provides capabilities for creating and managing architecture diagrams, including EA entity shapes and relationships.

</td><td>

Manual

</td><td>

Enterprise Architecture Workspace \(`com.snc.apm_workspace`\), APM Diagram Builder \(`com.sn_apm_diagram_builder`\), Enterprise Modeling Common \(`com.snc.apm_modelling_tool_common`\)

</td></tr><tr><td>

20

</td><td>

PA for APM

 `[com.snc.pa.apm]`

</td><td>

Provides Performance Analytics content packs for EA dashboards and reporting.

</td><td>

Automatic

</td><td>

Enterprise Architecture \(`com.snc.apm`\)

</td></tr><tr><td>

21

</td><td>

PPT Export for EA

 `[com.snc.apm_ppt_export]`

</td><td>

Provides PowerPoint export capabilities for EA diagrams and workspace content.

</td><td>

Manual

</td><td>

Enterprise Architecture Workspace \(`com.snc.apm_workspace`\)

</td></tr><tr><td>

22

</td><td>

Lucidchart Integration

 `[com.snc.sn_lucidchart_integration]`

</td><td>

Provides integration with Lucidchart for collaborative diagram editing and import.

</td><td>

Manual

</td><td>

IntegrationHub

</td></tr><tr><td>

23

</td><td>

Lucidchart Diagramming Spoke \(IH\)

 `[com.sn.lucidchart.spoke]`

</td><td>

Provides IntegrationHub spoke actions for Lucidchart diagram operations in Flow Designer.

</td><td>

Manual

</td><td>

IntegrationHub, Lucidchart Integration \(`com.snc.sn_lucidchart_integration`\)

</td></tr><tr><td>

24

</td><td>

PA for APM – Change

 `[com.snc.pa.apm.change_request]`

</td><td>

Provides Performance Analytics content for change request tracking in EA dashboards.

</td><td>

Manual

</td><td>

PA for APM \(`com.snc.pa.apm`\)

</td></tr><tr><td>

25

</td><td>

PA for APM – Problem

 `[com.snc.pa.apm.problem]`

</td><td>

Provides Performance Analytics content for problem management in EA dashboards.

</td><td>

Manual

</td><td>

PA for APM \(`com.snc.pa.apm`\)

</td></tr><tr><td>

26

</td><td>

EA – Predictive Intelligence

 `[com.snc.apm.predictive_intelligence]`

</td><td>

Provides predictive intelligence capabilities for enterprise application analysis and recommendations.

</td><td>

Manual

</td><td>

Enterprise Architecture \(`com.snc.apm`\)

</td></tr></tbody>
</table>## Enterprise Architecture Workspace plugin activation sequence

To avoid missing features and activation issues, activate the manually activated plugins in the following sequence. Plugins marked as Automatic in the table earlier do not require manual activation.

1.  Read-only Roles for EA \(`com.snc.apm_read_roles`\)
2.  Enterprise Architecture Workspace \(`com.snc.apm_workspace`\)
3.  Enterprise Architecture – TRM \(`com.snc.apm_trm`\)
4.  Technology Portfolio Management \(`com.snc.apm_tpm`\)
5.  \(Optional\) Cloud Readiness Assessment \(`com.snc.apm_cloud_readiness`\)
6.  Advanced Risk Management \(`com.sn_risk_advanced`\)
7.  Risk Assessment for EA \(`com.snc.apm_risk_assessment`\)
8.  Compliance \(`com.sn_compliance`\)
9.  Control Management for EA \(`com.snc.apm_control_management`\)
10. APM Diagram Builder \(`com.sn_apm_diagram_builder`\)
11. Enterprise Modeling Common \(`com.snc.apm_modelling_tool_common`\)
12. Enterprise Modeling and Visualization \(`com.snc.apm_modelling_tool`\)
13. \(Optional\) PPT Export for EA \(`com.snc.apm_ppt_export`\)
14. \(Optional\) Lucidchart Integration \(`com.snc.sn_lucidchart_integration`\)
15. \(Optional\) Lucidchart Diagramming Spoke \(IH\) \(`com.sn.lucidchart.spoke`\)
16. \(Optional\) PA for APM – Change \(`com.snc.pa.apm.change_request`\)
17. \(Optional\) PA for APM – Problem \(`com.snc.pa.apm.problem`\)
18. \(Optional\) EA – Predictive Intelligence \(`com.snc.apm.predictive_intelligence`\)

## Resolving missing features

If a feature is missing after activation, check whether a required plugin was inactive when another plugin was activated. The following table lists common symptoms and how to resolve them.

|Symptom|Cause|Resolution|
|-------|-----|----------|
|Bubble Chart page is empty or missing|Four-Quadrant Bubble Chart was not active when EA Workspace was activated|Confirm `sn_4_q_bubble` is active, then reactivate `com.snc.apm_workspace`.|
|Risk Assessment menu missing in workspace|Advanced Risk Management was not active when Risk Assessment for EA was activated|Activate `com.sn_risk_advanced` first, then activate `com.snc.apm_risk_assessment`.|
|No entity shapes in Enterprise Modeling and Visualization|Enterprise Architecture was not active when Enterprise Modeling and Visualization was activated|Confirm `com.snc.apm` is active, then reactivate `com.snc.apm_modelling_tool`.|
|Lucidchart spoke actions missing in Flow Designer|IntegrationHub was not active before the Lucidchart spoke was activated|Activate IntegrationHub, then reactivate `com.sn.lucidchart.spoke`.|
|Architectural Artifacts section missing|Document Management was not active when Enterprise Architecture was activated|Activate `com.snc.platform_document_management`, then reactivate `com.snc.apm`.|
|Now Assist buttons not visible in workspace|Now Assist for EA was not active when EA Workspace was activated|Activate `sn_apm_gen_ai`, then reactivate `com.snc.apm_workspace`.|
|Digital Integration entities missing in diagrams|Digital Integration Management was not active when Enterprise Modeling Common was activated|Activate `com.snc.apm_digital_integration`, then reactivate `com.snc.apm_modelling_tool_common`.|

**Parent Topic:**[Install Enterprise Architecture Workspace](../../task/install-ea-workspace.md)

