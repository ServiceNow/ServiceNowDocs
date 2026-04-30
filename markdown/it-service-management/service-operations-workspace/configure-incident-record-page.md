---
title: Configure the incident record page in SOW for ITSM
description: Configure the data displayed in various incident tabs such as Overview and Details tabs.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Record page configurations in SOW for ITSM, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the incident record page in SOW for ITSM

Configure the data displayed in various incident tabs such as **Overview** and **Details** tabs.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  On the **Configurations** tab, select the **Incident Management** option.

3.  Select **Incident record** and then select **Configure** to configure any of the following tabs.

    -   Overview: Configure any of the following options for the **Overview** tab.
        -   Tab visibility for tier 1 agents: Configure the visibility settings to display the **Overview** tab for the tier-1 agents. You can also configure the user criteria to include or exclude users with other roles and user groups.

            **Note:**

            -   By default, the **Overview** tab is displayed for the tier-1 agents.
            -   When you choose to hide the **Overview** tab for the tier-1 agents, the **Details** tab opens by default.
            -   This option is available only if the **glide.ux.user\_criteria\_enabled** property is **true**. For more information, see [Enable the user criteria property](https://www.servicenow.com/docs/access?context=enable-user-criteria-property&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
        -   Summary: Configure the fields layout, UI elements and the visible data content on the Summary section of the **Overview** tab.
        -   Impact: Configure the fields layout, UI elements and the visible data content on the Impact section of the **Overview** tab.
        -   Cause: Configure the fields layout, UI elements and the visible data content on the Cause section of the **Overview** tab.
        -   Resolution: Configure the fields layout, UI elements and the visible data content on the Resolution section of the **Overview** tab.
    -   Details: Configure any of the following options for the **Details** tab.

        -   Record: Provides further details on the incident record. Configure the fields layout, UI elements, and the visible data content of the **Details** tab using form builder.
        -   New record: This layout appears when an agent creates an incident record. Configure the fields layout, UI elements, and the visible data content of the **Details** tab using form builder.
        For more information about configuring the field layout, UI elements and the visible data content using form builder, see [Customize forms within a form component](https://www.servicenow.com/docs/access?context=learn-by-example-edit-form-component&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


