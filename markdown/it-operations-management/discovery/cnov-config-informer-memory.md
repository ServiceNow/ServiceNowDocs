---
title: Configure informer pod memory limit and memory request
description: Set the memory limit and memory request of the Kubernetes Visibility Agent Informer pod.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery/cnov-config-informer-memory.html
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Agent Client Collector, Kubernetes, Visibility, Informer, memory, consumption, resources, Cloud Native Operations for Visibility, CNO for Visibility]
breadcrumb: [Install Kubernetes Visibility Agent \(KVA\) Informer, Configuring Kubernetes Visibility Agent, Kubernetes discovery using Kubernetes Visibility Agent, Discovery for containerized resources, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure informer pod memory limit and memory request

Set the memory limit and memory request of the Kubernetes Visibility Agent Informer pod.

## Before you begin

Role required: none

## About this task

Informer pod memory consumption depends mainly on the number of resources contained in the cluster. Memory limit defines the maximum memory the informer container is allowed to use, while memory request defines how much memory to reserve when scheduling the informer pod. Set the Informer pod's memory request and the Informer pod’s memory limit to at least \(number of pods\)/8MB, with a default minimum of 200MB. Memory request must not exceed the memory limit. For example:

|Estimated pod count|1000|5000|30000|
|-------------------|----|----|-----|
|Minimum memory limit|200Mi|625Mi|3.75Gi|
|Memory request|200Mi|625Mi|3.75Gi|

## Procedure

1.  Do one of the following:

    -   When using a Helm chart, in the Helm install command, add the following command line arguments:

        ```
        --set memoryLimit=MEM_LIMIT\
        --set memoryRequest=MEM_REQUEST
        ```

        For example:

        ```
        --set memoryLimit=625Mi\
        --set memoryRequest=625Mi
        ```

    -   When using the k8s\_informer.yaml, under the line containing “limits:” add the line `memory: MEM_LIMIT`.

        In the following example, MEM\_LIMIT and MEM\_REQUEST are 625Mi.

        ```
        
          limits:
            cpu: 100m
            memory: 625Mi
          resources:
            cpu: 100m
            memory: 625Mi
        
        
        ```

        **Note:**

        Setting `memoryRequest` equal to `memoryLimit` reserves exactly the memory your ACC agent needs. It prevents the ACC agent from being shut down if the system runs low on memory. This guarantees stable, uninterrupted agent operation. But if you leave memoryRequest at the default 200Mi while setting a higher memoryLimit \(such as 625Mi\), the pod is burstable — it schedules against 200Mi but can grow to 625Mi.


**Parent Topic:**[Install Kubernetes Visibility Agent \(KVA\) Informer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/cnov-deploy-install.md)

