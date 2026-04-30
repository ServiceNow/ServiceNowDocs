---
title: Activate an agentic workflow template
description: Activate an agentic workflow that come installed with Now Assist applications in AI Agent Studio.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an agentic workflow, Now Assist AI agents, Enable AI experiences]
---

# Activate an agentic workflow template

Activate an agentic workflow that come installed with Now Assist applications in AI Agent Studio.

## Before you begin

Role required: sn\_aia.admin

## About this task

Agentic workflows that are installed with Now Assist applications aren’t automatically activated. You must activate them before they can be used in the Now Assist panel or as a UI action. Some may come with predefined triggers that must be set to active, too.

These predefined agentic workflows can also be used as templates for your own customized ones. You can [duplicate an agentic workflow](clone-aia-usecase.md) and use it as a blueprint for one that better suits your business needs, such as changing which records are available or providing different instructions.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows**.

2.  Select the agentic workflow that you want to configure.

3.  Select **Define trigger** to go to that step in Guided Setup.

4.  In the Existing triggers section, select the name of an inactive trigger to open the form.

5.  Toggle the Active slider so that it’s turned on.

6.  Select **Save**.

7.  If there’s more than one trigger, repeat steps 4–6 for each trigger that you want to activate.

8.  Select **Save and continue**.

9.  Toggle the display for the Now Assist panel and/or UI action so that it’s turned on.

    You have enabled the agentic workflow in the Now Assist panel. If the option isn't available, you must enable the panel first. For more information, see [Turn on the Now Assist panel](../../now-assist-admin/task/activate-now-assist-panel.md).

10. Select **Save and test**.


## Result

The agentic workflow runs when the trigger is detected in the Now Assist panel.

## What to do next

After completing the steps, you're redirected to test your agentic workflow to be sure it works as intended. You can [test an execution of your agentic workflow manually](test-aia-use-case.md) or [test the user access](test-aw-access.md). Once you've determined that the agentic workflow has the basic functionality you expect, you can [evaluate it using automated tests](execute-aia-eval.md).

