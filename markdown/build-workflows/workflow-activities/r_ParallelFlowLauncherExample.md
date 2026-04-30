---
title: Parallel Flow Launcher example
description: This example shows how to use the Parallel Flow Launcheractivity with an array of input values and with a WorkflowCoordinator object.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Parallel Flow Launcher workflow activity, Subflow activities in workflow, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Parallel Flow Launcher example

This example shows how to use the **Parallel Flow Launcher**activity with an array of input values and with a WorkflowCoordinator object.

## Sample workflow

This example shows a SQL-based web server with four application nodes. A single subflow runs to provision the database, and multiple parallel subflows each configure an application node. Finally, a separate set of parallel subflows configures the nodes to use a load balancer and sets up the server DNS.

![](../image/WFExampleParallelMainFlow.png "Parallel flow launcher business case")

## Provision the application nodes

The first **Parallel Flow Launcher**activity launches the **Provision Node** subflow four times. The activity passes a unique IP address to each subflow from an array in the **Inputs** variable. The scripts defined in the **Flow complete** and **Finished script** variables write log messages regarding the status of the subflows.

![](../image/WFParallelActivityDetail.png "Parallel flow launcher activity properties")

## Add nodes to the load balancer

The second **Parallel Flow Launcher** activity uses WorkflowCoordinator objects to specify which subflows to run. The `coordinator` variable stores the completed flow information from the previous **Provision Nodes** activity. The script then retrieves the IP address and port for each node that was provisioned. The `coord2` WorkflowCoordinator object runs the Add Node to Load Balancer subflow once for each node, using the retrieved IP address and port information as input variables. Finally, the `coord2` WorkflowCoordinator object runs the **SetupDNS** subflow once to configure the load balancer.

![](../image/WFParallelActivityDetail2.png "Specifying which subflows to run")

**Parent Topic:**[Parallel Flow Launcher workflow activity](r_ParallelFlowLauncher.md)

