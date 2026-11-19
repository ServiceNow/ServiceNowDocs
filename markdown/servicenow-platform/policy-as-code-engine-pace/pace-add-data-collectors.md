---
title: Add data collectors to a policy version
description: After testing the activated data collectors, add them to a policy in the Policy Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/policy-as-code-engine-pace/pace-add-data-collectors.html
release: zurich
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Passing parameters to PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Add data collectors to a policy version

After testing the activated data collectors, add them to a policy in the Policy Builder.

## Before you begin

Role required: sn\_pace.code\_editor

## Procedure

1.  In the Policy Builder tab, select the version of the policy you want to add the new data collector to, then the Data sources icon \[Omitted image "pace-data-source-icon.jpg"\] Alt text: Data source icon.

2.  Select the data collector from the list of possible data collectors in the system, then click **Next**.\[Omitted image "pace-add-data-collector-list.jpg"\] Alt text: Add data collector list.

3.  In the Add data collector page in the Details tab, give the data collector a label and variable name.

    **Note:** If you're using the same data collector multiple times, it should have a different variable name.\[Omitted image "pace-add-data-collector-details.jpg"\] Alt text: Add data collector details

4.  Provide inputs to complete the configuration of the data collector in the Input tab.

    **Note:** The input can be user-specified or selected from the data picker icon.

5.  Click **Save**.

    After the data collector is added and configured, you can access the data collector in the script editor using the data picker in low-code. Additionally, you can delete a data collector by selecting it and selecting the **Delete** button


