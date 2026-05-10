---
title: Configure testing support for playbooks
description: Configure the Automated Test Framework \(ATF\) to support testing playbooks by authoring tests in the ATF UI on your ServiceNow instance.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Testing support, Running Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Configure testing support for playbooks

Configure the Automated Test Framework \(ATF\) to support testing playbooks by authoring tests in the ATF UI on your ServiceNow instance.

## Before you begin

Role required: admin or atf\_test\_admin

## About this task

For more information about the ATF test configuration, see [Build and run your first automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-tut-build-first.md).

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

2.  Select **New**.

3.  On the form, fill in the fields.

    | | |
    |---|---|
    |Name|Type a name for the test.|
    |Application|Application scope that the test applies to.|
    |Active|Select the check box to activate the test.|
    |Fail on server error|Select the check box to fail the test if there is a server error.|
    |Enable parametrized testing|Select the check box to enable testing that executes a single test case multiple times using different sets of input data instead of creating separate tests for each scenario.|
    |Description|Type a description of the test that helps you identify it.|

4.  Select **Save**.

5.  On the Test Steps tab, select **Add Test Step**.

6.  In the Add Test Step dialog box, select **Configurable Workspace** &gt; **Open Workspace Page**, and then select **Next**.

7.  In the Add Test Step: Open Workspace Page, in the **Workspace URL** text box, enter the URL for your playbook.

    For example: `/now/playbook-workspace-demo/record/interaction/-1`

8.  Select **Submit**.

9.  On the Test page, select **Add Test Step**.

10. In the Add Test Step dialog box:

    1.  Select **Configurable Workspace** &gt; **Test Page**.
    2.  In the **Insert after** drop-down list, select **Step 1 - Open Workspace Page**.
    3.  Select **Next**.
    4.  In the Configurable Workspace Test Authoring dialog box, select **Open**.
11. In the Create New Interaction page, under PAGE COMPONENTS, select one of the Playbook components based on whether you are testing a monolithic playbook or a custom layout playbook:

    |Choose one of the following for monolithic playbooks:|Choose one of the following for custom layout playbooks:|
    |-----------------------------------------------------|--------------------------------------------------------|
    |**now-playbook-experience-connected**|**sn-playbook-card**|
    |**sn-playbook-card**|**now-playbook-activity-picker**|
    | |**now-playbook-activity-viewer**|
    |**now-playbook-stage-picker**|

    **Note:** The **sn-playbook-card** component can be used for either a monolithic or a custom playbook.

12. Under ACTIONS:

    1.  From the Action drop-down list, select **\[Stacked Selector\]: Gets the playbook title by index.**
    2.  In the next text box, enter `0`.
    3.  Select **Submit**.
    4.  Select **Save**.

## Result

Return to your test configuration page on your instance, refresh the page, and you can see the test step you just configured added to the Test Steps tab. For more information, see [Build and run your first automated test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-tut-build-first.md).

## What to do next

Add as many test steps as you need and then run the test. For information about running an ATF test, see [Run an automated test on a playbook](run-atf-test-on-playbook.md).

**Parent Topic:**[Testing support for playbooks](../concept/testing-support-playbooks.md)

