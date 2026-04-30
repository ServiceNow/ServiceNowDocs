---
title: Opportunity Type Configuration for Opportunity Marketplace
description: Opportunity Marketplace \(OPM\) supports different opportunity types that are designed for unique types of opportunities and roles.
locale: en-US
release: xanadu
product: Opportunity Marketplace
classification: opportunity-marketplace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference Opportunity Marketplace roles and tables, Opportunity Marketplace, Talent Development, Employee Service Management]
---

# Opportunity Type Configuration for Opportunity Marketplace

Opportunity Marketplace \(OPM\) supports different opportunity types that are designed for unique types of opportunities and roles.

Admins can create opportunity types. There are three opportunity types that automatically come with OPM. Admins can create other opportunity types.

|Opportunity type|Description|
|----------------|-----------|
|Gig|A Gig is an opportunity that consists of just a single role that can have one or many vacancies.|
|Project|A Project is an opportunity that is intended to enable sourcing a team that consist of multiple roles with one or many vacancies according to the role.|
|Volunteer|A Volunteer is an opportunity that consists of multiple roles with one or many vacancies according to role for volunteering-related activities.|

<table id="table_rq3_klt_bcc"><thead><tr><th>

Field name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Title**

</td><td>

A title for the opportunity that is visible from the Opportunity Marketplace in the Employee Center.

</td></tr><tr><td>

**Role display**

</td><td>

Controls the number of roles that can be added to an opportunity.-   **Embedded within opportunity \(1 position only\)**
-   **Separate from opportunity \(1 or more positions\)**

</td></tr><tr><td>

**Opportunity details**

</td><td>

A list of available opportunity descriptions. The **Opportunity details** are visible in the opportunity. **Opportunity details** are stored in the Project opportunity creation details \[sn\_opp\_market\_opportunity\] table.

 Opportunity details and Roles and requirements are record producer records in the Catalog Item \[sc\_cat\_item\] table. The record producer is a configuration of the layout for which fields are shown. There are 3 opportuntiy types included with the base system \(Gigs, Project, and Volunteer\). Clone one of the base opportunity types to create a custom **Opportunity type**.

</td></tr><tr><td>

**Roles and requirements**

</td><td>

A list of available opportunity roles and requirements. Opportunity Marketplace roles and requirements are stored in the Opportunity position \[sn\_opp\_market\_opportunity\_position\] table.

 Opportunity Marketplace roles are the job roles or positions for the opportunity.

</td></tr><tr><td>

**Description**

</td><td>

The text for the description of the opportunity that is displayed in Opportunity Marketplace the Employee Center.

</td></tr><tr><td>

**Hiring approval flow**

</td><td>

A list of available approval flows for managing the hiring process for an opportunity.

</td></tr><tr><td>

**Active**

</td><td>

Select to make the record active.

</td></tr><tr><td>

**User criteria**

</td><td>

Criteria to restrict access to the opportunity record. User criteria defined in the opportunity type determines who can create an opportunity type.

</td></tr><tr><td>

**Icon**

</td><td>

You can add an icon to opportunity types or view the icons for existing opportunity types.

</td></tr><tr><td>

**Help link label**

</td><td>

The text that is visible to users as the link for help. Add the label from the opportunity type page. The link appears at the bottom of the **Create an opportunity** page in the Employee Center.

</td></tr><tr><td>

**Help link URL**

</td><td>

The URL that is associated with the **Help link label**.

</td></tr></tbody>
</table>**Parent Topic:**[Reference Opportunity Marketplace roles and tables](../concept/egd-oppt-mrktplc-references.md)

