---
title: Configure the List Menu for Public Sector Digital Services
description: Add public sector-related menu options to the List Menu in the CSM Configurable Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up the CSM Configurable Workspace for Public Sector Digital Services, Optional configuration steps for Public Sector Digital Services Core, Public Sector Digital Services Core, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Configure the List Menu for Public Sector Digital Services

Add public sector-related menu options to the List Menu in the CSM Configurable Workspace.

## Before you begin

Role required: admin

## About this task

To configure the List Menu, you can follow this procedure or use [guided setup](psds-use-gs.md) for the Public Sector Digital Services Core application.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the Tables \[sys\_db\_object\] table, select the **Search** icon next to the **Label** column and under the column heading, enter `UX List Menu Configuration`.

    ![Table list view showing search results for UX list menu configuration.](../image/ps-tables-list.png)

3.  In the UX List Menu Configuration List table, go to **Related Links** and select **Show List.**

    ![Table view showing UX list menu configuration settings with related links.](../image/ps-config-table.png)

4.  From the Context menu, select **Create Favorite** to bookmark the UX List Menu Configurations table so that you can quickly access it if you need to make changes later.

    ![Context menu on the UX list menu configuration settings page with the Create Favorite option highlighted.](../image/ps-create-fav.png)

5.  Remove the categories that are not applicable to Public Sector Digital Services.

    1.  Select the **CSM/FSM Configurable Workspace List Menu** record and go to the **UX List Categories** tab.

        ![UX List Categories tab in the UX List Menu Configuration page showing active categories and their details.](../image/csm-fsm-config-workspace.png)

    2.  For each of the following categories, select the category record and change the Active value to false:

        **Note:** If the following message is displayed, select **here** to edit the page.

        ![Error message redirecting the user to a link to edit a selected record.](../image/ps-config-workspace-msg.png)

        -   Cases
        -   Major Issue Management
        -   Tasks
        -   SLAs
        -   Incidents
        -   Problems
        -   Change
        -   Requests
        -   Catalog Tasks
        -   CMDB
        -   Conversation Monitoring

## What to do next

[Configure the Public Sector landing page using UI Builder.](public-sector-configure-landing-page.md)

**Parent Topic:**[Set up the CSM Configurable Workspace for Public Sector Digital Services](../concept/setting-up-csm-fsm.md)

