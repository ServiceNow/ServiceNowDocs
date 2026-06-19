---
title: Application plugin installation sequence for Enterprise Architecture Workspace
description: Activate the required plugins and optional add-ons in the correct order to confirm all Enterprise Architecture Workspace features are available on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/enterprise-architecture/eaw-plugin-activation-sequence.html
release: australia
product: Enterprise Architecture
classification: enterprise-architecture
topic_type: reference
last_updated: "2026-05-18"
reading_time_minutes: 4
breadcrumb: [Install Enterprise Architecture Workspace, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Application plugin installation sequence for Enterprise Architecture Workspace

Activate the required plugins and optional add-ons in the correct order to confirm all Enterprise Architecture Workspace features are available on your instance.

## Enterprise Architecture Workspace application plugin list

The Enterprise Architecture Workspace consists of a core plugin and several feature plugins and optional add-ons. Some features only become available when their dependent plugins are active at the time of activation.

Loading the core plugin before feature plugins and optional add-ons confirms that all functionalities are initialized properly.

**Note:** Activating plugins out of order can cause features to appear missing after activation — with no error message to indicate the cause. Follow the sequence in this topic to avoid this.

You must have the admin role to activate plugins and store apps. Verify that your instance is on a supported release for the plugins you plan to activate.

## Plugin activation sequence

|\#|Plugin ID|Display name|Required|What it enables|
|---|---------|------------|--------|---------------|
|Core|
|1|com.snc.apm\_core|Enterprise Architecture Core|Yes|Base data model. Activate first.|
|2|com.snc.apm|Enterprise Architecture|Yes|Core plugin. All other EA plugins depend on this.|
|3|com.snc.apm\_read\_roles|Read-only Roles for EA|Yes|Read-only access roles. Activate before assigning roles to users.|
|4|sn\_4\_q\_bubble|Four-Quadrant Bubble Chart|Yes|UI component required by the workspace. Must be active before \#5.|
|5|com.snc.apm\_workspace|Enterprise Architecture Workspace|Yes|Main workspace UI. Requires \#1–4 to be active first.|
|Feature plugins — activate after core \(\#1–5\) in any order|
|6|`com.snc.apm_trm`|TRM|Yes|Technology reference model, lifecycle tracking, and technical debt calculation. Activate before TPM \(\#7\).|
|7|com.snc.apm\_tpm|Technology Portfolio Management|Yes|Software lifecycle data, capability scores, and software model mapping in the workspace. Activate after TRM \(\#6\).|
|8|com.snc.apm\_tco|Total Cost of Ownership|No|TCO cost data on application records.|
|9|com.snc.apm\_digital\_integration|Digital Integration Management|No|Digital integration entities. If you plan to use Enterprise Modeling and Visualization \(\#15–17\), activate this plugin first.|
|10|com.snc.apm\_cloud\_readiness|Cloud Readiness Assessment|No|Cloud readiness scoring on application records.|
|GRC integration — activate the platform plugin before the EA plugin in each pair|
|11|com.sn\_risk\_advanced|Advanced Risk Management|No|Platform plugin. Required before \#12.|
|12|com.snc.apm\_risk\_assessment|Risk Assessment for EA|No|Risk Assessment section on Business Application records and in diagrams.|
|13|com.sn\_compliance|Compliance|No|Platform plugin. Required before \#14.|
|14|com.snc.apm\_control\_management|Control Management for EA|No|Controls section on Business Application records and in diagrams.|
|Enterprise Modeling and Visualization — activate in this exact order after core and feature plugins|
|15|com.sn\_apm\_diagram\_builder|APM Diagram Builder|No|Diagram builder engine. Required before \#16–17.|
|16|com.snc.apm\_modelling\_tool\_common|Enterprise Modeling and Visualization Common|No|Base data model for diagrams. Required before \#17.|
|17|com.snc.apm\_modelling\_tool|Enterprise Modeling and Visualization|No|Diagramming and modeling capabilities in the workspace.|
|Optional add-ons — activate at any point after their listed prerequisites|
|18|com.snc.apm\_ppt\_export|PPT Export for EA|No|PowerPoint export from the workspace. Requires \#5.|
|19|com.snc.sn\_lucidchart\_integration|Lucidchart Integration|No|Lucidchart diagram integration. Requires IntegrationHub to be active first.|
|20|com.sn.lucidchart.spoke|Lucidchart Diagramming Spoke|No|Lucidchart spoke actions in Flow Designer. Requires IntegrationHub to be active first.|
|21|com.snc.pa.apm|Performance Analytics for APM|No|Performance Analytics dashboards for EA. Requires Performance Analytics to be active.|
|22|com.snc.pa.apm.change\_request|Performance Analytics for APM – Change|No|Change request analytics for EA. Requires \#21.|
|23|com.snc.pa.apm.problem|Performance Analytics for APM – Problem|No|Problem analytics for EA. Requires \#21.|
|24|com.snc.apm.predictive\_intelligence|EA – Predictive Intelligence|No|Predictive Intelligence features for EA. Licensable.|

## Post-activation checklist

After activating all required plugins and any optional add-ons, verify that the expected features are available.

-   Go to **Workspaces** &gt; **Enterprise Architecture Workspace**. The workspace opens without errors.
-   The Application Rationalization bubble chart is visible.
-   The Business Applications list populates with data.
-   The Capability Heatmap renders correctly.
-   If TPM \(\#7\) is active, lifecycle data is visible on application records and capability scores display in the Business Capability Hierarchy.
-   If Enterprise Modeling and Visualization \(\#15–17\) is active, the **Modeling and Visualization** section is available in the workspace navigation and EA entity shapes appear in the diagram shape library.

## Resolving missing features

If a feature is missing after activation, use the following table to identify the cause and resolve it.

|Missing feature|Likely cause|Resolution|
|---------------|------------|----------|
|Bubble Chart page is blank or missing|The Four-Quadrant Bubble Chart plugin was not active when the workspace was activated|Reactivate com.snc.apm\_workspace after confirming sn\_4\_q\_bubble is active.|
|Risk Assessment section missing from workspace|Advanced Risk Management was not active before Risk Assessment for EA was activated|Activate com.sn\_risk\_advanced, then reactivate com.snc.apm\_risk\_assessment.|
|No entity shapes in diagram editor|Enterprise Architecture Core was not active when Enterprise Modeling and Visualization was activated|Confirm com.snc.apm is active, then reactivate com.snc.apm\_modelling\_tool.|
|Digital Integration shapes missing from diagrams|Digital Integration Management was activated after Enterprise Modeling and Visualization|Activate com.snc.apm\_digital\_integration, then reactivate com.snc.apm\_modelling\_tool\_common.|
|Lucidchart spoke actions missing in Flow Designer|IntegrationHub was not active before the Lucidchart spoke was activated|Activate IntegrationHub, then reactivate com.sn.lucidchart.spoke.|
|Architectural Documents section missing|The Document Management platform plugin was not active whenEnterprise Architecture was activated|Activate com.snc.platform\_document\_management, then reactivate com.snc.apm.|
|Now Assist buttons not visible in the workspace|The Now Assist for Enterprise Architecture \(EA\) plugin is not active|Activate sn\_apm\_gen\_ai.|

**Parent Topic:**[Install Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/enterprise-architecture/install-ea-workspace.md)

