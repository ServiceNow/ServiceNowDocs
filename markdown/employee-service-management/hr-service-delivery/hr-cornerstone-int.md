---
title: HR Service Delivery Integration with Cornerstone OnDemand
description: The ServiceNow HR Service Delivery Integration with Cornerstone OnDemand application enables you to display relevant learning courses for employees as part of their To-do tasks in the ServiceNow Employee Center.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# HR Service Delivery Integration with Cornerstone OnDemand

The ServiceNow® HR Service Delivery Integration with Cornerstone OnDemand application enables you to display relevant learning courses for employees as part of their To-do tasks in the ServiceNow Employee Center.

Cornerstone OnDemand is a learning system that hosts learning videos, training, and certifications for employees. Using HR Service Delivery Integration with Cornerstone OnDemand, you can pull learning tasks from the Cornerstone OnDemand system to ServiceNow so that employees can view all their To-do tasks in a single location, Employee Center.

## Setting up the application

To set up the HR Service Delivery Integration with Cornerstone OnDemand application, you must first activate the HR Service Delivery Integration with Cornerstone OnDemand plugin \[sn\_hr\_cornerstone\] from ServiceNow Store. This plugin activates Cornerstone spoke in IntegrationHub and Enterprise Service Management Integrations Framework. Next you must set up the Cornerstone spoke in IntegrationHub. For details on how to complete the set up, refer to [Setting up HR Service Delivery Integration with Cornerstone OnDemand](../task/set-up-cornerstone.md).

## Using Enterprise Service Management Integrations Framework

Enterprise Service Management Integrations Framework provides a consistent way of building integrations for common use cases such as pulling employee profile information, pulling to-dos, or pulling other data from third-party systems and storing it in ServiceNow instance. It contains common components, such as the Source table, HR Integration Services table, scheduled flows, and transform maps, that can be used for building integrations.

By default, when the HR Service Delivery Integration with Cornerstone OnDemand application is set up, source, HR integration services, scheduled flows, and transform maps are automatically set up for the Cornerstone OnDemand system in Enterprise Service Management Integrations Framework. The schedule flows in Enterprise Service Management Integrations Framework interact with the Cornerstone OnDemand system to pull users, learning objects, and transcripts into ServiceNow.

## Assigning learning tasks to employees

When learning tasks are assigned to employees in the Cornerstone OnDemand system, transcripts are created for those employees in the Cornerstone OnDemand system.

Enterprise Service Management Integrations Framework, using the Sync Transcripts service, pulls the transcripts from the Cornerstone OnDemand system and displays them as tasks in the To-dos page in Employee Center.

On clicking the learning task in Employee Center, the employee is navigated to Cornerstone OnDemand system for completing the task. When the employee completes the task in Cornerstone OnDemand system, the status of task gets updated in Employee Center after the scheduled job is run for the Cornerstone OnDemand system.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

<table id="table_iwv_lpv_klb" class="nav-card"><tbody><tr><td>

[Configure ![Plan and configure your implementation.](../../../common/image/icon-set-up.png) Plan and configure your implementation.](../task/set-up-cornerstone.md)

</td><td>

[Reference ![Get details about components like fields, tables, and properties.](../../../common/image/icon-reference.png) Get details about components like fields, tables, and properties.](../reference/reference-ondemand.md)

</td></tr></tbody>
</table>