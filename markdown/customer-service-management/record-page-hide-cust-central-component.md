---
title: Configure record pages to hide Customer Central components
description: Configure the CSM default record page and CSM Interaction record page to hide the Customer Activity and Customer Information tab components.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure record pages to hide Customer Central components

Configure the CSM default record page and CSM Interaction record page to hide the Customer Activity and Customer Information tab components.

## Before you begin

Role required: admin

## About this task

Starting with the Yokohama release, CSM Configurable Workspace has a dependency on the [Customer Central plugin](../concept/customer-central.md#section_jmt_bnt_ydc). The Customer Central application is installed automatically with CSM Configurable Workspace.

The Customer Central installation can result in the Customer Activity and Customer Information tab components appearing on the following CSM Configurable Workspace record pages:

-   CSM default record page
-   CSM Interaction record page

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the Page collections tab.

3.  Select a page collection.

    -   CSM default record post-Details
    -   CSM Interaction record post-Details
4.  Select **Settings** for one of the following page variants to open the settings panel.

    -   Customer Activity default
    -   Customer Information default
5.  In the Availability section, disable the **Active** check box.

6.  Select **Save**.


