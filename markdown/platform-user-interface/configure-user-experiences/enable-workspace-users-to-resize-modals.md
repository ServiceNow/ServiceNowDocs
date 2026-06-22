---
title: Resize all record page modals in Configurable Workspace
description: Configure the Enable Resize property in UI Builder to enable resizing for all record page modals in your Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-user-interface/configure-user-experiences/enable-workspace-users-to-resize-modals.html
release: yokohama
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Resize all record page modals in Configurable Workspace

Configure the **Enable Resize** property in UI Builder to enable resizing for all record page modals in your Configurable Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Open a record page in UI Builder.

    1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

    2.  Open an experience to work in or create an experience by selecting **+ Create**.

        See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

    3.  Open or create a record page in the experience.

        For more information on creating a record page in UI Builder, see [Learning UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/ui-builder/learning-uib.md).

2.  Enable resizing for a modal.

    1.  Select the **Modal Container**.

    2.  Select **Enable Resize**.

    3.  Enter a minimum resize height and width.

    4.  Select **Save**.

    If resizing isn’t required for all record page modals, use declarative actions to enable resizing for select modals. For instructions, see [Set up resizing for select modals in your Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-user-interface/configure-user-experiences/set-up-resizing-for-select-modals-in-configurable-workspace.md).


