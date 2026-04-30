---
title: Tables installed with Risk Management
description: Tables are added with activation of GRC: Risk Management.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Components installed with Risk Management, Reference, Risk Management, Governance, Risk, and Compliance]
---

# Tables installed with Risk Management

Tables are added with activation of GRC: Risk Management.

<table id="table_kf4_nqk_qjb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk\[sn\_risk\_risk\]

</td><td>

Extends Item table \[sn\_grc\_item\] and stores specific risks associated with entities

</td></tr><tr><td>

Risk Statement \[sn\_risk\_definition\]

</td><td>

Extends Content table \[sn\_grc\_content\] and stores definitions of risks.

</td></tr><tr><td>

Risk Framework\[sn\_risk\_framework\]

</td><td>

Extends Document table \[sn\_grc\_document\] and stores all risk frameworks, a collection of risk statements

</td></tr><tr><td>

Risk Framework to Entity Type\[sn\_risk\_m2m\_framework\_profile\_type\]

</td><td>

Extends Document to Entity Type table \[sn\_grc\_m2m\_document\_profile\_type\] and is a many-to-many relationship table that is used to manage the relationships between risk frameworks and entity types

</td></tr><tr><td>

Entity Type to Risk Statement\[sn\_risk\_m2m\_risk\_definition\_profile\_type\]

</td><td>

Extends Content to Entity Type table \[sn\_grc\_m2m\_content\_profile\_type\] and is a many-to-many relationship table that is used to manage the relationships between entity types and risk statements

</td></tr><tr><td>

Risk Tasks\[sn\_risk\_m2m\_risk\_task\]

</td><td>

Stores many-to-many relationships between risks and tasks

</td></tr><tr><td>

Risk Transfer\[sn\_risk\_transfer\_task\]

</td><td>

When a risk is analyzed, there are four ways to respond to it. This table provides a way for a risk manager to transfer a risk.

</td></tr><tr><td>

Color Setting\[sn\_risk\_color\_setting\]

</td><td>

This table is used for the reports to relate impact/likelihood with palette colors.

</td></tr><tr><td>

Risk Avoidance\[sn\_risk\_avoidance\_task\]

</td><td>

When a risk is analyzed, there are four ways to respond to it. This table provides a way for a risk manager to avoid a risk. For example, by having a building in California, you are exposed to earthquake risk. You can avoid this risk by choosing not to have buildings in California.

</td></tr><tr><td>

Risk Acceptance\[sn\_risk\_acceptance\_task\]

</td><td>

When a risk is analyzed, there are four ways to respond to it. This table provides a way with an approval process that allows a risk manager to approve \(accept\) or reject the risk.

</td></tr><tr><td>

Risk Mitigation\[sn\_risk\_mitigation\_task\]

</td><td>

When a risk is analyzed, there are four ways to respond to it. This table provides a way for a risk manager to mitigate a risk.

</td></tr><tr><td>

Risk to Controlsn\_risk\_m2m\_risk\_control

</td><td>

Contains relationships of risks to controls.

</td></tr><tr><td>

Risk Statement to Control Objectivesn\_risk\_m2m\_risk\_definition\_policy\_statement

</td><td>

Contains relationships of Risk statements to Control objectives. On addition of entry to this, related risks to controls relationships get created in Risk to Control table with matching entity.

</td></tr><tr><td>

Risk Mitigation to Controlsn\_risk\_m2m\_risk\_mitigation\_control

</td><td>

Controls added to Risk mitigation task as part of the task's flow to mitigate risk are added to this table.

</td></tr><tr><td>

Risk Relationshipsn\_risk\_m2m\_risk\_risk

</td><td>

Contains upstream-downstream/parent-child relationship between two risks.

</td></tr><tr><td>

Risk Response Tasksn\_risk\_response\_task

</td><td>

Base table to Risk Acceptance, Risk Avoidance, Risk Mitigation, Risk Transfer tasks.

</td></tr></tbody>
</table>**Note:** All additional tables installed by the dependent plugins are also needed for GRC: Risk Management.

**Parent Topic:**[Components installed with Risk Management](r_InstallWRisk.md)

