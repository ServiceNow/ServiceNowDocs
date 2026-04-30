---
title: Manage the workspace configuration for a Change request in Service Operations Workspace
description: Utilize the new table-based configuration to align with the Service Operations Workspace Dynamic Overview Pages with the change process of your organization.Show the activity stream bar for a for a change request in Service Operations Workspace.Configure the order of the cards that display in the Overview section for a change request in Service Operations Workspace.You can configure if the Work notes or Additional comments sections to display for a change request.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Change Management, IT Service Management]
---

# Manage the workspace configuration for a Change request in Service Operations Workspace

Utilize the new table-based configuration to align with the Service Operations Workspace Dynamic Overview Pages with the change process of your organization.

These configuration options allow users to define how the Dynamic Overview pages render throughout the change life cycle. This includes configuration options for overview pages, contextual sidebar and activity stream behavior for each state.

**Note:** You can configure the layout of default sections containing forms in the configure forms section.

You can also create custom sections. To create a section use the UI builder. For more information, see [UI Builder tutorial](https://www.servicenow.com/docs/access?context=uib-tutorial&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

For a custom section, add a corresponding overview card record to display the section in the required container. The custom section must be created in the **Chg Overview Viewport SNC** page, and the name of the custom section must match with the choice list value for the overview card.

With this you can configure the following components in the workspace configuration:

-   Control the display of the cards in the contextual side panel
-   Control the order of the cards to be displayed in the Overview pages
-   Control the display of activity stream bar in the Overview pages
-   Configure the journal fields

**Parent Topic:**[Using Change Management](../../change-management/concept/using-change-management.md)

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

    ![Action bar in change request record](../image/display-action-bar.png)


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


