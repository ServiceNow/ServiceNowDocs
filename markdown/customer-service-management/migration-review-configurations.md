---
title: Review existing CSM Agent Workspace configurations
description: Before you start migrating, record your current CSM Agent Workspace configurations. Use this record to verify that each one is correctly reproduced in CSM Configurable Workspace after migration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-review-configurations.html
release: australia
topic_type: task
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Review existing CSM Agent Workspace configurations

Before you start migrating, record your current CSM Agent Workspace configurations. Use this record to verify that each one is correctly reproduced in CSM Configurable Workspace after migration.

## Before you begin

Role required: admin

## About this task

No automated export of CSM Agent Workspace configurations is available, so review each area manually. As you review, note the following:

-   Custom scripts attached to configurations. These may need review before they work in CSM Configurable Workspace.
-   The agent groups that use each configuration. You need this information when you set up audiences in UI Builder.

## Procedure

1.  To view your highlighted value records, navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **Highlighted Values**.

2.  To view your landing pages, navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **All Workspaces**, open the CSM Agent Workspace record, and go to the **Landing Pages** related list.

3.  To view your UI actions, navigate to **All** &gt; **System UI** &gt; **UI Actions** and filter by the tables your agents use.

4.  To view your ribbon configurations, navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Ribbon Setting**.

5.  To view your form header configurations, navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Header Configurations**.

6.  To note your chrome header settings, navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **All Workspaces**, open the CSM Agent Workspace record, and note whether the **Search enabled**, **Notifications enabled**, and **User Preference Controls enabled** check boxes are selected.

7.  To note your custom client scripts, navigate to **All** &gt; **System Definition** &gt; **Client Scripts** and filter by the tables your agents use.

    Pay particular attention to scripts that manipulate the DOM. These scripts don't work in CSM Configurable Workspace.


