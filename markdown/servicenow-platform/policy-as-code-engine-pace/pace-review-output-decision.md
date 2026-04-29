---
title: Review execution output and decision
description: After evaluating any changes made to the PaCE policy script, you can review the execution output and compliance decision reached. You can review this output immediately after evaluating any policy script changes.
locale: en-US
release: australia
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Test Playground, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Review execution output and decision

After evaluating any changes made to the PaCE policy script, you can review the execution output and compliance decision reached. You can review this output immediately after evaluating any policy script changes.

## Before you begin

Role required: sn\_pace.execution\_reader

## Procedure

1.  In the **Policy builder** tab, click the policy version you want to evaluate.

2.  Select the Test playground icon ![Test playground icon.](../image/pace-test-playground-icon.jpg).

3.  After modifying the policy script according to your requirements, click **Run Test**

    The **Output** tab is displayed automatically, and shows the output and the decision reached.

    ![Output tab.](../image/pace-output-tab-2.jpg)

4.  Review the execution output in the **Output** tab:

<table id="table_c5l_tph_5pb"><thead><tr><th>

Output tab section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compliance decision

</td><td>

The decision can be:-   **Compliant**: The changes you applied to the policy script are compliant with the policy logic. When you click **Save Script**, the changes are saved, and the changes implemented the next time the policy is invoked.
-   **Non-compliant**: The changes you applied to the policy script are not compliant with the policy logic.
-   **Compliant-exception**: In this case, if a policy exception has been approved, any policies that are non-compliant are set to the compliant-exception state.
-   **Name of a custom decision**: In this case, the decision is pre-defined by the admin for decisions other than complaint or non-complaint.

**Note:** There could be multiple custom decisions depending on the type of application you're integrating with PaCE.

</td></tr><tr><td>

Warnings/Failures

</td><td>

Lists the number of warnings or failures generated during the execution.

</td></tr><tr><td>

Evaluation time

</td><td>

Shows how long the evaluation took, in milliseconds.

</td></tr><tr><td>

Execution output

</td><td>

Shows the execution output in JSON format. You can integrate this output with other applications and services and present it in your required format.

</td></tr><tr><td>

Custom

</td><td>

Shows the custom output of the custom decision.**Note:** This tab will only show up if you are testing a custom decision.

</td></tr></tbody>
</table>    If required, modify the policy script to resolve any issues that arose during the evaluation. You can also review policy execution logs for further analysis.


