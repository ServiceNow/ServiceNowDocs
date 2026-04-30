---
title: View and update incident information on the Overview tab in SOW
description: View and update the incident information, such as summary, impact, cause, and resolution, from the Overview tab. This incident information helps you analyze the issue and resolve the incident quickly.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Incident Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# View and update incident information on the Overview tab in SOW

View and update the incident information, such as summary, impact, cause, and resolution, from the **Overview** tab. This incident information helps you analyze the issue and resolve the incident quickly.

## Before you begin

An incident must be created. For more information, see [Create an incident in Service Operations Workspace](create-incident-sow.md).

Role required: itil or service\_desk\_agent or incident\_read

## About this task

Review the incident information on the **Overview** tab. If necessary, you can edit or add information.

## Procedure

1.  On an incident record, select the **Overview** tab.

2.  On the Summary section, add or edit the information as needed.

    1.  Select the **Edit summary** \(![Edit summary icon](../image/mim-edit-icon.png)\) icon to edit the fields.

    2.  On the form, fill in the details.

<table id="table_q2v_phj_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description of the incident.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation on the incident.

</td></tr><tr><td>

Number

</td><td>

The unique system-generated incident number. This is a read-only field.

</td></tr><tr><td>

Priority

</td><td>

How quickly the service desk should address the task. The **Priority** field is calculated based on the **Impact** and **Urgency** fields.

</td></tr><tr><td>

Opened

</td><td>

The date and time when the incident was created. This is a read-only field.

</td></tr><tr><td>

Impact

</td><td>

Level of impact that the incident has on the business. Possible values:-   1-High
-   2-Medium
-   3-Low
**Note:** When you modify the value in the **Impact** and **Urgency** fields and save the record, a Record update pop-up window is displayed where you must enter the **Work notes** information to proceed further.

</td></tr><tr><td>

Urgency

</td><td>

Level of urgency the incident requires to be resolved. Possible values:-   1-High
-   2-Medium
-   3-Low
**Note:** When you modify the value in the **Impact** and **Urgency** fields and save the record, a Record update pop-up window is displayed where you must enter the **Work notes** information to proceed further.

</td></tr><tr><td>

State

</td><td>

Different states through which the incident proceeds during its life cycle. Possible values: -   New
-   In progress
-   On Hold
-   Resolved
-   Canceled
**Note:**

-   When you select the **On Hold** state and save the record, a Record update pop-up window appears where you must select the **On hold reason** field and enter the **Additional comments**.
-   When you select the **Resolved** state and save the record, a Record update pop-up window appears where you must select the **Resolution code** field and enter the **Resolution notes** to proceed further.


</td></tr><tr><td>

Major Incident state

</td><td>

State of the Major incident. **Note:** This field is available only if the Major Incident Management for Service Operations Workspace \(sn\_sow\_mim\) plugin is installed and active. For more information, see [Setting up Major Incident Management in Service Operations Workspace](../concept/setup-mim-sow.md).

</td></tr><tr><td>

Caller

</td><td>

User who reported the incident.

</td></tr><tr><td>

Link

</td><td>

URL that you can click to open on a new tab for more information on the issue. Overview page supports "URL" type of field in read-only mode.**Note:** This field is not available in the base system. But you can customize the form to add a field with a custom field label and add a URL.

</td></tr></tbody>
</table>    3.  Select the **Save Summary** \(![Save icon](../image/mim-save-icon.png)\) icon.

3.  On the Impact Summary section, edit the information as needed.

    1.  Select the **Edit impact summary** \(![Edit summary icon](../image/mim-edit-icon.png)\) icon.

    2.  On the form, fill in the details.

        |Field|Description|
        |-----|-----------|
        |Configuration item|Primary configuration item that is impacted.|
        |Service|Primary business service that is impacted.|
        |Service offering|Consists of one or more service commitments that uniquely define the level of service in terms of availability, scope, pricing, and packaging options. Service offering enables you to receive different features and their levels of performance for a given service.|
        |Business impact|Impact of the incident on the business.|

        For the reference fields such as **Configuration item**, **Service offering** and **Service**, you can perform the following actions:

        -   Select the **Preview record** icon \(![Preview icon](../image/inc-preview-record.png)\) to display a preview of that record information on the same page. If necessary, you can also select **Open record** to open the record on a separate tab.
        -   Select the **Dependency view** icon \(![Dependency icon](../../incident-management/image/dependency-icon-r.png)\) to view the unified dependency CMDB map in a new tab within the workspace view.
        **Note:** Selecting any empty reference field such as **Configuration item**, **Service offering** and **Service** in SOW displays only the recent selection values instead of automatic searching and displaying the results of the field values available in the system. This change increases the overall performance of the reference fields. This change is applicable only to reference fields with no field values. By default, this change is enabled. To revert this change, set the **Reference search on click** \(**ref\_search\_on\_click**\) UX page property to set to `true`.

    3.  Select the **Save Impact Summary** \(![Save icon](../image/mim-save-icon.png)\) icon.

4.  On the **Location** field of the Impact section, select **View impacted locations** to view the impacted locations and users on a world map in a separate tab.

    The **Impacted location** tab displays the following information:

    -   Number of impacted users – Number of users impacted by the incident.

        **Note:** The number of impacted users is calculated based on the following data sources:

        -   Caller of the incident.
        -   Callers of the child incidents.
        -   Service offerings associated with the Incident. This source is only used if Service Portfolio Management Foundation is activated and being used. For more information, see [Activate Service Portfolio Management](../../service-portfolio-management2/task/activate-SPM2-plugin.md).
    -   Number of impacted locations – Number of unique locations calculated based on the number of users.
    -   Impact world map – Map of impacted locations marked on the world map along with the impacted users. You can view the impacted users counts and details at these locations. You can further narrow down to the continent, country, state, or city level.
    **Note:**

    -   The Location section is available only if the Major Incident Management for Service Operations Workspace \(sn\_sow\_mim\) plugin is installed and active, and if the incident is a major incident. For more information, see [Major Incident Management in Service Operations Workspace](../concept/mim-in-sow.md).
    -   You can add multiple locations from the Affected location related list in the **Related records** tab of the Major incident record.
5.  Select the following cards to add or update the configuration items associated with the Incident.

    1.  Select the **Affected CIs** card to add or remove the configuration items \(CI\) that are affected by the incident.

    2.  Select the **Impacted Services/CIs** card to add or remove the Configurations items or Services impacted by the incident.

    3.  Select the **Assets** card to add or remove the configuration items that users use as assets.

    You can search and filter the Configuration Items \(CI\) based on the configuration class when you add the affected CIs to an incident record.

    When adding a list containing more than 50 child incidents, affected CIs, impacted services/CIs or assets, the Multiple Record Associator \(MRA\) component batch processes in async and helps adding them in background thereby increasing the overall performance of the system. This feature works only if the number of items to be added is more than 50 as the **async Threshold** configuration property is set to 50.

    **Note:** The child incidents are added from the Child incidents related list in the **Related records** tab while the affected CIs, impacted services/CIs or assets are added from the **Overview** tab of an incident record.

6.  On the Cause section, add or update the cause of the incident.

    1.  Select **Add cause**.

    2.  Enter **Probable cause** of the incident.

    3.  Select **Save cause** \(![Save icon](../image/mim-save-icon.png)\) icon.

7.  On the Resolution section, add the resolution information to resolve the incident.

    **Note:** Populate the values in this section only when the incident is ready to be resolved.

    1.  Select **Add resolution**.

    2.  On the form, fill in the details.

        |Field|Description|
        |-----|-----------|
        |Resolution code|Category in which the incident is resolved.|
        |Resolution notes|Details on how the incident is resolved.|

    3.  Select the **Save resolution** \(![Save icon](../image/mim-save-icon.png)\) icon.

8.  On the Compose section, post messages to the activity stream and send emails to stakeholders.

    1.  Enter and post the **Work notes \(Private\)** message to the activity stream.

        **Note:**

        By default, the **Work notes \(Private\)** option is selected for you to enter and post the message.

    2.  Enter and post the **Additional comments \(Customer visible\)** message to the activity stream.

    3.  Enter and post the **Action taken** on the major incident to the activity stream.

    4.  **Compose** and then **send Email** to the stakeholders.

    -   The activity stream supports the following features:
        -   The activity stream in the **Overview** and **Details** tab displays the activity information in tiles that are collapsible. By default, the latest event activity tile, if a work note or additional comment, is expanded and the other consecutive event activity tiles are collapsed. The collapsed tile only displays the time stamp and the activity event source name. This ensures a clean UI and enables you to expand and view the activity information when required. To enable this feature, set the **Enable the expandable activity stream tiles** \(**enableExpandableActivityStreamTiles**\) UX page property to `true`.
        -   An internal tag is added for the work notes.
        -   You can define, customize, and apply tags to the activity streams. These tags help you search and filter the activity based on the tags. By default, no pre-defined tags are available in the base system. However, you can use the **Activity stream property** \(**activitystreamprops**\) UX Page Properties for SOW to define and customize your tags for incident records. For more information, see [Define and customize activity stream tags](define-customize-activity-stream-tags.md).
    -   For reference fields in SOW record pages, the following glide list actions are available:
        -   Add me \(![Add me icon](../../incident-management/image/add-me.png)\) icon: Add the logged in user to the field. This option is available for reference fields where you can add current user \(sys\_user\). For example, Watch list or Work note list fields.
        -   Remove me \(![](../../digital-product-release/image/dpr-icon-release-remove.png)\): icon Remove the logged in user from the field. This option is available for reference fields where you can remove current user \(sys\_user\). For example, Watch list or Work note list fields.
        -   Add multiple users \(![Little persons image](../../site-reliability-ops/image/icon-3-persons.png)\) icon: Add multiple users to the field. This option is available for reference fields where you can add multiple users \(sys\_user\). For example, Watch list or Work note list fields.
        -   Add multiple records \(![Add icon](../../incident-management/image/add_icon.png)\) icon: Add multiple records to the field. This option is available for reference fields where you can add multiple records of any table. For example, Problem or Change request field.

**Parent Topic:**[Incident Management in Service Operations Workspace](../concept/incident-sow.md)

**Related topics**  


[Create an incident in Service Operations Workspace](create-incident-sow.md)

[Viewing incident record information using the Contextual side panel](../concept/view-inc-record-info-contextual-sidepanel.md)

[Work on an incident list page in Service Operations Workspace](work-incident-list-page-sow.md)

[Work on an incident record in Service Operations Workspace](work-on-incident-sow.md)

[Remedial actions using Playbook](../concept/remedial-actions-playbook.md)

[Close resolved incident](close-resolved-incident-sow.md)

[Reopen an incident in Service Operations Workspace](reopen-incident-sow.md)

[Incident Management in Service Operations Workspace reference](../concept/sow-im-reference.md)

