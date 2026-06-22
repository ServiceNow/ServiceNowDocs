---
title: Manage the workspace configuration for a Change request in Service Operations Workspace
description: Utilize the new table-based configuration to align with the Service Operations Workspace Dynamic Overview Pages with the change process of your organization.Configure the layout of the overview page for Change Management in Service Operations Workspace.Configure or modify fields for change overview cards containing forms to display the fields that you need in the change request form in Service Operations Workspace.Show the activity stream bar for a for a change request in Service Operations Workspace.Configure the order of the cards that display in the Overview section for a change request in Service Operations Workspace.You can configure if the Work notes or Additional comments sections to display for a change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/configure-sow-chg-dynamic-overview-pages.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Change Management, IT Service Management]
---

# Manage the workspace configuration for a Change request in Service Operations Workspace

Utilize the new table-based configuration to align with the Service Operations Workspace Dynamic Overview Pages with the change process of your organization.

These configuration options allow users to define how the Dynamic Overview pages render throughout the change life cycle. This includes configuration options for overview pages, contextual sidebar and activity stream behavior for each state.

**Note:** To create a custom section, add new change overview cards. For information on modify the layout and formatting of the sections, see [UI Builder tutorial.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/uib-tutorial.md)

With this you can configure the following components in the workspace configuration:

-   Control the display of the cards in the contextual side panel
-   Control the order of the cards to be displayed in the Overview pages
-   Control the display of activity stream bar in the Overview pages
-   Configure the journal fields

**Parent Topic:**[Using Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/using-change-management.md)

## Configure change overview container and cards

Configure the layout of the overview page for Change Management in Service Operations Workspace.

### Before you begin

Role required: admin

### About this task

You can configure the layout of the overview page of the change request form in the Service Operations Workspace layout using the overview containers. You can configure different layouts for different change states or change models. Within each overview container, you can define multiple overview cards in a specific order. You can set conditions so that each change model displays specific cards in each form at every stage of the change request process.

Overview cards can be reused across various Overview Containers and Overview Containers can be reused across multiple change models. Names of Overview Containers and cards must be consistent with the layout and feature.

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Overview** &gt; **Workspace Configuration** &gt; **Overview Container**.

2.  Select **New** to add a new container.

3.  Provide information in the fields on the Change Overview Container page.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Overview Container.|
    |First to match order|Enter the order in which the Overview Container is evaluated when multiple containers match. Lower values are evaluated first.|
    |Table|Table to which the overview container applies. Defaults to Change Request table.|
    |Application|Application where the display is being configured. Global is the default application.|
    |Active|Select this option to make the overview container available when you create a change request.|
    |Display action bar|Select this option to display the activity panel at the bottom of the Overview page, when you create a change request.|
    |Use advanced condition|Select this option to add a script that defines an advanced condition for displaying the card.|
    |Condition|Fields and conditions that define when the overview container is displayed for each state.|

4.  Select **Submit** to save the change overview container with details provided.

5.  In the Change Overview Cards section, select **New** to add a card.

6.  Provide information in the fields on the Change Overview Card page.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the overview card.|
    |Chg overview container|Name of the associated change overview container.|
    |Display order|Order in which the card is displayed.|
    |Application|Application where the display is being configured. Global is the default application.|
    |Active|Select this option to activate the Change Overview Card in SOW when you create a change request.|
    |Expanded|Select this option to display the card in expanded form when you create a change request. If you clear this option, the card is displayed in compact form.|
    |Display for new record|Select this option to display the card for New \(Draft\) change request records..|
    |Heading|Heading of the change overview card displayed in the change request form.|

7.  Select **Submit** to save the change overview card with details provided.


### What to do next

To configure the fields for the overview page in change request page in Service Operations Workspace, see [Configure the fields for change overview cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/configure-sow-chg-dynamic-overview-pages.md).

For information on how to configure new fields, related lists, and other elements in the Details page, see [Create a custom field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateCustomField.md).

You can configure contextual side panel or journal fields for the change request form. For more information, see [Manage the workspace configuration for a Change request in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/configure-sow-chg-dynamic-overview-pages.md).

## Configure the fields for change overview cards

Configure or modify fields for change overview cards containing forms to display the fields that you need in the change request form in Service Operations Workspace.

### Before you begin

You can configure which fields are displayed within Service Operations Workspace \(SOW\) by configuring the SOW View of the form. You must create the sections using change overview cards before you can configure the fields. For more information, see [Configure change overview container and cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/configure-sow-chg-dynamic-overview-pages.md).

Role required: personalize\_form

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Create New**.

2.  In the change form context menu, select **Configure** &gt; **Form Layout**.

3.  Select the **SOW-Change-Overview** option in the View name field to modify the Overview page for change request form in SOW.

4.  Select **Edit this section in the Change Management for Service Operations Workspace**.

5.  Select the section for which you want to configure fields.

6.  Create new fields or add existing fields to the form.

7.  Provide field name, type and length in the Create new field section, and then select **Add** to add the new field in list of available fields.

    You can then move the newly added field to the Selected list.

8.  Move the fields that you want to display from the Available list to the Selected list, and reorder them as needed within the Selected list.

9.  Select **Save**.


## Show the activity stream bar

Show the activity stream bar for a for a change request in Service Operations Workspace.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Workspace Configuration** &gt; **Overview Container**.

2.  Select a state.

3.  On the Change Overview Container form for the selected state, enable **Display action bar**.

4.  Right-click on the form header and select **Save**.

    The action bar is shown on the Service Operations Workspace at the bottom of the screen.

    \[Omitted image "display-action-bar.png"\] Alt text: Action bar in change request record


## Configure the order of the cards in Overview section

Configure the order of the cards that display in the Overview section for a change request in Service Operations Workspace.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Workspace Configuration** &gt; **Overview Card**.

2.  Right-click on Chg overview container column, and select **Group By Chg overview container**.

3.  Select a state.

4.  In the **Change Overview Cards** section, modify the order of the overview cards using **Display order**.

5.  Right-click on the form header, and select **Save**.


## Configure the journal field of a change request

You can configure if the **Work notes** or **Additional comments** sections to display for a change request.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Workspace Configuration** &gt; **Overview Journal Field**.

2.  Select a Chg overview card.

3.  In the **Change Overview Fields** section, to delete select the journal field, and select **Delete** from **Actions on selected rows.**

4.  Right-click on the header and select **Save**.


