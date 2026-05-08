---
title: Configure the incident record page in SOW for ITSM
description: Configure the data displayed in various incident tabs such as Overview and Details tabs.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Record page configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
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
            -   This option is available only if the **glide.ux.user\_criteria\_enabled** property is **true**. For more information, see Enable the user criteria property.
        -   Summary: Configure the fields layout, UI elements and the visible data content on the Summary section of the **Overview** tab.
        -   Impact: Configure the fields layout, UI elements and the visible data content on the Impact section of the **Overview** tab.
        -   Cause: Configure the fields layout, UI elements and the visible data content on the Cause section of the **Overview** tab.
        -   Resolution: Configure the fields layout, UI elements and the visible data content on the Resolution section of the **Overview** tab.
    -   Details: Configure any of the following options for the **Details** tab.
        -   Record: Provides further details on the incident record. Configure the fields layout, UI elements, and the visible data content of the **Details** tab using form builder.
        -   New record: This layout appears when an agent creates an incident record. Configure the fields layout, UI elements, and the visible data content of the **Details** tab using form builder.
    -   Response templates: Create and configure response templates for incidents. Response templates are used as reusable messages that you can copy and paste in the required areas such as email or chat for a quick response. To use the response template feature, the users must have the sn\_templated\_snip.template\_snippet\_reader role. The number of the response templates created for the incident table is displayed in this section. For more information on defining and configuring the response templates for incident tables in Service Operations Workspace, see Response templates.
    -   Incident management properties: Configure the incident features using the incident management properties. For more information on configuring incident management properties, see [Incident Management properties](../../incident-management/reference/incident-management-properties.md).
    For more information about configuring the field layout, UI elements and the visible data content using form builder, see Customize forms within a form component.

    For information about incident record page customizations, see [Customize the incident record page](../concept/customize-the-incident-record-page.md#).


**Parent Topic:**[Record page configurations in Service Operations Workspace for ITSM](../concept/record-page-configurations-sow-itsm.md)

