---
title: Configure the memory limit of the Informer pod
description: Set the memory limit of the Agent Client Collector for Kubernetes – Visibility Informer pod.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, Informer, memory, consumption, resources, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Agent Client Collector for Kubernetes – Visibility, Configuring Agent Client Collector for Kubernetes – Visibility, Kubernetes discovery using Agent Client Collector for Kubernetes – Visibility, Container discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure the memory limit of the Informer pod

Set the memory limit of the Agent Client Collector for Kubernetes – Visibility Informer pod.

## Before you begin

Role required: none

## About this task

Informer pod memory consumption depends mainly on the number of resources contained in the cluster. Set the Informer pod’s memory limit to at least \(number of pods\)/8MB, with a minimum of 200MB. For example:

<table id="table_mcf_qbz_syb"><tbody><tr><td>

Estimated pod count

</td><td>

1000

</td><td>

5000

</td><td>

30000

</td></tr><tr><td>

Minimum memory limit

</td><td>

200Mi

</td><td>

625Mi

</td><td>

3.75Gi

</td></tr></tbody>
</table>## Procedure

1.  Do one of the following:

    -   When using a Helm chart, in the Helm install command, add the following command line argument:

        `--set memoryLimit=MEM_LIMIT`

        For example: `--set memoryLimit=625Mi`

    -   When using the k8s\_informer.yaml, under the line containing “limits:” add the line `memory: MEM_LIMIT`.

        In the following example, MEM\_LIMIT is 625Mi.

        ```
        resources:
          limits:
            cpu: 100m
            memory: 625Mi 
        
        ```


