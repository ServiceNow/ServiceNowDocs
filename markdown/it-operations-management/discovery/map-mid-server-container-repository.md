---
title: Map MID Server to container image repository
description: If network access or datacenter location requires a specific MID Server, map MID Server to a private container image repository.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [container image scan, private repository, MID Server mapping, container repository]
breadcrumb: [Container image scanning for software decomposition, Kubernetes discovery using patterns, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Map MID Server to container image repository

If network access or datacenter location requires a specific MID Server, map MID Server to a private container image repository.

## Before you begin

-   Verify that you have at least version 1.30.2 of Discovery and Service Mapping Patterns.
-   Verify that the Linux MID Server has the following requirements:
    -   8GB RAM with 4GB for the Java Virtual Machine \(JVM\).
    -   MID Server **Capability** configured to **Scan Container Images**. For more information on configuring capabilities, see [MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/orchestration/mid-server-capabilities.md).
    -   Can access the image repository.
    -   Has Aqua Trivy, starting 0.44.0, installed on the MID Server. The last version validated is 0.68.2. For more information on installing Aqua Trivy, see the [Container Image scan feature overview \[KB1218504\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1218504) article in the Now Support Knowledge Base.
-   Verify that the container image repository credentials are configured for the private repositories. For more information, see [Create and test your credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/t_CreateCredential.md) and [Container image repository credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/container-image-repo-credential.md).
-   Verify that a container image discovery has run for Docker, Kubernetes, or Amazon Elastic Container Service \(Amazon ECS\) discovery. For more information, see:
    -   [Docker virtualization](../../discovery/concept/c-docker-virtualization.md)
    -   [Kubernetes discovery using patterns](../concept/kubernetes-discovery.md)
    -   [Amazon ECS resource discovery with Patterns](../reference/aws-ecs-fargate-discovery.md)
-   Verify that the Container Repository table contains the repository names required for this mapping. You can view the container repository list by entering `cmdb_ci_container_repository_list.do` in the navigation filter.

Role required: discovery\_admin

## About this task

By default, container image scanning selects a MID Servers with the **Scan Container Images** capability from the available MID Servers. You can configure the Image Registry to Mid Server Mapping table to map specific MID Servers to private repositories.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the **Label** column, enter `Image Registry to Mid Server Mapping`.

3.  Select the **Image Registry to Mid Server Mapping** table.

4.  In the **Related Links** section, select **Show List**.

5.  Select **New**.

6.  In the form, fill in the fields:

<table id="table_field_configuration"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Registry URL

</td><td>

Registry domain or host from the Container Repository table, up to the first slash. For example, if the full path is `registry.example.com/project/image`, enter `registry.example.com`.

</td></tr><tr><td>

Mid server

</td><td>

Linux MID Server for this repository that has the **Scan Container Images** capability configured.

</td></tr><tr><td>

Active

</td><td>

Option for enabling this mapping.

</td></tr></tbody>
</table>7.  Select **Submit**.


## What to do next

Scan the container images. For more information, see [Scan container images](container-image-task.md).

**Parent Topic:**[Container image scanning for software decomposition](../concept/container-image-concept.md)

