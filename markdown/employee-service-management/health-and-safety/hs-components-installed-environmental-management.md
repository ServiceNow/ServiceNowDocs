---
title: Components installed with Health and Safety Environmental Management
description: Several types of components are installed with activation of the Health and Safety Environmental Management plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Components installed with Health and Safety Environmental Management

Several types of components are installed with activation of the Health and Safety Environmental Management plugin, including tables, user roles, and scheduled jobs.

## Store applications installed

<table id="table_at1_ddl_lhc"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Core

</td><td>

Installs core data model for Health and Safety. This data model includes common components such as Health and Safety user profile and actions that are used in the Health and Safety applications.

 For more information on store applications, roles, and tables installed with Health and Safety Core, see [Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md).

</td></tr><tr><td>

Health and Safety Risk Management

</td><td>

Installs the Health and Safety Risk Management application. For more information on store applications, roles, and tables installed with Health and Safety Risk Management, see [Components installed with Health and Safety Risk Management](../../hs-risk-management/reference/components-installed-with-hs-risk-mgmt.md)

</td></tr></tbody>
</table>## Roles installed

<table id="table_yfk_mvd_lhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Admin

 \[sn\_hs\_env.admin\]

</td><td>

Administrator for Health and Safety Environmental Management

</td><td>

sn\_hs\_chm.manager

</td></tr><tr><td>

Chemical manager

 \[sn\_hs\_chm.manager\]

</td><td>

Can read, create, write, and delete access to all chemical records

</td><td>

-   sn\_hs\_chm.writer
-   sn\_hs\_chm.reader

</td></tr><tr><td>

Chemical requestor

 \[sn\_hs\_chm.requestor\]

</td><td>

Can create chemical requests from the Employee Center

</td><td>

sn\_ohs\_im.document\_reader

</td></tr><tr><td>

Chemical reader

 \[sn\_hs\_chm.reader\]

</td><td>

Can view all chemical records

</td><td>

-   sn\_ohs\_im.document\_reader
-   sn\_hs\_rm.safety\_register\_reader
-   sn\_ohs\_im.action\_reader
-   sn\_ohs\_im.hs\_profile\_reader

</td></tr><tr><td>

Chemical writer

 \[sn\_hs\_chm.writer\]

</td><td>

Can create, write, and delete access to all chemical records

</td><td>

-   sn\_ohs\_im.action\_writer
-   sn\_ohs\_im.document\_writer
-   sn\_hs\_rm.safety\_register\_writer

</td></tr><tr><td>

Chemical sensitive content user

 \[sn\_hs\_chm.sensitive\_content\_user\]

</td><td>

Can access sensitive chemical records

</td><td>

None

</td></tr><tr><td>

Connector admin

 \[sn\_hs\_connector\_co.admin\]

</td><td>

Administrator for Connector Core application. Can manage connections with external applications or plugins.

</td><td>

sn\_hs\_connector\_co.user

</td></tr><tr><td>

Connector core user

 \[sn\_hs\_connector\_co.user\]

</td><td>

Can read, create, write, and view connector plugins.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_cgk_mvd_lhc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Chemical

 \[sn\_hs\_chm\_chemical\]

</td><td>

Stores information about each chemical, including hazard identification, ingredients \(with concentrations\), related documents \(such as safety data sheets\), and location-specific chemical items.

</td></tr><tr><td>

Chemical first aid

 \[sn\_hs\_chm\_chemical\_first\_aid\]

</td><td>

Stores information about the first aid measures for a chemical exposure.

</td></tr><tr><td>

Chemical group

 \[sn\_hs\_chm\_chemical\_group\]

</td><td>

Stores details about multiple chemicals that can be grouped.

</td></tr><tr><td>

Chemical ingredient

 \[sn\_hs\_chm\_chemical\_ingredient\]

</td><td>

Contains information defining how much of each chemical substance is included in the chemical.

</td></tr><tr><td>

Chemical request

 \[sn\_hs\_chm\_chemical\_request\]

</td><td>

Stores data obtained from the chemical request. It includes details such as chemical name, SDS attachment, usage details, quantity, and location.

</td></tr><tr><td>

Chemical substance

 \[sn\_hs\_chm\_chemical\_substance\]

</td><td>

Stores data about individual components or materials that make up the ingredients of a chemical.

</td></tr><tr><td>

Chemical hazard category

 \[sn\_hs\_chm\_hazard\_category\]

</td><td>

Stores categories for chemical hazards.

</td></tr><tr><td>

Chemical hazard class

 \[sn\_hs\_chm\_hazard\_class\]

</td><td>

Stores class for chemical hazards.

</td></tr><tr><td>

Chemical hazard identification

 \[sn\_hs\_chm\_hazard\_identification\]

</td><td>

Stores data based on Globally Harmonized System \(GHS\)

</td></tr><tr><td>

Chemical hazard statement

 \[sn\_hs\_chm\_hazard\_statement\]

</td><td>

Statements that describe the hazards that are associated with the chemical.

</td></tr><tr><td>

M2M chemical group action

 \[sn\_hs\_chm\_m2m\_chemical\_group\_action\]

</td><td>

Tables that connects chemicals with the actions list.

</td></tr><tr><td>

M2M chemical group risk assessment

 \[sn\_hs\_chm\_m2m\_chemical\_group\_risk\_assessment\]

</td><td>

Table that connects chemical group to risk assessments.

</td></tr><tr><td>

Chemical item

 \[sn\_hs\_rm\_safety\_register\_chemical\]

</td><td>

Stores details about specific physical containers or instances.

</td></tr><tr><td>

Chemical precautionary statement

 \[sn\_hs\_chm\_precautionary\_statement\]

</td><td>

Stores data based on Globally Harmonized System \(GHS\)

</td></tr><tr><td>

Statement

 \[sn\_hs\_chm\_statement\]

</td><td>

Additional statements that can be added. Extends from the chemical hazard statement table and the chemical precautionary statement table.

</td></tr><tr><td>

Service provider request

 \[sn\_hs\_connector\_core\_service\_provider\_request\]

</td><td>

Stores records of data requested from the 3E system.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Environmental Management reference](../concept/hs-reference-environmental-management.md)

