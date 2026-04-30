---
title: Create remote service catalog items in Service Exchange for Providers for Public Sector Digital Services
description: As a government agency provider, you can create remote catalogs to automate the task fulfillment process for constituents that are using the Government Service Portal. By using remote catalogs, agency providers can maintain the development of shared service catalogs on their instances and provide consumers with native catalog items in their instances remotely.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Service Exchange for Providers, Service Bridge, Case Management, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Create remote service catalog items in Service Exchange for Providers for Public Sector Digital Services

As a government agency provider, you can create remote catalogs to automate the task fulfillment process for constituents that are using the Government Service Portal. By using remote catalogs, agency providers can maintain the development of shared service catalogs on their instances and provide consumers with native catalog items in their instances remotely.

## About this task

Remote record producers in Service Exchange for Providers are service request catalog items that are remotely published to consumer instances, and contain the variables that determine the information that a consumer can or must provide to submit a request. They enable your consumer to request provider services through their service catalog by auto-generating a Provider Task record on the provider's instance and triggering a Create Case, Create Incident, or Create Change Request fulfillment task when a request is submitted.

By using remote catalogs, agency providers can maintain the development of shared service catalogs on their instances, and provide constituents with native catalog items in their instances remotely. The Remote Catalog is maintained on the Provider’s instance and made available selectively through Authorized Users.

## Before you begin

Role required: admin

**Note:** Ensure that the catalog scope is set to Global.

## Procedure

1.  Log into the provider instance and navigate to **All** &gt; **Service Bridge Provider** &gt; **Administration** &gt; **Remote Catalog Items**.

2.  Select **New** to create a new catalog item.

3.  On the form, fill in the fields.

<table id="table_uzj_fds_jmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the remote record producer catalog item.

</td></tr><tr><td>

Application

</td><td>

This is a read only field and is set by default based on the application scope.

</td></tr><tr><td>

State

</td><td>

Shows the status of the remote record producer. When you create a remote record producer, this field is set to the **Draft** state. **Note:** This field is automatically updated when you Publish, Archive, or Retire a remote record producer.

</td></tr><tr><td>

Table name

</td><td>

Table name is Provider Task. This is a read only field.

</td></tr><tr><td>

Flow

</td><td>

Choose one of the default Service Exchange flows provided or create your own flow if required.

</td></tr><tr><td>

Active

</td><td>

This is a read only field and is enabled based on the Publish, Retire, Archive, or Delete actions.

</td></tr><tr><td>

Persona

</td><td>

Catalog personas that you want to assign to this record producer.

</td></tr><tr><td>

Compatibility

</td><td>

This field is populated by default. It shows the Service Exchange version that is being used by the provider. If the consumer is using a compatible Service Exchange version, data can be synced between the provider and consumer instances. But if the consumer is not using a compatible version, any new entitlements cannot be activated until the corresponding Service Exchange version is upgraded.

</td></tr><tr><td>

Short Description

</td><td>

Short description for the record producer.

</td></tr><tr><td>

Description

</td><td>

Detailed description for the record producer.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The remote catalog item is now created, and will create a provider task in the provider instance. For more information on how to configure remote provider task definitions, see [Create remote task definitions in Service Exchange for Providers in Public Sector Digital Services](../task/psds-servicebridge-config-create-remote-task-def.md).

For more information on record producers in Service Exchange, see [Remote record producers in Service Exchange](https://www.servicenow.com/docs/access?context=service-bridge-v2-remote-record&version=yokohama&pubname=yokohama-service-bridge&ft:locale=en-US)

