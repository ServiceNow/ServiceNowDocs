---
title: Components installed with Enterprise Agile Planning
description: Several types of components are installed with Enterprise Agile Planning when you install the Strategic Planning applications, including tables and user roles.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Components installed with Enterprise Agile Planning

Several types of components are installed with Enterprise Agile Planning when you install the Strategic Planning applications, including tables and user roles.

## Roles installed

<table id="table_pbg_cxp_d1c"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

EAP admin \[sn\_apw\_advanced.eap\_admin\]

</td><td>

Can add teams to EAP configurations or remove them.

</td><td>

sn\_apw\_advanced.eap\_user

</td></tr><tr><td>

EAP user \[sn\_apw\_advanced.eap\_user\]

</td><td>

-   Can create, update, and delete work items
-   Can create and modify iterations like Planning Intervals and Sprints
-   Can access the team's Backlog and Planning Board

</td><td>

-   scrum\_master
-   sn\_apw\_advanced.eap\_read\_only
-   now\_assist\_panel\_user

This role is available only with the Now Assist for SPM plugin.


</td></tr><tr><td>

EAP read-only role \[sn\_apw\_advanced.eap\_read\_only\]

</td><td>

Can view the EAP team's Backlog and Planning Board

</td><td>

-   scrum\_user
-   workspace\_user
-   canvas\_user

</td></tr></tbody>
</table>## Tables installed

<table id="table_tbg_cxp_d1c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agile Release Train

 \[sn\_apw\_advanced\_agile\_release\_train\]

</td><td>

Stores information of all Agile Release Trains created for the Agile structure of an EAP configuration.This table extends the Enterprise agile team \[sn\_apw\_advanced\_eap\_team\] table.

</td></tr><tr><td>

Agile Team

 \[sn\_apw\_advanced\_agile\_team\]

</td><td>

Stores information of all Agile Teams created for the Agile structure of an EAP configuration.This table extends the Enterprise agile team \[sn\_apw\_advanced\_eap\_team\] table.

</td></tr><tr><td>

Capability

 \[sn\_align\_core\_capability\]

</td><td>

Stores information of all Capability type of work items created in EAP.This table extends the EAP planning item \[sn\_align\_core\_eap\_planning\_item\] table.

</td></tr><tr><td>

EAP planning item

 \[sn\_align\_core\_eap\_planning\_item\]

</td><td>

Base table for all EAP work item types.This table extends the Planning Item Entry \[sn\_align\_core\_planning\_item\] table.

</td></tr><tr><td>

Enterprise agile calendar

 \[sn\_apw\_advanced\_eap\_calendar\]

</td><td>

Stores information of iteration types such as Planning Intervals and Sprints.This table extends the Business Calendar \[business\_calendar\] table.

</td></tr><tr><td>

Enterprise agile calendar entry

 \[sn\_apw\_advanced\_eap\_calendar\_span\]

</td><td>

Stores information of the timeline defined or date span for calendar entries of a business calendar span.For example, for a Sprint calendar type, six calendar entries spanning over three months can be created. This table stores the date spans for each of these Sprint calendar entries.

This table extends the Business Calendar Entry \[business\_calendar\_span\] table.

</td></tr><tr><td>

Enterprise agile configuration

 \(sn\_apw\_advanced\_eap\_configuration\)

</td><td>

Stores information of agile configurations such as Full configuration, Portfolio configuration, and other default and custom configurations.

</td></tr><tr><td>

Enterprise agile configuration detail

 \[sn\_apw\_advanced\_eap\_configuration\_detail\]

</td><td>

Stores the details of the default work item type and planning calendar associated with a team type for a configuration.It also stores:

-   Team hierarchy in the Agile structure for a configuration.
-   Work item type available on the Backlog and Planning board pages.

</td></tr><tr><td>

Enterprise agile iteration

 \[sn\_apw\_advanced\_eap\_iteration\]

</td><td>

Stores the details of team-level iterations details such as capacity, total points, State, and others.

</td></tr><tr><td>

Enterprise agile iteration type

 \[sn\_apw\_advanced\_eap\_iteration\_type\]

</td><td>

Stores the information about planning calendar types such as Planning Intervals or Sprints.

</td></tr><tr><td>

Enterprise agile team

 \[sn\_apw\_advanced\_eap\_team\]

</td><td>

Base table for all EAP teams such as ART, Solution Trains, Agile Release Trains, and Portfolios created in the Agile structure for a configuration.

</td></tr><tr><td>

Enterprise agile team structure

 \[sn\_apw\_advanced\_eap\_team\_structure\]

</td><td>

Contains information of team hierarchy.

</td></tr><tr><td>

Enterprise agile work structure

 \[sn\_apw\_advanced\_eap\_work\_structure\]

</td><td>

Contains information of work item type hierarchy.

</td></tr><tr><td>

Epic

 \[sn\_align\_core\_scrum\_epic\]

</td><td>

Stores information of all Epic work items created in EAP.This table extends the EAP planning item \[sn\_align\_core\_eap\_planning\_item\] table.

</td></tr><tr><td>

Feature

 \[sn\_align\_core\_feature\]

</td><td>

Stores information of all Feature work items created in EAP. This table extends the EAP planning item \[sn\_align\_core\_eap\_planning\_item\] table.

</td></tr><tr><td>

Solution Train

 \[sn\_apw\_advanced\_solution\_train\]

</td><td>

Stores information of all Solution Trains created for the Agile structure of an EAP configuration.This table extends the Enterprise agile team \[sn\_apw\_advanced\_eap\_team\] table.

</td></tr><tr><td>

SAFe Portfolio

 \[sn\_apw\_advanced\_eap\_portfolio\]

</td><td>

Stores information of all Portfolios created for the Agile structure of an EAP configuration.This table extends the Enterprise agile team \[sn\_apw\_advanced\_eap\_team\] table.

</td></tr><tr><td>

Story\[rm\_story\]

</td><td>

Stores information of all stories created.

 This table is installed with the Agile Development 2.0 application, which is installed with Strategic Planning.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Agile Planning reference](eap-reference.md)

