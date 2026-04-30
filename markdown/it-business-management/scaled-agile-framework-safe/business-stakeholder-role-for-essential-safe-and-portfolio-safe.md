---
title: Business stakeholder role for Essential SAFe and Portfolio SAFe
description: Use the business stakeholder role to read and retrieve data from any table of the Essential SAFe and Portfolio SAFe applications to generate reports.
locale: en-US
release: xanadu
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Business stakeholder role for Essential SAFe and Portfolio SAFe

Use the business stakeholder role to read and retrieve data from any table of the Essential SAFe and Portfolio SAFe applications to generate reports.

**Important:**

Starting with the Xanadu release, Portfolio SAFe, Essential SAFe, Performance Analytics Content Pack for Essential SAFe, Work Progress Status for SAFe, Agile - Scaled Agile Framework - Unified Backlog, and Read only roles for SAFe plugins are being prepared for future deprecation. These plugins will be hidden and can no longer be activated on new instances but will continue to be supported. [Enterprise Agile Planning in Strategic Planning](../../spw-eap/concept/eap-landing.md) provides the latest experience for this functionality.

For more information on the deprecation process and its impact, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

When you activate the Business Stakeholder plugin \(com.snc.business\_stakeholder\) in your ServiceNow instance, the Read only roles for SAFe plugin \(com.snc.sdlc.safe\_read\_roles\) is also activated. This plugin provides a business stakeholder role \(sn\_safe\_read\) with which you can access all the tables of Essential SAFe and Portfolio SAFe applications. You can assign this role to any user in your organization who is a business stakeholder.

## Plugin availability

If you are a new customer, the Read only roles for SAFe plugin \(com.snc.sdlc.safe\_read\_roles\) is activated on zBoot. However, the business stakeholder role \(sn\_safe\_read\) is available only when you activate the Agile - Scaled Agile Framework - Essential SAFe plugin \(com.snc.sdlc.safe\) or Agile - Scaled Agile Framework - Portfolio SAFe plugin \(com.snc.sdlc.portfolio\_safe\).

If you are an upgrade customer, you must manually activate the Read only roles for Essential SAFe and Portfolio SAFe plugins \(com.snc.sdlc.safe\_read\_roles\).

## SAFe tables accessible by users with the business stakeholder role

When the read-only roles for SAFe plugin \(com.snc.sdlc.safe\_read\_roles\) is active in your ServiceNow instance along with either the Essential SAFe plugin \(com.snc.sdlc.safe\) or Portfolio SAFe plugin \(com.snc.sdlc.portfolio\_safe\), the user with the business stakeholder role \(sn\_safe\_read\) has read access to the following tables.

<table id="table_dqt_pnp_kcb0"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SAFe epic\[sn\_safe\_epic\]

</td><td>

Information about epics.

</td></tr><tr><td>

SAFe feature\[sn\_safe\_feature\]

</td><td>

Information about features.

</td></tr><tr><td>

Agile Release Train\[sn\_safe\_program\]

</td><td>

Information about ART.

</td></tr><tr><td>

Program Increment\[sn\_safe\_program\_increment\]

</td><td>

Information about program increments. Stores the predictability measure data from PI objectives.

</td></tr><tr><td>

SAFe ART team\[sn\_safe\_program\_m2m\_group\]

</td><td>

Relationships between groups and ART.

</td></tr><tr><td>

SAFe ART Member\[sn\_safe\_program\_member\]

</td><td>

Information about members within an ART.

</td></tr><tr><td>

SAFe ART Sprint\[sn\_safe\_program\_sprint\]

</td><td>

Sprint schedules of teams within the ART.

</td></tr><tr><td>

SAFe ART VTB Board\[sn\_safe\_program\_vtb\_board\]

</td><td>

Records displayed on the ART level, Board tab.

</td></tr><tr><td>

SAFe Scrum Task\[sn\_safe\_scrum\_task\]

</td><td>

Information about SAFe scrum tasks.

</td></tr><tr><td>

SAFe Sprint\[sn\_safe\_sprint\]

</td><td>

Information about sprints.

</td></tr><tr><td>

SAFe Story\[sn\_safe\_story\]

</td><td>

Information about stories.

</td></tr><tr><td>

SAFe Team VTB Board\[sn\_safe\_team\_vtb\_board\]

</td><td>

Records displayed on the Team level, Board tab.

</td></tr><tr><td>

SAFe PI Objectives\[sn\_safe\_pi\_objective\]

</td><td>

Stores the SAFe PI objectives.

</td></tr><tr><td>

SAFe team predictability measure\[sn\_safe\_pi\_m2m\_group\]

</td><td>

Stores the business value achieved per team from PI objectives which is used for team-level predictability measure data.

</td></tr></tbody>
</table><table id="table_dqt_pnp_kcb1"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SAFe epic\[sn\_safe\_epic\]

</td><td>

Information about epics.

</td></tr><tr><td>

SAFe feature\[sn\_safe\_feature\]

</td><td>

Information about features.

</td></tr><tr><td>

Agile Release Train\[sn\_safe\_program\]

</td><td>

Information about ART.

</td></tr><tr><td>

Program Increment\[sn\_safe\_program\_increment\]

</td><td>

Information about program increments.

</td></tr><tr><td>

SAFe ART team\[sn\_safe\_program\_m2m\_group\]

</td><td>

Relationships between groups and ART.

</td></tr><tr><td>

SAFe ART Member\[sn\_safe\_program\_member\]

</td><td>

Information about members within an ART.

</td></tr><tr><td>

SAFe ART Sprint\[sn\_safe\_program\_sprint\]

</td><td>

Sprint schedules of teams within the ART.

</td></tr><tr><td>

SAFe ART VTB Board\[sn\_safe\_program\_vtb\_board\]

</td><td>

Records displayed on the ART level, Board tab.

</td></tr><tr><td>

SAFe Scrum Task\[sn\_safe\_scrum\_task\]

</td><td>

Information about SAFe scrum tasks.

</td></tr><tr><td>

SAFe Sprint\[sn\_safe\_sprint\]

</td><td>

Information about sprints.

</td></tr><tr><td>

SAFe Story\[sn\_safe\_story\]

</td><td>

Information about stories.

</td></tr><tr><td>

SAFe PI Objectives\[sn\_safe\_pi\_objective\]

</td><td>

Stores the SAFe PI objectives.

</td></tr><tr><td>

SAFe team predictability measure\[sn\_safe\_pi\_m2m\_group\]

</td><td>

Stores the business value achieved per team from PI objectives which is used for team-level predictability measure data.

</td></tr><tr><td>

Portfolios\[pm\_portfolio\]

</td><td>

Information about portfolios.

</td></tr><tr><td>

Portfolio SAFe VTB board\[sn\_portfolio\_safe\_vtb\_board\]

</td><td>

Records displayed on the portfolio level, Board tab.

</td></tr><tr><td>

SAFe Team VTB Board\[sn\_safe\_team\_vtb\_board\]

</td><td>

Records displayed on the Team level, Board tab.

</td></tr></tbody>
</table>