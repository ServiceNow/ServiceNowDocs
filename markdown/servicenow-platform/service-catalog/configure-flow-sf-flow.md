---
title: Configure a step-based service fulfillment flow
description: Define service fulfillment steps while creating a catalog item in Catalog Builder.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up the Catalog Builder, Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a step-based service fulfillment flow

Define service fulfillment steps while creating a catalog item in Catalog Builder.

## Before you begin

Role required: admin, catalog\_builder\_editor, or catalog\_admin

## About this task

In the base system, the Step-based request fulfillment flow is available. It includes the Service Fulfillment Steps base flow subflow that runs all steps defined in the service fulfillment flow. Following are the input and output parameters of the subflow.

|Parameter|Type|Description|
|---------|----|-----------|
|task|Reference|RITM record|

<table id="table_ctr_qhd_jpb"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

state

</td><td>

String

</td><td>

State of the subflow. Possible values are:-   completed: All steps are complete.
-   failed: At least one step failed because of invalid configurations such as missing subflow or step configurations.

</td></tr></tbody>
</table>For information about subflow field types, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

If your organization has processes to be run before or after the service fulfillment steps, create a flow and ensure that it is configured as a step-based service fulfillment flow.

## Procedure

1.  Create a Workflow Studio flow \(With the trigger type as Service Catalog\).

    Ensure that the Service Fulfillment Steps base flow subflow is called from this flow.

    For information about creating a flow with Service Catalog trigger type, see [Create a flow with a Service Catalog trigger](https://www.servicenow.com/docs/access?context=create-sc-flow&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

2.  Register the flow as service fulfillment flow.

    1.  Navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Service Fulfillment Steps Registry**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Service Fulfillment Flow Registry|Workflow Studio flow for which you want to enable service fulfillment steps.|
        |Application|Application scope in which the flow is supported for service fulfillment.|
        |Active|Option to enable the service fulfillment support for the flow.|

    4.  Click **Submit**.


**Parent Topic:**[Setting up the Catalog Builder](set-up-cat-builder.md)

