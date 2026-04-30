---
title: The Cloud API Trail
description: The Cloud API Trail is an activity log for all activity that uses the Cloud API and goes through the MID Server.Open the Cloud API Trail to debug and troubleshoot issues like a failed policy or failed Discovery of cloud resources.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# The Cloud API Trail

The Cloud API Trail is an activity log for all activity that uses the Cloud API and goes through the MID Server.

## Cloud API Trail contents

![The Cloud API Trail form](../image/cloud-api-trail-form.png "CAPI trail form")

<table id="table_ibs_2x5_gz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dynamic route ID

</td><td>

An auto-generated ID number for the entry.

</td></tr><tr><td>

Mid name

</td><td>

The name of the MID Server through which the Discovery was performed.

</td></tr><tr><td>

Route status

</td><td>

Whether or not the Discovery operation run by the API was successful. Possible values are:-   **success**
-   **error**
-   **executing**

</td></tr><tr><td>

Input parameters

</td><td>

The input parameter that generated the API trail record. This value is usually the datacenter in which the Discovery was run.

</td></tr><tr><td>

Interface name

</td><td>

 

</td></tr><tr><td>

Invoked by

</td><td>

This value is always **CMP** when running Discovery.

</td></tr><tr><td>

Method name

</td><td>

The interface operation from the Cloud API that processed this record.

</td></tr><tr><td>

Provider name

</td><td>

The cloud provider.

</td></tr><tr><td>

Version

</td><td>

The version specified in the Cloud API.

</td></tr></tbody>
</table>## CAPI Trail Logs

The CAPI Trail Logs related list provides more details about Cloud API trail entry. The following types of log keys are available:

|Log key|Description|
|-------|-----------|
|route\_data|Information about the Cloud API calls.|
|dynamic\_route|Information about the actual route the data took, including URIs.|
|route\_result|The payload received by the instance, or a description of the result of the data transfer. The payload|
|chunk\_number|The number of data chunks that the instance received.|
|route\_status|Whether the route connection and payload transfer was successful.|
|route\_error|The error that occurred. For example, the error `Failed to list loadbalancer Failed : HTTP error code : 403` means that your credentials were incorrect and Discovery could not access the cloud resource.|
|error\_detail|More details about the error, including the Cloud Provisioning and Governance API and connector that was used in the attempted Discovery, and the errors that the cloud provider threw.|

An example of a route\_error is as follows:

```
Failed to list loadbalancer Failed : HTTP error code : 403
```

An example of the error\_detail entry for the same error is as follows:

```
com.snc.cmp.connector.cloud.loadbalancer.component.LoadBalancerException: Failed to list loadbalancer Failed : HTTP error code : 403
       at com.snc.cmp.connector.cloud.loadbalancer.customizer.impl.AWSLoadBalancerCustomizer.listLoadBalancers(AWSLoadBalancerCustomizer.java:56)
	at com.snc.cmp.connector.cloud.loadbalancer.component.LoadBalancerProducer.process(LoadBalancerProducer.java:46)
	at org.apache.camel.util.AsyncProcessorConverterHelper$ProcessorToAsyncProcessorBridge.process(AsyncProcessorConverterHelper.java:61)
       at org.apache.camel.processor.SendProcessor.process(SendProcessor.java:145)
       ...
```

These two entries indicate that the credentials were incorrect, and Discovery could not access the cloud resource. The load balancer interface throws the first error because the load balancer device is the first device that allows access to the cloud resource. The `org.apache.camel` errors indicated routing errors on the Amazon Web Services side.

The corresponding error on the instance side is captured in the Cloud Orchestration Trail.

**Related topics**  


[The Cloud Orchestration Trail](cloud-orch-trail.md)

## Open the Cloud API Trail

Open the Cloud API Trail to debug and troubleshoot issues like a failed policy or failed Discovery of cloud resources.

### Before you begin

Role required: sn\_cmp.cloud\_operator or sn\_cmp.cloud\_admin

### Procedure

1.  In the Cloud Admin Portal, navigate to **Operate** &gt; **Trails**.

2.  On the **Cloud Api Trail** tab, filter and sort the list of Cloud API Trail records as needed.

    If you are looking for something like a failed Discovery, filter the list so the **Route Status** column shows only entries with **error**.

3.  Click a link in the Created column to open the Cloud API Trail record.

4.  In the CAPI Trail Logs related list, open the log record that displays the information you want.

    For example, open **route\_error** or **error\_detail** to debug a failed operation.


