---
title: Create a CDM application that is based on an existing service in the CMDB
description: Create an application as the container for all config data for a service \(an application service, application model, or dynamic CI group \[infrastructure\] in the CMDB\).
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create an application in DevOps Config, Configuring DevOps Config, DevOps Config, IT Service Management]
---

# Create a CDM application that is based on an existing service in the CMDB

Create an application as the container for all config data for a service \(an application service, application model, or dynamic CI group \[infrastructure\] in the CMDB\).

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: CDM Admin \[sn\_cdm.cdm\_admin\]

## About this task

For the application, you specify the number of deployables to generate and the SDLC environment that the deployables represent. When you upload existing config data into the application, the system maps the data as `[name:value]` pairs \(config data items — CDIs\) in the appropriate node in the data structure of the CDM application. For an overview of the process of preparing a new application to receive config data, see [Preparing an application for config data upload](../concept/cdm-prep-app-for-upload.md).

## Procedure

1.  Select the Applications icon \(![Applications icon](../image/icon-applications-nav.png)\) to open the Create new application page and then select **Application based on existing services** to specify the CMDB service that the new application will hold config data for.

    ![Choose how to create the new CDM application](../image/cdm-create-new-app-page.png)

2.  Fill in the settings on the Create Deployables dialog box to specify the quantity and environment type of the deployables and the CMDB services to connect them to.

<table id="table_efn_lrs_xrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Environment

</td><td>

The kind of code environment that is configured by the config data in the deployable.-   Production
-   Development
-   Test


</td></tr><tr><td>

Connection preference

</td><td>

Option to connect the newly created deployables to services.-   Auto-connect each new deployable to a service in the application model or dynamic CI group.
-   Manually specify the service to connect each new deployable to. You make the connections on the next page.
 **Note:** Because the DevOps pipeline applies config data in a deployable only to the services that the deployable is connected to, every deployable must be connected to a service.

</td></tr><tr><td>

Quantity

</td><td>

The number of deployables to create.If the number exceeds the number of services that are associated with the existing item in the CMDB, then the system generates new blank services.

</td></tr></tbody>
</table>    When you select **Create**, the system generates the application with the specified number and types of deployables and opens the **Edit deployables** tab for the application.

3.  Select **Manage deployables** to open the **Edit deployables** tab where you can configure the deployables.

4.  On the **Edit deployables** tab, update the settings for each deployable and then select **Next**.

    You connect each deployable to a service in the CMDB. The deployable holds the config data for its associated service.

    The system auto-saves your updates to settings.

<table id="table_zy2_rlt_xrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deployable name

</td><td>

Default name for the deployable that the system generates. Rename as needed.

</td></tr><tr><td>

Deployable description

</td><td>

Description that helps other users understand the purpose, scope, and intent of the deployable.

</td></tr><tr><td>

Identifier

</td><td>

Unique identifier that distinguishes this deployable from other deployables that share the same name and possibly many config data settings. For example, the production deployable that has the identifier **Uraguay** might have different config settings for the `currency` setting than the deployable that has the identifier **Greenland**.

</td></tr><tr><td>

Connected to

</td><td>

Service in the CMDB that is configured by the data in snapshots of the deployable. Select a service in the **Available services** list.

 **Note:** To continue, you must connect each deployable to a service.

 Perform one of the following actions:

-   Connect the deployable to a CI in the CMDB: Select the cmdb\_ci and then select **Next**.
-   Create a CI to connect to: Select **New**, define the CI, and then select **Next**.


</td></tr></tbody>
</table>    The Review page opens.

5.  Click **Next** to view the list of deployables on the **Edit deployables** tab.

    ![Choose how to create the new CDM application](../image/cdm-edit-deployables-tab.png)


## What to do next

The application is not yet structured to accept config data, so the next step is to add the data structure. See [Add the nodes that will contain config data to a new CDM application](cdm-data-structure-add-for-upload.md).

**Related topics**  


[CDM data model](../reference/cdm-data-model.md)

[Viewing and editing config data](../concept/cdm-editing-config-data-changesets.md)

[Define or update a component](cdm-component-define.md)

[Define or update a collection in an application](cdm-collection-define.md)

[Create or update a variable CDI](cdm-variables-crud.md)

[How encrypted data is handled](../concept/cdm-secrets-managing.md)

