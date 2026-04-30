---
title: Configure Shift Handover Templates
description: The Admin can define and configure different Shift Handover templates for the Shift Owner to create shift handover records and hand them over to the next shift team.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Shift Handover, Configuring SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Shift Handover Templates

The Admin can define and configure different Shift Handover templates for the Shift Owner to create shift handover records and hand them over to the next shift team.

## Before you begin

Role required:

-   sn\_escm\_sh.shift\_admin
-   sn\_si.admin inherits the sn\_escm\_sh.shift\_admin role

## About this task

To configure a Shift Handover template, the Admin either creates a new Shift Handover template or opens an existing template in the base system with the name **Sample Shift Template** and modifies the details and sections according to your requirements.

The Shift Owner can use the configured template to create Shift Handover log records, and then the Shift Handover report is shared with the next active Shift Owner and team.

**Note:** Only the active Shift Handover templates are visible for the Shift Owner to create handover log records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace** &gt; **Administration**.

2.  Navigate to **Shift Handover** &gt; **Template Configurations**.

    The Template Configurations page is displayed.

    **Note:** As a part of the base system, you’re provided with one predefined Shift Handover template configuration to view, edit, or modify the shift handover template. However, you can’t create or delete the predefined Shift Handover template configuration.

    ![Shift Handover Template Configurations](../image/shift-handover-landing.png "Shift Handover Template Configurations")

3.  To create a new Shift Handover template, select **New**.

4.  On the Details form, fill the fields.

<table id="table_mhk_bd3_pyd"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Shift Handover template. For example, SIR Template.

</td></tr><tr><td>

Application

</td><td>

Name of the application for which you’re creating the Shift Handover template. For example, Security Incident Response Workspace.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the Shift Handover template is active. Enable this option to activate the Shift Handover template.

</td></tr><tr><td>

Description

</td><td>

Description of the Shift Handover template.

</td></tr><tr><td>

Record mention configuration

</td><td>

Use this field to configure the Rich Text Editor's \(RTE\) record mention details. The input is an array of JSON objects with the following fields:-   `sourceTable`: Name of the source table.
-   `label`: Name of the label to be displayed.
-   `filterCondition`: Encoded query for filtering
-   `field`s: Select the fields to query the pattern
Sample configuration that you can copy and paste in the Record mention configuration field.

```
[
    {
        "sourceTable": "incident",
        "label": "Incidents",
        "filterCondition": "active=true",
        "fields": [
            "number"
        ]
    }
]
```

To copy the sample configuration, use the **Copy to clipboard** action in the Contextual Assistance pane. Then, you can make any additional modifications based on your requirements.

</td></tr><tr><td>

Template

</td><td>

Create a Shift Handover template using sections. Make sure that there is at least one section for the analysts to be able to contribute to the shift handover log records based on the template. The template can have static text, images, and so on, in the appropriate sections. You can copy and paste images directly in the Template field. You can create sections in the template using the following code:

```
${section:Section Label}
```

Example:

```
${section:Key Incidents/Events During Current Shift}
${section:Incidents/Events to Monitor or Follow Up}
${section:System/Infrastructure Updates}
${section:Next Steps for Incoming Shift}
${section:References}
```

**Note:** For more information, refer to the **Contextual Assistance** on the right-pane.

</td></tr></tbody>
</table>5.  To use and modify an existing Shift Handover template, select **Sample Shift Template**.

    ![Create a new Shift Handover template](../image/shift-handover-template.png "Shift Handover template")

6.  Update the Shift Handover template according to your requirements.

7.  Select **Preview** to view the runtime preview of the Shift Handover template.

    The report generates a preview based on the Shift Handover template configuration.

    ![Preview of the Shift Handover template](../image/shift-handover-preview.png "Preview of the Shift Handover template")

8.  Select **Save** to save the Shift Handover template.


## What to do next

To learn how to Manage Shift Handover records in the list view and perform actions like create, edit, copy, or delete Shift Handover records, see [Manage Shift Handover records](../concept/manage-shift-handover-records.md).

**Parent Topic:**[Configure Shift Handover](../concept/config-shift-handover.md)

**Related topics**  


[Create shifts through Security Incident Response Workspace](configure-shift-times.md)

