---
title: Assign the data steward role
description: Select a data steward to make decisions about data sharing with ServiceNow in Now Assist applications.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Assign, data steward, Now Assist, Generative AI, Gen AI, User Administration, sn\_generative\_ai.data\_steward]
breadcrumb: [Data sharing and processes, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Assign the data steward role

Select a data steward to make decisions about data sharing with ServiceNow in Now Assist applications.

## Before you begin

Role required: sys\_admin

## About this task

A data steward is responsible for determining whether prompts, inputs, and responses with generative AI in Now Assist applications on your instance are shared with ServiceNow.

The ServiceNow customer data sharing program allows you to provide data to improve ServiceNow AI products. This data helps improve prediction accuracy, enhance user experience, tailor products to your business needs, and reduce hallucinations for your activated Now Assist skills.

The following steps explain how to assign a role to a specific user. Another option is to make a group, such as "AI Data Stewards," assign the role to the group, and then put the user in that group. See [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and then open a user record.

2.  In the Roles related list, select **Edit**.

3.  In the collection of roles, select the sn\_generative\_ai.data\_steward role, and then select the **Add** \(![Button with a chevron](../../now-assist-platform/images/collection-add-icon.png)\) icon.

4.  Select **Save**.


## Result

Once the data steward has the correct role, they can review the data sharing information on the Now Assist Admin console in the **Settings** tab under **Data privacy and sharing** &gt; **Data sharing**.

**Parent Topic:**[Data sharing and processes](../concept/now-assist-data-sharing-and-processes.md)

