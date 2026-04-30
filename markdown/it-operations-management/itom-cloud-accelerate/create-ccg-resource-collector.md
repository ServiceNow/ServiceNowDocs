---
title: Create a resource collector
description: Create a resource collector to set up how Cloud Configuration Governance imports all the resources of a given type.
locale: en-US
release: zurich
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Configuration Governance policies, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a resource collector

Create a resource collector to set up how Cloud Configuration Governance imports all the resources of a given type.

## Before you begin

Role required: sn\_itom\_ccg.governor

## About this task

The cloud resources are available under a service account or service account-datacenter combination. The resource collector uses Integration Hub subflows to import the resource list from the cloud. Create only one resource collector per resource type.

## Procedure

1.  Create an Integration Hub subflow for the configuration collector.

    1.  Copy the **CCG – Collector Template** subflow.

        For more information on copying subflow templates, see [Copy an Integration Hub subflow template](copy-ih-subflow-template.md).

    2.  Add the appropriate Cloud Action Library \(CAL\) action and flow logic to read the resource data.

        For more information on the available CAL actions, see [Cloud Action Library actions reference](../reference/ccg-cal-actions.md).

        If CAL doesn’t have the required action, you can refer to an existing CAL action and use the Integration Hub datastream action to implement the custom action. Alternatively, you can also use the REST step. For more information, see [Data Stream actions and pagination](https://www.servicenow.com/docs/access?context=data-stream-actions&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) and [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    3.  Add the **CCG – Insert Resource Record** action, and then select the appropriate inputs to insert the configuration data to the Configuration Management Database \(CMDB\).

        For more information on the **CCG – Insert Resource Record** action, see [Cloud Configuration Governance actions reference](../reference/ccg-ih-reference.md).

    4.  Select **Publish**.

2.  Navigate to **Cloud Configuration Governance** &gt; **Resource Collectors**.

3.  Select **New**.

4.  On the form, fill in the fields.

    For the description of the field values, see [Cloud Configuration Governance Resource collector form](../reference/ccg-res-collector-form.md).

5.  Select **Submit**.


## What to do next

-   If the required configuration data is not available at the cloud resource level, see [Create a configuration key](create-ccg-config-key.md).

-   If you have created a new resource type in the Cloud Configuration Governance application, you can optionally create a CI finder mapping for the newly created resource type. For more information, see [Create a CI finder mapping](create-ci-finder-mapping-for-ccg.md).


