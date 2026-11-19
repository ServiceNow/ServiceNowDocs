---
title: Add details to desktop actions in AI Desktop Actions
description: Add desktop action details, such as name, description, and associated applications, and review inputs and outputs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/add-details-desktop-action-ad.html
release: zurich
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 2
breadcrumb: [Design defined-path desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Add details to desktop actions in AI Desktop Actions

Add desktop action details, such as name, description, and associated applications, and review inputs and outputs.

## Before you begin

-   Capture your automation steps. For more information, see [Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/auto-create-desktop-action-ad.md) or [Extend a desktop action by manually capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/manual-create-desktop-action-ad.md).
-   Configure the properties for screens, anchors, and steps. For more information, see [Screen, anchor, and step properties in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/screen-anchor-and-action-properties-ad.md).

Role required: sn\_aia.admin

## Procedure

1.  In the Design workspace, select the Details tab.

    \[Omitted image "details-tab-ad.png"\] Alt text: AI Desktop Actions details tab displaying name, description, application, and many other fields, along with inputs and outputs.

2.  In the Desktop action details section, edit the name of the desktop action.

    The description in the **Action description** field is auto-filled when you select the **Record with AI** option and an AI badge appears.

3.  In the **Application** list, select the applications you want to automate.

    The list displays the applications available on the ServiceNow instance. If an application isn't listed, you can add it by selecting the **Add** icon \[Omitted image "ad-add-app-icon.png"\] Alt text:.

4.  In the Input and output parameters section, review the parameters related to steps for each screen.

5.  Select **Save**.

    You can save the desktop action after all the required fields are configured.


## What to do next

Test and activate the desktop action so that it’s available as a tool in the AI Agent Studio. You can add this tool to the AI agents that execute desktop actions in your desktop environment. For more information, see [Test and activate a desktop action in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/test-activate-desktop-action-ad.md).

