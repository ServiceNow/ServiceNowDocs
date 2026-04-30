---
title: Log an injury and illness
description: Log an injury and illness that resulted from a health and safety incident.
locale: en-US
release: zurich
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Work on a safety incident, Manage incidents and observations, Manage incidents, observations, and anonymous safety concerns, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Log an injury and illness

Log an injury and illness that resulted from a health and safety incident.

## Before you begin

Role required: sn\_ohs\_im.manager, sn\_ohs\_im.agent, or sn\_ohs\_im.operations\_manager

## About this task

Add an injury and illness record for each affected person during the incident.

**Note:** If your admin has turned off the playbook and you're using a tab-based experience for safety incidents, you can associate multiple injuries and illnesses to a single incident. For more information, see [Disable the safety incident playbook](disable-safety-incident-playbook.md).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the incident management icon \(![Incident Management icon.](../image/list-icon-hs.png)\) and navigate to the **Lists** tab.

3.  Open a safety incident assigned to you to add the injury to.

4.  Select the **Report an incident** tab.

    The incident playbook opens.

5.  In the **Add injury and illness** activity, add the injury and illness.

    1.  Select **New**.

    2.  On the form, fill in the fields in the **Person**, **Healthcare**, and **Injury and illness details** sections.

        For field descriptions, see [Injury and illness fields](../reference/hs-injury-illness-form.md).

6.  Select **Save**.

    The injury picker section is enabled where you can add injuries on a human body.

7.  In the **What was the injury?** section, add the injury.

    1.  In the visual human body part picker, select the injured body part.

    2.  Fill in the fields and select **Save**.

        |Field|Description|
        |-----|-----------|
        |Severity|Seriousness of the injury.|
        |Affected body part|Body part that was injured.|
        |Description|Details of the injury.|

    3.  To add multiple injury types to the same body part, select **Add New Injury** and fill in the fields.

    4.  If there's more than one injury, select the other injured body parts and add their details like the earlier step.

    -   The selected body parts are highlighted on the injury picker based on the severity of the injury. For example, a red region on the body represents a serious injury.
    -   The color on an injury detail card matches with the highlighted color of the related body part.
8.  Select **Save**.

9.  Create an HR case for the injury or illness using the **Create HR Case** button, if needed.

    **Note:** This button appears only when the following conditions are met:

    -   Health and Safety Case Management \(sn\_hs\_cm\) application and the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin are installed on your ServiceNow instance.
    -   Safety case manager \[sn\_hs\_cm.case\_manager\] role assigned to you.
    -   **Employee** is selected in the **Person type** field.
    For more information, see [Create an HR case from an injury or illness](create-hr-case-injury-illness.md).

10. Create a return to work case for the person involved in this injury or illness using the **Create RTW Case** button, if needed.

    **Note:** This button appears only when the following conditions are met:

    -   Health and Safety Case Management \(sn\_hs\_cm\) application is installed on your ServiceNow instance.
    -   Safety case manager \[sn\_hs\_cm.case\_manager\] role assigned to you.
    -   **Employee** is selected in the **Person type** field.
    However, the button doesn't appear when the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is also installed on the instance.

    For more information, see [Create a return to work case from an injury or illness](create-rtw-case-injury-illness.md).

11. Research content related to the injury by selecting the Agent assist icon \(![agent assist icon](../../../common/image/Form_AgentAssistIcon.png)\).

    Agent assist searches the knowledge base using the text from the injury's **Injury description** field and shows relevant articles.


## Result

-   The injury is listed in the Injury and Illness section of the activity. The injury card also appears in the Injuries and Illnesses section in the **Incident Overview** tab.
-   The **Generate OSHA 301 form** button appears based on the following conditions:
    -   The Health and Safety Incident Management OSHA Content Pack \(com.snc.sn\_hs\_im\_osha\) application is installed on your ServiceNow instance.
    -   The **Recordable** option is selected on the injury and illness report.
    -   The safety compliance manager \[sn\_ohs\_im.compliance\_manager\] role is assigned to you.

## What to do next

If an asset was involved in this injury, add it in the next playbook activity.

**Parent Topic:**[Work on a safety incident](work-hs-incident-observation.md)

