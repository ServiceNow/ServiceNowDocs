---
title: Disable Docker container CI discovery
description: Configure Docker discovery to collect image CIs only, instead of both image and container CIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/disable-docker-container-discovery.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [Kubernetes discovery, Docker container, ITOM Licensing V4]
breadcrumb: [Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Disable Docker container CI discovery

Configure Docker discovery to collect image CIs only, instead of both image and container CIs.

## Before you begin

-   Verify that you have at least version 1.31.0 of Discovery and Service Mapping Patterns.
-   Check your entitlements to determine whether you have access to 2026 Container Packaging.

Role required: discovery\_admin \(granted automatically with 2026 Container Packaging\)

## About this task

In large environments, container instances can generate a high volume of CIs. The **sn\_itom\_pattern.bring\_discovery\_container** system property controls whether the Kubernetes, Kubernetes Event, Docker Pattern, and Amazon AWS - ECS patterns discover both Docker container and Docker image CIs, or only Docker image CIs. By default, the property is set to true and both Docker Container \[cmdb\_ci\_docker\_container\] and Docker Image \[cmdb\_ci\_docker\_image\] are populated. When set to false, only Docker Image \[cmdb\_ci\_docker\_image\] is populated.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `sn_itom_pattern.bring_discovery_container`.

3.  Select the **sn\_itom\_pattern.bring\_discovery\_container** system property.

4.  In the **Value** field, enter `false`.

    To discover both Docker container and Docker image CIs, set the value to `true`.

5.  Select **Update**.


## What to do next

Run discovery again to apply the changes.

**Parent Topic:**[Discovery for containerized resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/container-discovery.md)

