---
title: Assign bot process to an automation project
description: Assign a bot process to an automation project in RPA Desktop Design Studio to start using the bot process resources.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [assign bot process in rpa desktop design studio]
breadcrumb: [Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Assign bot process to an automation project

Assign a bot process to an automation project in RPA Desktop Design Studio to start using the bot process resources.

## Before you begin

Role required: sn\_rpa\_fdn.rpa\_developer or sn\_rpa\_fdn.rpa\_admin, if running from RPA Desktop Design Studio

## About this task

The Assign Bot Process feature is enabled for all automation projects including skills. It shows both attended and unattended bot processes in the **Bot process** field.

To access resources \(Queues, Process Parameters, and so on\) limited to a specific bot process within the automation from RPA Desktop Design Studio, the **Assign bot process** option helps in selecting the bot process and there by accessing resources to successfully run the automation in RPA Desktop Design Studio.

## Procedure

1.  From the **Design** tab of RPA Desktop Design Studio, select **Assign bot process**.

    The Assign Bot Process dialog box is displayed.

2.  Select the required bot process from the **Bot Process** list.

    **Note:** The users who are a part of the Managed by Group for the respective bot process, those bot processes are also displayed in this list.

3.  If the selected bot process is enabled with Embedded Task Automation, fill in the following required fields.

<table id="table_dx1_xs5_11c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Attended Config

</td><td>

The attended configurations that are associated with the selected bot process in step 2, are displayed here.Select an attended configuration.

</td></tr><tr><td>

Record Context

</td><td>

Enter the Sys ID or URL of the ServiceNow form record. This helps you to fetch field values using GetProcessFieldParameters component and update field values using SetProcessFieldParameters component of the selected Sys ID.

For more about getting the Sys ID or URL, see [Unique record identifier \(sys\_id\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_UniqueRecordIdentifier.md).

</td></tr></tbody>
</table>    **Note:** For more information about Embedded Task feature, see [Embedded Task Automation \(ETA\) in RPA Hub](../../rpa-hub/concept/embedded-task-auto-rpa.md).

4.  For unattended bot process, select the required robot from the **Robot** list.

    You can select the robots that are assigned to the bot process.

    **Note:** Starting from the Vancouver release of RPA Desktop Design Studio, for unattended automations, you can view only those robots from the bot process that are mapped to your user role. The robot must also have your machine name where RPA Desktop Design Studio is running. If there are no robots associated to the bot process, then an error is displayed.

5.  Select **OK**.

    If one or more skills are overridden in the bot process, the automation uses the updated skill version during current execution. For more information about overridden skill versions, see [Override a skill version for a bot process in RPA Hub](../../rpa-hub/task/override-skill-version-rpahub.md).


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

