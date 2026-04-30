---
title: Test updates to a PaCE policy version
description: Use the Test Playground to test updates to a PaCE policy script. You can evaluate changes to the policy script in real time, enabling you to determine if the changes that are applied render the policy compliant or non-compliant.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use Test Playground, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Test updates to a PaCE policy version

Use the Test Playground to test updates to a PaCE policy script. You can evaluate changes to the policy script in real time, enabling you to determine if the changes that are applied render the policy compliant or non-compliant.

## Before you begin

Role required: sn\_pace.admin

## About this task

The Test Playground enables you to apply changes to the policy script, and see the impact of those changes in real time. After the changes have been evaluated, save the script to ensure that the changes are implemented when the policy is next invoked.

## Procedure

1.  In the **Policy builder** tab, select the Test playground icon ![Test playground icon.](../image/pace-test-playground-icon.jpg) in the right-hand menu.

2.  In the Test parameters tab, fill in the forms as needed.

<table id="table_rnc_mw4_1xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Document

</td><td>

The document that you want to test the policy version with.**Note:** This field will change depending on which application PaCE is being used.

</td></tr><tr><td>

Log level

</td><td>

Level of the log.

</td></tr><tr><td>

Timeout

</td><td>

Timeout to determine the execution threshold of the test.

</td></tr><tr><td>

Execution log

</td><td>

Execution tag for the policy version.

</td></tr><tr><td>

Verbose

</td><td>

Option to make the test display in a verbose format.

</td></tr></tbody>
</table>    ![Test parameters tab.](../image/pace-test-paras-section-2.jpg)

3.  Under the **API parameters** and **Config parameters** tabs, select the variables you want to test with the policy version.

4.  When you are done modifying your policy script, click **Run Test**.

    A decision is reached regarding the compliance or non-compliance of the policy, based on the changes you made to the script. In the Test Parameters section, either **Compliant** or **Non-compliant** is displayed, along with additional output on any warnings or failures, and how long the evaluation took.

    **Note:** A decision with Compliant with exception will not work with a custom decision.

    ![Output tab.](../image/pace-output-tab-2.jpg)


