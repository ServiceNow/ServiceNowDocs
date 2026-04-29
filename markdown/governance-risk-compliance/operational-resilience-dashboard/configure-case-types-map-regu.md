---
title: Map regulations to the entities
description: Map single or multiple regulations with the entity linked to an incident or security incident.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Using Digital resilience incident reporting, Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Map regulations to the entities

Map single or multiple regulations with the entity linked to an incident or security incident.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_dri\_inc\_rptg.digital\_resilience\_incident\_admin

## About this task

The Digital Resilience Incident Case module in the Operational Resilience Workspace lists all Digital Resilience Incident Cases associated with an incident or security incident. A new Regulation Mappings related list, now available in each Digital Resilience Incident Case record, displays the relationships between entities related to the cases and their corresponding regulations.

## Procedure

1.  Navigate to **All** &gt; **Digital Resilience Incident Reporting** &gt; **Digital Resilience Incident Case Type** and open the desired case record.

    The Digital Resilience Incident Case record is displayed.

    ![Digital Resilience Incident Case record.](../image/dri-case-record.png)

    It contains the following tabs for the record:

    -   **State Model**: The state model and action task state model specify the workflow states and transition conditions for a record type and an action task, respectively. A record type and an action task follow the workflow states configured in their respective state models.
    -   **Assessment Configuration**: Assessment templates are pre-defined formats to request responses from assessors or reviewers that help to evaluate the record.
    -   **Template Configuration**: Document templates are set up for generating word reports.
    -   **Inbound Email Configuration**: Group email configuration is set up to inform the group members about the case record.
    You can configure the following related lists as outlined in the next steps.

    -   Subtypes
    -   View Rules
    -   Assignment Rules
    -   Jurisdictions
    -   Record type area configs
    -   Regulation Mappings
2.  To map a regulation to an entity associated with the case, select **New** in the Regulation Mappings related list.

    The Regulation Mappings New record is displayed.

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Entity|Name of the entity, for example, Acer.|
        |Regulation|Regulation that is mapped to the entity associated with the case, for example, Digital Operational Resilience Act.|
        |Record type|Digital Resilience Incident Case record. This field is auto-filled.|

        The example illustrates mapping the Acer entity to the 'Digital Operational Resilience Act' \(a single regulation\). However, entities can also be mapped to multiple regulations.

        ![Mapping an entity to a single regulation.](../image/reg-mapping-new-record-regulations-added.png)

3.  To add a subtype for the case, navigate to the Subtypes related list and select **New**.

    1.  Add the parameters such as Label, Name, Parent, Category, and Description.

        The following example shows a Subtypes record.

        ![Subtypes record.](../image/casetype-subtype-new-record.png)

    2.  To mark the record as active, set the Active option.

    3.  Select **Submit**.

4.  To set up rules, navigate to the View Rules related list and complete the substeps.

    1.  Add Name, Table, View, Workspace type, and Execution Order number.

        The following example shows a Rules record.

        ![Rules record.](../image/casetype-viewrule-sample-record.png)

    2.  Set the Active flag.

    3.  Set up the roles and conditions in the **Conditions** tab.

    4.  Select Hide details &amp; UI actions, Hide section navigation, and Disable section collapsing in the **Form Settings** tab.

    5.  Set up the Default tab order and focus in **Form Tabs**.

    6.  Select **Submit**.

5.  To assign tasks to specific users and groups automatically, navigate to the Assignment Rules related list and set up the assignment rules.

    The following example shows an Assignment rules record.

    ![Assignment rules record.](../image/casetype-assignrule-sample-record.png)

    1.  Add the name of the rule and set the Active flag.

        The name of the application is auto-filled as Digital Resilience Incident Reporting.

    2.  Select a table in **Applies to** and specify the conditions that must be met before the task is assigned to the user or group.

        The rule is applied only if the task isn’t already assigned to another user or group.

    3.  To assign a task to the users or groups, configure the users or groups in the **Assign to** tab.

    4.  To customize the assignment rule further, enter a script in the **script** tab.

        Scripts provide access to the pool of current variables.

    5.  Select **Submit**.

6.  To set up the location details and jurisdiction of the case, navigate to the Jurisdictions related list and select **New**.

    The following example shows a Jurisdictions location record.

    ![Jurisdictions record.](../image/casetype-Juris-sample-record.png)

    1.  Add Name, City, Zip code, State, country, Phone, Latitude, Longitude details.

    2.  Select **Submit**.

    3.  To edit an existing Jurisdictions record, select **Edit**.

7.  To define the area type for the case and the table associated with it, navigate to the Record type area configs related list and complete the substeps.

    The following example shows a Record type area configuration record.

    ![Area configs record.](../image/casetype-areatype-sample-record.png)

    1.  Set its order and Active flag.

    2.  Select **Submit**.

    The area type can be Impacted area, Related area, Cause area. The associated table can be Entity \[sn\_grc\_profile\] or Citation \[sn\_compliance\_citation\] table.

8.  Select **Save**.

    The regulation mappings, subtypes, rules, and other details for the entity are saved in the case record.


**Related topics**  


[Complete action tasks and report incidents associated with regulations](work-on-action-tasks.md)

