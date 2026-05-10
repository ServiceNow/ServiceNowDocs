---
title: Licensable Software Products Deployed on Containers report
description: You can use the Licensable Software Products Deployed on Containers report to gain visibility into the software products that are deployed across both on-premise and cloud environments using Docker containers.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SQL Server licensing in container deployments, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Licensable Software Products Deployed on Containers report

You can use the Licensable Software Products Deployed on Containers report to gain visibility into the software products that are deployed across both on-premise and cloud environments using Docker containers.

**Note:** To view this report, activate the Software Asset Management Professional plugin \(com.snc.samp\) and the [Discovery and Service Mapping Patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/install-discovery-service-mapping-patterns.md) application.

The Licensable Software Products Deployed on Containers report is available only in the Software Asset Workspace. To view this report, navigate to **All** &gt; **Software Asset** &gt; **Software Asset Workspace**. From the Software Asset Workspace, navigate to **License usage** &gt; **Reports** &gt; **Licensable Software Products Deployed on Containers**.

|Field|Description|
|-----|-----------|
|Container Name|Docker container through which you are deploying a software product.|
|Environment|On-premise or cloud environment in which you are deploying a software product through the Docker container.|
|Container ID|Unique identifier for the Docker container.|
|Hosted On Server|Physical server on which the Docker container is running.|
|Kubernetes Cluster|Kubernetes cluster that enables the Docker container to run.|
|Virtual CPU|Number of virtual CPUs \(vCPUs\) that are assigned to the Docker container.|
|Software Installed|Software product that you are deploying through the Docker container.|

**Parent Topic:**[Microsoft SQL Server licensing in container deployments](../concept/microsoft-licensing-software-containers.md)

