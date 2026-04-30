---
title: View the agent feature matrix
description: The agent feature matrix displays the availability of Agent Client Collector features. The matrix displays data in a graph and a table.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Collecting data from your system devices, ACC deployment - shared between servers and endpoints, Agent Client Collector, IT Operations Management]
---

# View the agent feature matrix

The agent feature matrix displays the availability of Agent Client Collector features. The matrix displays data in a graph and a table.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

The agent feature matrix displays the granularity of Agent Client Collector features that are fully supported, partially supported, and not supported. A partially supported feature may have instance and framework requirements met, but runs on at least one agent version which does not meet the feature requirements.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agent Feature Matrix**.

    The **Agent feature matrix** appears.

    ![Agent feature matrix](../image/acc-agent-feature-matrix.png "Agent feature matrix")

    The matrix shows the support status of Agent Client Collector features that are fully supported, partially supported, and not supported \(Unsupported\).

2.  Select one of the categories on the graph.

    A list of all features in the category appears on the **Agent Feature Support Status** page.

    ![Agent feature support status page](../image/acc-agent-support-status.png "Agent Feature Support Status Page")

3.  Select one of the features.

    The **Agent Feature Support Status** page for the specific feature appears:

    ![Agent feature support status details page](../image/acc-feature-support-status-details.png "Agent Feature Support Status Details page")

    The page displays the following:

    -   Sections indicating the support status of the feature, and the various instance requirements of the feature. The **Action Items** field displays the actions you need to take to fully support a feature that is either partially supported or unsupported.
    -   Instance requirements and agent framework version requirements that have been met by the agent feature.

