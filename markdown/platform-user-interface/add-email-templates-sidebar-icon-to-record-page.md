---
title: Set up email templates on the record page
description: If your workspace does not use the latest version of the standard record page, add the email templates tab manually in UI Builder.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up email templates in Configurable Workspace, Administering emails in Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Set up email templates on the record page

If your workspace does not use the latest version of the standard record page, add the email templates tab manually in UI Builder.

## Before you begin

Role required: email\_client\_admin

If your workspace is built using the standard record page, the email templates tab is available by default and manually adding the email templates tab in UI Builder is not needed.

## Procedure

1.  Open a record page in UI Builder:

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

    2.  Open an experience to work in or create an experience by selecting **+ Create**.

        See [Configure how users interact with your applications in UI Builder](https://www.servicenow.com/docs/access?context=work-experiences&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) for more information on creating experiences.

    3.  Open or create a record page in the experience.

        For more information on creating a record page in UI Builder, see [Learning UI Builder](https://www.servicenow.com/docs/access?context=learning-uib&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

2.  Add a tab for email templates to the sidebar by selecting **+ Add component** under the Tab sidebar.

3.  Add a **Tabs** component.

4.  In the Tab Settings panel, add the following settings for each field.

    |Field name|Configuration|
    |----------|-------------|
    |**Tab label**|Enter `Email Templates`.|
    |**Icon**|Select **Envelope Plus Outline**.|
    |**Hide tab**|Enter `IF(@data.record.isEmailClientEnabled,false,true)`.|

5.  Select **Create**.

6.  Configure Agent Assist to apply contextual search:

    1.  Navigate to **Tab sidebar** &gt; **Email Templates \(Flex\)**.

    2.  Select **+ Add component**, and select **Agent Assist**.

    3.  **Note:** If Agent Assist presets are available, the following fields will auto-fill. These steps are only needed if Agent Assist presets are not available.

        Change the **Table config** property to `Email Templates [global]` in the Agent Assist panel.

    4.  Open the **Events** tab, and select **+ Add event handler** under Apply Email Template.

7.  **Note:** If Agent Assist presets are available, this field will auto-fill. This step is only needed if Agent Assist presets are not available.

    Select **\[Record\] Request Email Action**, and configure the following properties within its panel.

    |Field name|Configuration|
    |----------|-------------|
    |**Sys ID**|Enter `-2`.|
    |**Target table**|Enter `@payload.params.sysparm_parent_table`.|
    |**Target record**|Enter `@payload.params.sysparm_parent_sys_id`.|
    |**Reply Type**|Enter `@data.record.activityStream.composeEmailInfo.replyType`.|
    |**Reply ID**|Enter `@data.record.activityStream.composeEmailInfo.replyId`.|
    |**Should focus email tab**|Select to activate.|
    |**Template details**|Enter `@payload.templateDetails`.|


