---
title: Link a new Issue Page Configuration record to a workspace
description: Create a new Issue Page Configuration record and link it from the classic user interface to the desired workspace. After linking the Issue Page Configuration record, the workspace view displays the new settings in the Issues overview landing page.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Issue Page Configuration module, Landing Page Configurations module, Common GRC features, Governance, Risk, and Compliance]
---

# Link a new Issue Page Configuration record to a workspace

Create a new Issue Page Configuration record and link it from the classic user interface to the desired workspace. After linking the Issue Page Configuration record, the workspace view displays the new settings in the Issues overview landing page.

## Before you begin

To link a new configuration to the desired workspace, you have to update the **issuePageConfigId** property for the workspace.

Role required: sn\_grc.admin

## About this task

When a new issue configuration is created and saved in the Issue Page Configurations record, it is displayed in the workspace only after linking it to the desired workspace.

## Procedure

1.  Create a new issue configuration in the Issue page configurations record.

    For instructions, see [Create a new Issue Page Configuration record](../../grc-common/task/create-new-issue-page-configuration.md).

2.  Copy the sys\_id of the new configuration and keep note of it.

    You will later use the sys\_id to update the Issue Page Configuration record.

3.  Navigate to the Experiences list in the classic user interface.

4.  From the UX Applications list, select the workspace where you want to integrate the change.

5.  In the selected workspace, select the **issuePageConfigId** property.

6.  On the issuePageConfigId property page, set the **Value** field to the sys\_id of the new configuration, and click **Save**.

    **Note:** Multiple configuration records can be configured in the workspace. But only the configuration record for which the sys\_id is configured in the **issuePageConfigId** property is displayed in the workspace.


## Result

The new issue page configuration setting is displayed in the desired workspace view.

**Parent Topic:**[Issue Page Configuration module](../concept/issue-page-config-record.md)

