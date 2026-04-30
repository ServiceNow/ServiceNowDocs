---
title: Universal Request state mapping
description: All workflows consist of states, transitions, and reasons. Map your service-specific states to the Universal Request states to provide a better user experience during request state transition.
locale: en-US
release: zurich
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure service to use Universal Request, Configure, Universal Request, Employee Service Management]
---

# Universal Request state mapping

All workflows consist of states, transitions, and reasons. Map your service-specific states to the Universal Request states to provide a better user experience during request state transition.

## Before you begin

Role required: admin

## About this task

For example, consider a universal request that has an HR payroll case attached to it as a primary task. When the HR case state changes from **In-progress** to **Awaiting Acceptance**, then the universal request state is updated to **Awaiting Response From User**.

![UR state mapping](../images/statemap.png)

By mapping the states of the service to the UR state, it is ensured that the correct state of UR is displayed. The state transition of the primary ticket is hidden from the requester and they only see the simplified UR state transitions that are driven by the state mappings. The following table describes the universal request states and the suggested mappings.

|Primary ticket status|UR state|
|---------------------|--------|
|When UR is created and there is no primary ticket|New|
|All states when ticket is being worked upon, like WIP, awaiting approval|In progress|
|All states that require response from a requester|In progress|

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration** &gt; **State Mapping**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For more information on the field description, see [State mapping form](../reference/ur-state-mapping-form.md).


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)

