---
title: Components installed with Portfolio Planning
description: Several types of components are installed with activation of the Portfolio Planning application, including tables and user roles.
locale: en-US
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Portfolio Planning, Strategic Portfolio Management]
---

# Components installed with Portfolio Planning

Several types of components are installed with activation of the Portfolio Planning application, including tables and user roles.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Portfolio Planning admin\[sn\_align\_core.apw\_admin\]

</td><td>

Can access all the modules in the Portfolio Planning application

</td><td>

-   it\_portfolio\_manager
-   sn\_align\_core.apw\_user
-   view\_changer

</td></tr><tr><td>

Portfolio Planning user\[sn\_align\_core.apw\_user\]

</td><td>

Can create, update, and delete portfolio plans, free-form roadmaps, and planning items.

 This role can be given to users such as portfolio or product managers, business unit leads, and other planning personas.

</td><td>

-   sn\_align\_cmn\_int.user
-   sn\_milestones.milestone\_editor

</td></tr><tr><td>

sn\_align\_core.ap\_read\_only

</td><td>

-   Can view portfolio plans and free-form roadmaps that are shared with them.
-   Can add notes, comments, or attachments to portfolio plans and roadmaps that are shared with them.
-   Can create, edit, and delete portfolio plan views and free-form roadmap views.

**Note:** Only the owner can edit or delete a portfolio plan view or a free-form roadmap view.


</td><td>

sn\_milestones.milestone\_viewer

</td></tr><tr><td>

Milestones editor\[sn\_milestones.milestone\_editor\]

</td><td>

Can create, update, and delete milestones on the roadmap.

</td><td>

sn\_milestones.milestone\_viewer

</td></tr><tr><td>

Milestones viewer\[sn\_milestones.milestone\_viewer\]

</td><td>

Can view milestones on the roadmap.

</td><td>

None

</td></tr><tr><td>

Business stakeholder\[business\_stakeholder\]

</td><td>

-   Can create and update portfolio plans and free-form roadmaps.
-   Can add notes, comments, or attachments to portfolio plans and roadmaps that are shared with them.
-   Can personalize the roadmaps.
-   Can view generated resource capacity for planning items in the Capacity Planning screen.
-   Can view goals and related records using the platform view.

 **Note:** Users with this role do not have access to create or edit any roadmap items.

</td><td>

-   sn\_align\_core.ap\_read\_only
-   sn\_align\_ws.spw\_capacity\_read
-   sn\_gf.goal\_user\_read

</td></tr></tbody>
</table>|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_align\_ws.scenario\_approver|Can approve the scenarios for the portfolio.|sn\_align\_core.apw\_user|

<table id="table_thr_jq3_fdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Portfolio Planning integrations user

 \[sn\_align\_cmn\_int.user\]

</td><td>

Imports, exports, and manages planning items between Portfolio Planning and PPM.

</td><td>

connection\_admin

</td></tr></tbody>
</table>|Role title \[name\]|Description|Contains role|
|-------------------|-----------|-------------|
|sn\_align\_ws.spw\_capacity\_user|Can generate resource capacity details.|sn\_align\_ws.spw\_capacity\_read|
|sn\_align\_ws.spw\_capacity\_read|Can view resource capacity details.|None|

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_align\_ws.spw\_financial\_user|Create cost plans and expense lines for planning items.|None|

## Tables installed

<table id="table_jkf_1js_cwb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alignment Integration

 \[sn\_align\_cmn\_int\_integrations\_setup\]

</td><td>

Stores data of integration information for your ServiceNow instance

</td></tr><tr><td>

Choice Map

 sn\_align\_cmn\_int\_choice\_map

</td><td>

Stores choice map relationships between fields of planning items of Portfolio Planning and PPM

</td></tr><tr><td>

Demand

 \[sn\_align\_core\_demand\]

</td><td>

Stores records created with Demand planning item type.

</td></tr><tr><td>

Dependency

 \[sn\_align\_core\_dependency\]

</td><td>

Stores data of dependencies between roadmap items.

</td></tr><tr><td>

Field Map

 \[sn\_align\_cmn\_int\_field\_map\]

</td><td>

Stores field map relationships between planning items of Portfolio Planning and PPM

</td></tr><tr><td>

Import Request

 \[sn\_align\_cmn\_int\_import\_request\]

</td><td>

Stores imports requests from Portfolio Planning to PPM

</td></tr><tr><td>

Instance Mapping

 \[sn\_align\_cmn\_int\_instance\_mapping\]

</td><td>

Stores mapping information between instances

</td></tr><tr><td>

Integration Error

 \[sn\_align\_cmn\_int\_integration\_error\]

</td><td>

Stores errors for integration between Portfolio Planning and PPM

</td></tr><tr><td>

Integration Mapping

 \[sn\_align\_cmn\_int\_integration\_mapping\]

</td><td>

Stores Integration mappings between Portfolio Planning and PPM

</td></tr><tr><td>

Lens

 \[sn\_align\_core\_lens\]

</td><td>

Stores data of the lens configuration.

</td></tr><tr><td>

Lens structure

 \[sn\_align\_core\_lens\_structure\]

</td><td>

Stores data of lens entities and the relationship between them for different lenses.

</td></tr><tr><td>

Planning Item

 \[sn\_align\_core\_planning\_item\]

</td><td>

Stores the data of all planning item types.

</td></tr><tr><td>

Portfolio plan

 \[sn\_align\_ws\_portfolio\_plan\]

</td><td>

Stores data of portfolio plans.

</td></tr><tr><td>

Project

 \[sn\_align\_core\_project\]

</td><td>

Stores records created with Project planning item type.

</td></tr><tr><td>

Roadmap configuration

 \[sn\_align\_ws\_roadmap\_configuration\]

</td><td>

Stores the configuration data for tables that are used to create portfolio roadmaps and free-form roadmaps.

</td></tr><tr><td>

Table Map

 sn\_align\_cmn\_int\_table\_map

</td><td>

Stores table mapping relationships between planning items in Portfolio Planning and PPM

</td></tr></tbody>
</table>## System properties installed

<table id="table_k2f_t3m_fwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.sn\_align\_cmn\_int.bulk\_import

</td><td>

-   Type: Choice list
-   Default value: INSERT
-   Other possible values:
    -   INSERT
    -   &lt;Value 2 name&gt;:
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Configure bulk import](../../apw-internal-integrations/reference/configure-bulk-import.md)

</td></tr></tbody>
</table>**Parent Topic:**[Portfolio Planning reference](../concept/portfolio-planning-reference.md)

