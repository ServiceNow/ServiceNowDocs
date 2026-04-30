---
title: Test a data collector for a policy version
description: Test a data collector for a policy version in the Test Playground.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Passing parameters to PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Test a data collector for a policy version

Test a data collector for a policy version in the Test Playground.

## Before you begin

Make sure you created a data collector in the policy. For more information, see [Create a data collector for a policy version](pace-create-data-collector.md).

Role required: sn\_pace.code\_editor

## Procedure

1.  Navigate to **All** &gt; **Variable Definition** &gt; **Data Collectors**.

2.  Select the data collector you want to test.

3.  Select the **Versions** tab, then the data collector name.

4.  Select the **Build** tab.

5.  In the contextual sidebar, select the Test playground icon ![Test playground icon.](../image/pace-test-playground-icon.jpg).

    ![Test data collector test playground.](../image/pace-data-collector-test-pg.jpg)

6.  Add the parameters in the inputs you want to test in the data collector, then select **Run test**.

    The results will appear in the Output tab.

7.  In the Publish draft window, select the **Activate this data collector** check box, then **Publish**.


