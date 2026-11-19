---
title: Migrate client scripts
description: Review all custom client scripts before agents go live in CSM Configurable Workspace. Some scripting approaches from CSM Agent Workspace aren't supported, and you must rebuild them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-client-scripts.html
release: australia
topic_type: task
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Migrate client scripts

Review all custom client scripts before agents go live in CSM Configurable Workspace. Some scripting approaches from CSM Agent Workspace aren't supported, and you must rebuild them.

## Before you begin

Role required: admin

## About this task

Custom client scripts control how fields behave on forms. For example, a script can make a field mandatory based on another field's value, or fill in fields when an agent opens a record. If a script doesn't work in CSM Configurable Workspace, agents may see unexpected form behavior or missing automation.

-   CSM Configurable Workspace doesn't support DOM manipulation.
-   Scripts that use Jelly scripting, UI macros, or UI pages don't appear in CSM Configurable Workspace. You must rebuild them in UI Builder.
-   Scripts that use standard GlideForm APIs usually work without changes, but verify each one.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Client Scripts**.

2.  Filter the list by the tables your agents use, such as sn\_customerservice\_case.

3.  Open each client script and sort it into one of the following categories.

    |Category|Description|
    |--------|-----------|
    |**Compatible**|The script uses standard GlideForm APIs and doesn't change the DOM. It works in CSM Configurable Workspace without changes.|
    |**Needs review**|The script uses approaches that may not work, such as jQuery selectors that target specific HTML elements, or window or document object calls.|
    |**Not supported**|The script uses DOM manipulation, Jelly scripting, or UI macros. You must rebuild it.|

4.  Test the scripts in the Needs review category in CSM Configurable Workspace on a non-production instance before go-live.

5.  For each script in the Not supported category, identify the agent workflow that the script supported, and then rebuild the same behavior using UI Builder components or declarative actions.

    To replace DOM manipulation scripts, use UI Builder components and event mappings, which let you set up field interactions visually without depending on the HTML structure of the page. For more information, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md).


