---
title: Set Automated Test Framework \(ATF\) code coverage
description: Define what percentage of code coverage results in Automated Test Framework \(ATF\) test failure tasks that require remediation.
locale: en-US
release: australia
product: ReleaseOps
classification: releaseops
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ReleaseOps, Deploying applications, Building applications]
---

# Set Automated Test Framework \(ATF\) code coverage

Define what percentage of code coverage results in Automated Test Framework \(ATF\) test failure tasks that require remediation.

## Before you begin

Role required: sn\_releaseops.releaseops\_tester or sn\_releaseops.releaseops\_developer

## About this task

The Automated Test Framework \(ATF\) code coverage threshold is the percentage of code that is covered by ATF test suites. By default, if ATF test suites cover less than 70 percent of the code in a deployment request, ReleaseOps transitions the deployment request to the **Reconciling** state and a test failure task is automatically created. You can adjust the ATF code coverage threshold in your deployment request assessment playbook.

To learn more about ATF code coverage, see [Deployment analyzer in ReleaseOps](../concept/deployment-analyzer.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the deployment request assessment playbook.

    **Important:** Remember to select the playbook that you use for the deployment request assessment stage of your pipeline, not the sample ReleaseOps deployment request assessment playbook. Preserving the ReleaseOps sample playbooks enables you to refer back to them as new features are added during instance upgrades.

    ![List of all playbooks in Workflow Studio. Select the deployment request assessment playbook.](../image/releaseops-dr-assessment-playbook.png)

3.  Select the playbook activity **Check test results**.

    ![Select the playbook activity Check test results.](../image/releaseops-select-check-test-results.png)

4.  In the side panel, select the **Branches** tab.

    ![In the side panel, select the Branches tab.](../image/releaseops-playbook-activity-branches.png)

5.  Select the low code coverage branch.

    ![The low code coverage branch is where you set the value of code coverage that triggers a test failure.](../image/releaseops-low-coverage-branch.png)

6.  Select **Modify condition**.

7.  Adjust the percentage of code coverage that triggers a test failure task by entering the percentage \(as an integer\) in the **Number** field.

    For example, if you want a test failure to be triggered when the code covered by ATF tests is less than 50 percent, enter `50` in the **Number** field.![In the Number field, enter the value of code coverage percentage as an integer that will trigger a test failure.](../image/releaseops-set-code-coverage-value.png)

8.  Select **Modify** to apply your changes to the branch.

9.  Select **Save and close**.


