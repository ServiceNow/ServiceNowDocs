---
title: Configure the Digital Resilience Incident Case record type
description: Configure the subtypes, view rules, assignment rules, jurisdictions, and area configurations that define how Digital Resilience Incident Reporting cases behave.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/configure-dri-case-record-type.html
release: zurich
topic_type: task
last_updated: "2026-11-11"
reading_time_minutes: 4
breadcrumb: [Configure, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure the Digital Resilience Incident Case record type

Configure the subtypes, view rules, assignment rules, jurisdictions, and area configurations that define how Digital Resilience Incident Reporting cases behave.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## About this task

The Digital Resilience Incident Case record type defines how Digital Resilience Incident Reporting cases behave. Each related list on the record type controls one aspect of the cases. To map regulations to the entities on a case, see [Map regulations to the entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-case-types-map-regu.md).

## Procedure

1.  Navigate to **All** &gt; **Digital Resilience Incident Reporting** &gt; **Digital Resilience Incident Case Type** and open the desired case record.

    The Digital Resilience Incident Case record is displayed.

    \[Omitted image "dri-case-record.png"\] Alt text: Digital Resilience Incident Case record.

    It contains the following tabs for the record:

    -   **State Model**: The state model and action task state model specify the workflow states and transition conditions for a record type and an action task, respectively. A record type and an action task follow the workflow states configured in their respective state models.
    -   **Assessment Configuration**: Assessment templates are pre-defined formats to request responses from assessors or reviewers that help to evaluate the record.
    -   **Template Configuration**: Document templates are set up for generating word reports.
    -   **Inbound Email Configuration**: Group email configuration is set up to inform the group members about the case record.
    You can configure the related lists described in the following table. The next steps outline each configuration.

    |Related list|What it controls|
    |------------|----------------|
    |Regulation Mappings|Specifies which regulations apply to an entity. When you add the entity to an incident or security incident, the application creates a regulation record on the case for each mapped regulation. Each regulation record triggers the action tasks for that regulation. You can map several regulations to an entity in one record. Each entity can have only one mapping record. For steps, see [Map regulations to the entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-case-types-map-regu.md).|
    |Record type area configs|Defines the tables that you can pick records from for each area type on the case. The area types are Impacted area, Related area, and Cause area. The order sets the sequence of the tables.|
    |Subtypes|Defines the choices for the Sub-type field on the case. A subtype is a record type whose parent is the Digital Resilience Incident Case record type. You select a subtype on the case to classify it more specifically.|
    |View Rules|Sets the form view and display options for cases, such as the default tab and whether details are shown. The default rule applies the Workspace view to Digital Resilience Incident Reporting cases.|
    |Assignment Rules|Defines the group that cases are assigned to. The default rule assigns cases to the Digital Resilience Incident Managers group.|
    |Jurisdictions|Links locations to the record type.|

2.  To add a subtype for the case, navigate to the Subtypes related list and select **New**.

    1.  Add the parameters such as Label, Name, Parent, Category, and Description.

        The following example shows a Subtypes record.

        \[Omitted image "casetype-subtype-new-record.png"\] Alt text: Subtypes record.

    2.  To mark the record as active, set the Active option.

    3.  Select **Submit**.

3.  To set up rules, navigate to the View Rules related list and complete the substeps.

    1.  Add Name, Table, View, Workspace type, and Execution Order number.

        The following example shows a Rules record.

        \[Omitted image "casetype-viewrule-sample-record.png"\] Alt text: Rules record.

    2.  Set the Active flag.

    3.  Set up the roles and conditions in the **Conditions** tab.

    4.  Select Hide details &amp; UI actions, Hide section navigation, and Disable section collapsing in the **Form Settings** tab.

    5.  Set up the Default tab order and focus in **Form Tabs**.

    6.  Select **Submit**.

4.  To assign tasks to specific users and groups automatically, navigate to the Assignment Rules related list and set up the assignment rules.

    The following example shows an Assignment rules record.

    \[Omitted image "casetype-assignrule-sample-record.png"\] Alt text: Assignment rules record.

    1.  Add the name of the rule and set the Active flag.

        The name of the application is auto-filled as Digital Resilience Incident Reporting.

    2.  Select a table in **Applies to** and specify the conditions that must be met before the task is assigned to the user or group.

        The rule is applied only if the task isn’t already assigned to another user or group.

    3.  To assign a task to the users or groups, configure the users or groups in the **Assign to** tab.

    4.  To customize the assignment rule further, enter a script in the **script** tab.

        Scripts provide access to the pool of current variables.

    5.  Select **Submit**.

5.  To link locations to the record type, navigate to the Jurisdictions related list and select **New**.

    Each Jurisdictions record is a location that is linked to the record type. The link is stored in the Case type to jurisdiction table. The Location field on a case isn't limited to the locations that are linked here.

    The following example shows a Jurisdictions location record.

    \[Omitted image "casetype-Juris-sample-record.png"\] Alt text: Jurisdictions record.

    1.  Add Name, City, Zip code, State, country, Phone, Latitude, Longitude details.

    2.  Select **Submit**.

    3.  To edit an existing Jurisdictions record, select **Edit**.

6.  To define the area type for the case and the table associated with it, navigate to the Record type area configs related list and complete the substeps.

    The following example shows a Record type area configuration record.

    \[Omitted image "casetype-areatype-sample-record.png"\] Alt text: Area configs record.

    1.  Set its order and Active flag.

    2.  Select **Submit**.

    The area type can be Impacted area, Related area, Cause area. The associated table can be, for example, Entity \[sn\_grc\_profile\] or Citation \[sn\_compliance\_citation\] table. The area type determines the list that you select from on the case. The table sets the records that you can select, and the order sets the sequence. The application provides configurations for entities, locations, users, companies, configuration items, citations, policies, policy statements, risk events, controls, and departments.

7.  Select **Save**.

    The subtypes, rules, jurisdictions, and area configurations are saved.


