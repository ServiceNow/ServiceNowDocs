---
title: Configure contextual side panel tabs in Service Operations Workspace
description: Add or delete tabs from the contextual side panel that is available in all record pages in Service Operations Workspace.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contextual side panel configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure contextual side panel tabs in Service Operations Workspace

Add or delete tabs from the contextual side panel that is available in all record pages in Service Operations Workspace.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin

## About this task

By default, all record pages such as an incident and interaction record page have a contextual side panel with multiple tabs in Service Operations Workspace. From these tabs, you can perform multiple tasks such as viewing the record information, collaborating through Microsoft Teams, viewing recommendations and so on.

![Contextual side panel in SOW](../image/contextual-side-panel-coral-theme.png "Contextual side panel in Service Operations Workspace")

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the Experiences list, select **Service Operations Workspace**.

3.  Under the Pages and variants list, select **SRP Record**.

4.  From the left of the UI Builder area, navigate to **Body** &gt; **Resizable panes** &gt; **right**, and select **Tab sidebar**.

5.  From the right of the UI builder, navigate to the **Config** &gt; **Tabs**, and select the **SOW - sidebar tabs top**.

6.  Select the ![Open contextual side panel tab](../image/open-side-panel-tab.png) icon to open the tab configuration.

    The pages and variants associated with contextual sidebar appears. For example, select the Agent assist SNC to add the Agent assist option in the sidebar.

7.  Edit the screen condition for the UX screen.

    1.  From the left of the page, select ![Menu](../../../reuse/icons/product-icons/menu-fill-24.svg) and navigate to **Developer** &gt; **Open variant record**.

    2.  On the UX screen form, edit the **Screen Condition** field to add or delete records to get the tab to the required position.

    3.  Select **Update**.

        You’re redirected to the Dashboards page.

8.  Edit the screen condition script for the UX screen by performing the following steps.

    1.  Select the previously opened tab of the UI Builder page, for example, the Agent assist SNC tab page.

    2.  From the left of the page, select ![Menu](../../../reuse/icons/product-icons/menu-fill-24.svg)and navigate to **Developer** &gt; **Open variant record**.

    3.  From the UX Screen Conditions related list on the UX screen form, open the associated record.

    4.  Edit the **Script** field to add or delete conditions for records where you want the tab to be available.

    5.  Select **Update**.


**Parent Topic:**[Contextual side panel configurations in Service Operations Workspace for ITSM](../concept/contextual-side-panel-configurations-sow-itsm.md)

