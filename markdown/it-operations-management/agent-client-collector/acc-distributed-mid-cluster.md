---
title: Enable metrics collection and evaluation
description: To enable a ServiceNow instance to collect and evaluate metrics, you must create a distributed MID Server cluster, associate MID Servers with the cluster, and enable Metric Intelligence for your MID Server.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Enable metrics collection and evaluation

To enable a ServiceNow instance to collect and evaluate metrics, you must create a distributed MID Server cluster, associate MID Servers with the cluster, and enable Metric Intelligence for your MID Server.

## Before you begin

Ensure that the following plugins are installed on your instance:

-   Event Management \(com.glideapp.itom.snac\)
-   Metric Intelligence - com.snc.sa.metric plugin
-   MetricBase

To verify that the MetricBase plugin has been installed correctly:

1.  Enter `stats.do` in the instance navigation pane.
2.  Search for the **MetricBase Statistics** section and verify that the following appears:
    -   Status: ONLINE
    -   Name: clotho

Role required: agent\_client\_collector\_admin

## Procedure

1.  Create a distributed MID Server cluster in your instance:

    1.  Navigate to **MID Server** &gt; **Clusters**.

        The MID Server Clusters page opens, displaying the list of configured MID Server clusters.

        ![MID Server Clusters page](../image/ACC-MID-Server-Clusters.png)

    2.  Click **New**.

        The **MID Server Cluster - New record** page opens.

    3.  In the **Name** field, assign a descriptive name for the cluster.

    4.  In the **Type** field, select **Distributed**.

    5.  Click **Submit**.

        The distributed MID Server appears on the MID Server Clusters page.

2.  Assign MID Servers to the distributed MID Server cluster:

    1.  On the MID Server Clusters page, select the distributed MID Server cluster.

        The following page appears:

        ![MID Server Cluster details page](../image/ACC-MID-Cluster.png)

    2.  On the **Includes MID Servers** tab, click **Edit**.

        The **Edit Members** page appears.

        ![Edit Members page](../image/ACC-Edit-Members.png)

    3.  Select the relevant MID Servers from the left cell and click the right arrow button ![Right arrow icon](../image/right-arrow-icon.png) to move them to the right cell.

        In a staging environment, it is acceptable to have only one MID Server in the cluster.

    4.  Click **Save**.

        The **Includes MID Servers** tab displays the MID Servers that are part of the cluster.

        ![Includes MID Servers tab](../image/ACC-includes-MID-Servers-tab.png)

3.  Enable Metric Intelligence for your MID Server:

    1.  Navigate to **MID Server** &gt; **Extensions** &gt; **Metric Intelligence**.

        The **Metric Intelligence Metrics Contexts** page appears.

    2.  Click **New**.

        The **Metric Intelligence Contexts - New record** page appears.

        ![Metric Intelligence metrics contexts - New record form](../image/acc-mi-metrics-context.png)

    3.  In the **Name** field, enter a descriptive name for the Metric Intelligence metrics extension.

    4.  In the **MID Server** field, select the MID Server to which you want to associate the Metric Intelligence metrics extension.

    5.  Select the **ACC Dedicated MID** check box to assign the specified MID Server as the only MID Server in the distributed cluster.

        Selecting this option helps conserve system resources and memory.

    6.  In the **Related Links** section at the bottom of the page, click **Start**.

        A message appears, indicating the status of the extension.

    7.  Click **Submit**.

    8.  Click **Start**.


**Related topics**  


[Limit metrics collection and evaluation](acc-limit-metrics-collection.md)

