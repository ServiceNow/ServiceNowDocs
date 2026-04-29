---
title: Configure a proxy bypass for specific internal or private container registries
description: Configure a proxy bypass to allow container image scans to reach specific internal or private registries that require a direct connection.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-08"
reading_time_minutes: 1
keywords: [container image scanning, MID Server proxy, proxy bypass, container registries]
breadcrumb: [Container image scanning for software decomposition, Kubernetes discovery using patterns, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure a proxy bypass for specific internal or private container registries

Configure a proxy bypass to allow container image scans to reach specific internal or private registries that require a direct connection.

## Before you begin

-   Verify that you have at least version 1.30.2 of Discovery and Service Mapping Patterns.
-   Verify that you have configured a proxy on the MID Server. For more information, see [MID Server parameters](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Role required: discovery\_admin

## About this task

When a proxy is configured on the MID Server, all container image scanning goes through that proxy by default. If some internal or private registries aren't reachable through the proxy, use the **sn\_itom\_pattern.container\_image\_scan\_no\_proxy** system property to specify registries that the MID Server contacts directly.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `sn_itom_pattern.container_image_scan_no_proxy`.

3.  Select the **sn\_itom\_pattern.container\_image\_scan\_no\_proxy** system property.

4.  In the **Value** field, enter the hosts, domains, or IP ranges that bypass the proxy, separated by commas.

    Examples:

    -   Hostname: internal.registry.mycompany.com
    -   Domains: internal.mycompany.com,.internal.mycompany.com
    -   IP ranges: 10.0.0.0/8,172.16.0.0/12
    -   Hostname, domain, and IP ranges combined: internal.registry.mycompany.com,internal.mycompany.com,.internal.mycompany.com,10.0.0.0/8,172.16.0.0/12
    **Note:** To stop using the bypass, clear the values in this field.

5.  Select **Update**.


## What to do next

Scan the container images. For more information, see [Scan container images](container-image-task.md).

**Parent Topic:**[Container image scanning for software decomposition](../concept/container-image-concept.md)

