---
title: Map regulations to the entities
description: Map single or multiple regulations with the entity linked to an incident or security incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/configure-case-types-map-regu.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Map regulations to the entities

Map single or multiple regulations with the entity linked to an incident or security incident.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## About this task

The Digital Resilience Incident Case module in the Operational Resilience Workspace lists all Digital Resilience Incident Cases associated with an incident or security incident. The Digital Resilience Incident Case record type now has a Regulation Mappings related list. It shows the relationships between entities related to the cases and their regulations.

A regulation mapping links an entity to a regulation. The sequence is as follows:

1.  You map an entity to one or more regulations in the Regulation Mappings related list.
2.  You add the entity to an incident or security incident.
3.  The application creates regulation records on the case.
4.  The action task flows run on each regulation record and create the action tasks.

Each regulation record on a case drives the action task workflow for that case. Two flows run when a regulation record is added or updated on a Digital Resilience Incident Reporting case. The flows are 'Action task automation for regulation addition' and 'Action task automation on regulation updates'. These flows read the action task configuration of the matching Regulatory Body Management Agency Profile \[sn\_reg\_body\_mgmt\_agency\_profile\] record. The flows automatically create the required action tasks \(Regulatory reporting assessment of IT incidents, DRI Initial/Intermediate/Final reports\). The action tasks use the assignment groups, due dates, repeat intervals, and termination conditions defined in those templates. For details on the action task templates, see [Set up action task templates in Regulatory agency profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/set-up-action-task-templates.md).

## Procedure

1.  Navigate to **All** &gt; **Digital Resilience Incident Reporting** &gt; **Digital Resilience Incident Case Type** and open the desired case record.

    The Digital Resilience Incident Case record is displayed.

    \[Omitted image "dri-case-record.png"\] Alt text: Digital Resilience Incident Case record.

2.  To map a regulation to an entity associated with the case, select **New** in the Regulation Mappings related list.

    The Regulation Mappings New record is displayed.

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Entity|Name of the entity, for example, Acer.|
        |Regulation|Regulation that is mapped to the entity associated with the case, for example, Digital Operational Resilience Act.|
        |Record type|Digital Resilience Incident Case record. This field is auto-filled.|

        The example illustrates mapping the Acer entity to the 'Digital Operational Resilience Act' \(a single regulation\).

        After this mapping is saved, adding the Acer entity to an incident or security incident creates regulation records on the case. These records trigger the corresponding action tasks based on the regulation's action task configuration. If a case has multiple regulation records, a separate set of action tasks \(and therefore separate Initial/Intermediate/Final reports\) is generated per regulation.

        \[Omitted image "reg-mapping-new-record-regulations-added.png"\] Alt text: Mapping an entity to a single regulation.

3.  To map several regulations to the same entity, select all of them in the **Regulation** field of the same record.

4.  Select **Save**.

    The regulation mapping is saved.


**Related topics**  


[Complete action tasks and report regulatory incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/work-on-action-tasks.md)

[Configure the Digital Resilience Incident Case record type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configure-dri-case-record-type.md)

