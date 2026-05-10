---
title: Configure a process for a clustering solution
description: Configure a process to be able to generate a cluster analysis.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cluster analysis, Analyzing and getting process insights, Use, Process Mining, Platform Analytics]
---

# Configure a process for a clustering solution

Configure a process to be able to generate a cluster analysis.

## Before you begin

**Note:**

-   You can create one configuration per table for each project based on a process.
-   Role required:
    -   The sn\_process\_mining\_admin and sn\_process\_mining\_power\_user roles can associate a clustering solution definition with a project, but cannot create a definition.
    -   The sn\_process\_mining\_analyst role can view a clustering solution definition, but cannot create, edit, associate, or delete a definition.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Configurations**.

2.  Open the process configuration for which you want to configure the cluster analysis.

    Alternately, you can also choose to create a new process configuration by selecting **New**. For more information, see [Create process configuration using Classic view](create-process-config.md).

    ![Configuring cluster analysis](../image/config-cluster-analysis.png)

3.  In the **Cluster Analysis** tab, select the search icon from the **Clustering solution definition** field.

4.  From the Clustering Definitions list, select an existing definition from the list, or select **New** to create a new clustering solution definition form.

    -   The administrator and ml\_admin roles can create a new clustering solution definition.
    -   If creating a new definition, configure the fields per guidance in [creating and training a clustering solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-clustering-solution.md).
5.  Select **Submit**.

    A clustering solution definition is associated with the process for the selected table.


## What to do next

[Perform a cluster analysis](request-cluster-analysis.md)

**Parent Topic:**[Cluster analysis](../concept/cluster-analysis.md)

