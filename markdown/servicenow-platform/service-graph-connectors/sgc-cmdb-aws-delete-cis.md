---
title: Enable optimized deletion of retired CIs in AWS
description: Enable the sn\_aws\_integ.enableOptimizedDeletion system property for the optimized deletion of retired configuration items \(CIs\) in AWS during full import of data.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-10-11"
reading_time_minutes: 1
breadcrumb: [Additional features, AWS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Enable optimized deletion of retired CIs in AWS

Enable the **sn\_aws\_integ.enableOptimizedDeletion** system property for the optimized deletion of retired configuration items \(CIs\) in AWS during full import of data.

## Before you begin

Set the application scope to Service Graph Connector for AWS using the application picker. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin

## About this task

By default, the ListDiscoveredResources API is used in batches of 20 to ascertain deleted resource data as there's no other API in AWS that provides deleted resource deltas. This action adversely impacts performance, particularly with a large number of resources, as the majority of time is dedicated to API calls.

When your AWS instance has a large number of CIs to import, you can enable the **sn\_aws\_integ.enableOptimizedDeletion** property to accelerate the import time. The property enables deleting any retired CI classes with an improved logic. In this optimized deletion approach, a complete pull is conducted. Without depending on AWS API calls, the deleted CI is determined by comparing imported resources from the last run with the resources imported in the current run. By default, the value of the property is set to `false`.

## Procedure

1.  Enter `sys_properties.list` in the navigation filter, and then open the **sn\_aws\_integ.enableOptimizedDeletion** property.

2.  In the **Value** field, enter `true`.

3.  Select **Update**.


