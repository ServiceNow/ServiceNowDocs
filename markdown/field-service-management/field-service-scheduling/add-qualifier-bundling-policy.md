---
title: Add qualifiers to a task bundling policy
description: Add qualifiers to task bundling policies to define whether policies apply for either assignment groups or territories with Field Service Task Bundling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/field-service-management/field-service-scheduling/add-qualifier-bundling-policy.html
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Dynamic task bundling, Configuring Task Bundling, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Add qualifiers to a task bundling policy

Add qualifiers to task bundling policies to define whether policies apply for either assignment groups or territories with Field Service Task Bundling.

## Before you begin

Qualifiers are subcomponents of policies. For more information on how to create a policy, see [Create a task bundling policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/field-service-scheduling/create-a-task-bundling-policy.md).

Role required: admin

## About this task

Qualifiers dictate which work order tasks are targeted for bundling. Qualifiers are required for policies to run.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dynamic Bundling Administration** &gt; **Policies**.

2.  Open an existing policy.

3.  In the **Qualifiers** related list, select **New**.

4.  Select one of the following:

    -   Enter an **Assignment Group** to assign the policy to an assignment group.
    -   Enter a **Territory** to assign the policy to a territory.

        **Note:** **Assignment Group** appears by default. To replace with **Territory**, see [Enable the Field Service territory model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/workforce-optimization-for-field-service/enable-territory-model.md).

5.  Select **Submit**.


