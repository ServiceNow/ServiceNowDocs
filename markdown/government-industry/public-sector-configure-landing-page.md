---
title: Configure the Public Sector landing page with UI Builder
description: Use the UI Builder to change certain fields in the Public Sector landing page of the CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSM Configurable Workspace, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Public Sector landing page with UI Builder

Use the UI Builder to change certain fields in the Public Sector landing page of the CSM Configurable Workspace.

## Before you begin

Role required: admin

## About this task

The Customer Service Management \(CSM\) landing page gives agents an overview of their new, assigned, and high-priority cases, plus the cases assigned to their groups. Replace certain fields in the landing page with fields relevant to Public Sector Digital Services. You can also add or change other fields as needed. For more information on using UI Builder to modify pages, see Work with pages.

## Procedure

1.  Navigate to **All** and in the filter, enter **UI Builder**.

2.  Select **UI Builder**.

3.  Navigate to the Customer Service Management \(CSM\) landing page:

    1.  In the list of **My experiences**, select the **CSM/FSM Configurable Workspace**.

    2.  In **UI Builder**, navigate to **Page** &gt; **Landing Page** and select **CSM Landing Page**.

        ![View of CSM landing page with fully customizable content.](../image/ps-csm-landing-page.png)

    3.  In the message displayed at the top of the page, select **Edit in original scope**.

        ![Top view of CSM landing page containing a button to edit in original scope.](../image/ps-edit-original-scope-msg.png)

4.  In the Customer Service Management \(CSM\) landing page, select the **My active cases** component and in the **Config** tab of the Configuration pane, delete the **account** field from the **Columns**.

    ![Admin view of the configuration pane showing the account field being removed from the columns of the landing page.](../image/ps-csm-landing-page-active-cases.png)

5.  Add the **Constituent** field:

    1.  In the Configuration pane, select **+Add** in the **Columns** list to open the field chooser.

        ![Admin view of the configuration pane, where you can customize the fields, columns, and sections displayed.](../image/ps-constituent-field.png)

    2.  In the Choose a field list, select **Consumer** &gt; **Constituent**, then select **OK**.

        ![Admin view of the field list, displaying a list of all fields that can be added or removed from the CSM landing page.](../image/ps-field-list.png)

    3.  In the Configuration pane, rearrange the columns by moving **consumer.constituent** below **short.description**.

        ![Admin view of the configuration pane that shows columns being rearranged.](../image/ps-configuration-pane-rearrange.png)

6.  Repeat Steps 3 and 4 to change the **My Team’s cases** component.

7.  Make other page changes as needed.

8.  Select **Save** to save the landing page changes.


**Parent Topic:**[Set up the CSM Configurable Workspace for Public Sector Digital Services](../concept/setting-up-csm-fsm.md)

