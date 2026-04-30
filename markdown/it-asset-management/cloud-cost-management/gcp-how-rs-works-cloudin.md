---
title: Rightsizing analysis for Google Cloud
description: Cloud Cost Management uses an optimized Rightsizing process for each provider.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Rightsizing resources, Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Rightsizing analysis for Google Cloud

Cloud Cost Management uses an optimized Rightsizing process for each provider.

## How Rightsizing analysis works for Google Cloud

The Google Cloud compute engine generates the recommendations that appear in the Rightsizing reports. Cloud Cost Management displays the recommendations that the Google Cloud compute engine generates. Cloud Cost Management updates the reports whenever billing data is updated.

For details on how the values are generated, see [Google Cloud documentation](https://cloud.google.com/docs).

**Note:** The Google Cloud console may show the same resources for both Unused resources and Rightsizing recommendations. If the same resources are displayed, Cloud Cost Management shows the information in Unused resources and excludes it from the Rightsizing recommendations with the reason, `Recommendation already present in unused`.

## Roles required for Google Insights modules

To get the recommendations from the Google Cloud console and perform start, stop, resize, and delete operations, you need the following roles.

-   compute.autoscalers.get compute.autoscalers.list compute.disks.delete
-   compute.disks.get compute.disks.getIamPolicy compute.disks.list compute.disks.resize
-   compute.disks.update compute.instances.delete compute.instances.getIamPolicy
-   compute.instances.setDiskAutoDelete compute.instances.start compute.instances.stop
-   compute.instances.update recommender.computeAddressIdleResourceInsights.get
-   recommender.computeAddressIdleResourceInsights.list
-   recommender.computeAddressIdleResourceRecommendations.get
-   recommender.computeAddressIdleResourceRecommendations.list
-   recommender.computeDiskIdleResourceInsights.get
-   recommender.computeDiskIdleResourceInsights.list
-   recommender.computeDiskIdleResourceRecommendations.get
-   recommender.computeDiskIdleResourceRecommendations.list
-   recommender.computeImageIdleResourceInsights.get
-   recommender.computeImageIdleResourceInsights.list
-   recommender.computeImageIdleResourceRecommendations.get
-   recommender.computeImageIdleResourceRecommendations.list
-   recommender.computeInstanceGroupManagerMachineTypeRecommendations.get
-   recommender.computeInstanceGroupManagerMachineTypeRecommendations.list
-   recommender.computeInstanceIdleResourceRecommendations.get
-   recommender.computeInstanceIdleResourceRecommendations.list
-   recommender.computeInstanceMachineTypeRecommendations.get
-   recommender.computeInstanceMachineTypeRecommendations.list
-   recommender.locations.get recommender.locations.list
-   resourcemanager.projects.get resourcemanager.projects.list

