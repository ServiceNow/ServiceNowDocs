---
title: Edit decision tables using draft authoring
description: Edit published decision tables in Workflow Studio when draft authoring is enabled. Without draft authoring enabled, decision tables are active and available to use as soon as they're created.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using decision tables, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Edit decision tables using draft authoring

Edit published decision tables in Workflow Studio when draft authoring is enabled. Without draft authoring enabled, decision tables are active and available to use as soon as they're created.

## Before you begin

Role required: admin, decision\_table\_admin, decision\_rule\_author, or decision\_result\_editor

## About this task

To modify a published decision table, you must create a draft, make any required changes, and publish the draft.

**Important:** Older versions of the decision table aren’t retained, so if you publish a draft, you can’t go back and access the previously published version again. This new published version is the live version.

Draft authoring is enabled by default on all new decision tables. For existing tables, draft authoring is available but not enabled by default.

To enable draft authoring for existing tables, ensure the decision table has no unsaved changes, open the decision table properties, and select **Enable draft authoring**. After you make this change, the decision table is moved to a published state, and you must create a new draft to make further changes.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Select a published decision table.

4.  Select **Create Draft**.

    This action creates a draft version of the table that you can edit to your liking and republish. The published version is available and is the version scripts, playbooks, and flows use when they execute decisions.

    You can view both the draft and published versions of the table by switching the **View** toggle.

5.  Change your decision table.

6.  Select **Save**.

7.  If you want this version to become the new published version and the original published version irretrievably replaced, select **Publish**.

8.  Select **Publish**.


**Parent Topic:**[Using decision tables](../concept/using-decision-builder.md)

