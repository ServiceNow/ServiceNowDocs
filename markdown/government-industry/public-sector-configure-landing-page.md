---
title: Configure the Public Sector landing page with UI Builder
description: Use the UI Builder to change certain fields in the Public Sector landing page of the CSM Configurable Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up the CSM Configurable Workspace for Public Sector Digital Services, Optional configuration steps for Public Sector Digital Services Core, Public Sector Digital Services Core, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure the Public Sector landing page with UI Builder

Use the UI Builder to change certain fields in the Public Sector landing page of the CSM Configurable Workspace.

## Before you begin

Role required: admin

## About this task

The CSM Landing Page gives agents an overview of their new, assigned, and high-priority cases, plus the cases assigned to their groups. Replace certain fields in the landing page with fields relevant to public sector. You can also add or change other fields as needed. For more information on using UI Builder to modify pages, see [Work with pages](https://www.servicenow.com/docs/access?context=work-pages&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **All** and in the filter, enter and select **UI Builder**.

2.  Navigate to the CSM Landing Page:

    1.  In the list of **My experiences**, select the **CSM/FSM Configurable Workspace**.

    2.  In **UI Builder**, navigate to **Page** &gt; **Landing Page** and select **CSM Landing Page**.

        ![View of CSM landing page with fully customizable content.](../image/ps-csm-landing-page.png)

    3.  In the message displayed at the top of the page, select **Edit in original scope**.

        ![Top view of CSM landing page containing a button to edit in original scope.](../image/ps-edit-original-scope-msg.png)

3.  In the CSM Landing Page, select the **My active cases** component and in the **Config** tab of the Configuration pane, delete the **account** field from the **Columns**.

    ![Admin view of the configuration pane showing the account field being removed from the columns of the landing page.](../image/ps-csm-landing-page-active-cases.png)

4.  Add the **Constituent** field:

    1.  In the Configuration pane, select **+Add** in the **Columns** list to open the field chooser.

        ![Admin view of the configuration pane, where you can customize the fields, columns, and sections displayed.](../image/ps-constituent-field.png)

    2.  In the Choose a field list, select **Consumer** &gt; **Constituent** and then select **OK**.

        ![Admin view of the field list, displaying a list of all fields that can be added or removed from the CSM landing page.](../image/ps-field-list.png)

    3.  In the Configuration pane, rearrange the columns by moving **consumer.constituent** below **short.description**.

        ![Admin view of the configuration pane that shows columns being rearranged.](../image/ps-configuration-pane-rearrange.png)

5.  Repeat Steps 3 and 4 to change the **My Team’s cases** component.

6.  Make other page changes as needed.

7.  Select **Save** in the top right corner to save the landing page changes.


**Parent Topic:**[Set up the CSM Configurable Workspace for Public Sector Digital Services](../concept/setting-up-csm-fsm.md)

