---
title: Cloud cost simulation
description: Simulate the cost of moving your on-premise resources to the cloud environment before performing the migration.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Cloud cost simulation

Simulate the cost of moving your on-premise resources to the cloud environment before performing the migration.

## Plugins required

The following plugins are required for supporting cloud cost stimulator recommendations:

-   Cloud Insights application plugin \(sn\_clin\_billing\): for cloud infrastructure details and cost.
-   Hardware Asset Management \(sn\_hamp\): for end of life cycle for hardware.
-   Cloud Migration Assessment application \(com.sn\_cloud\_migration\): for resource utilization.

## Overview

The sam\_manager role specifies the criteria for migrating the resources to the cloud. For example, you may need all virtual machines installed with SQL Server or all virtual machines having end of life software. In addition the Software Asset Management application automatically provides recommendations based on End of Life software and hardware and resource utilization.

Based on the criteria or recommendation, the Software Asset Management application automatically selects the virtual machines that match your criteria. Once all the on-premise virtual machine have been identified, the Software Asset Management application matches those virtual machines with the virtual machines on the cloud: AWS or Azure.

The most optimal matching of resources is conducted and the total cost involved is given to you. Cost for the various cloud providers: AWS and Azure is mentioned along with or without the cost of Bring Your Own License \(BYOL\). Once the decision is made to move to a particular cloud provider, a change request can be created to move forward with the implementation.

For information on comparing and evaluating the estimate cost of migrating your resources to the cloud, see [Cloud simulator dashboard](cloud-simulator-dashboard.md).

![Cloud cost simulation.](../image/cloud-cost-simulatorv5.png)

## Use cases

A sam\_manager role can receive recommendations for migrating on-premise resources to the cloud while taking into account the following considerations:

-   End of life for software: On some virtual machines, you may have software that is nearing the end of its life cycle. Calculate the cost of migrating these virtual machines to the cloud, taking into account all of the benefits. For example, Microsoft Azure offers free extended security updates for certain Microsoft products that have reached the end of their life cycle.​

    **Note:** Recommendations are only shown for Microsoft Azure and AWS shared VMware virtual machines and not for dedicated host machines.

-   End of life for hardware: You may have virtual machines running on hardware that is nearing its end of life phase. Simulate the cost of moving these virtual machines to the cloud.

    **Note:** Ensure that you have activated of the Hardware Asset Management \(sn\_hamp\) plugin to get data on end of life cycle for hardware and hardware cost.

-   Resource utilization: Some on-premise virtual machines may have low CPU and RAM utilization. Simulate the cost of moving these virtual machines to the cloud by recommending the appropriate sized virtual machines. For example, if a 32 vCPU virtual machine on-premises, is utilizing only 4 vCPU, the recommendation would be a 4-vCPU virtual machine on the cloud, resulting in cost savings.​

    **Note:** Ensure that you have activated the Cloud Migration Assessment application \(com.sn\_cloud\_migration\) plugin to get data on resource utilization.


**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

