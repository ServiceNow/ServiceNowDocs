---
title: Create a CDM application that generates a new service in the CMDB
description: Generate a new service \(an application service, application model, or dynamic CI group \[infrastructure application type\]\) in the CMDB\) and create a CDM application as the container for the config data for the service.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create an application in DevOps Config, Configure, DevOps Config, IT Service Management]
---

# Create a CDM application that generates a new service in the CMDB

Generate a new service \(an application service, application model, or dynamic CI group \[infrastructure application type\]\) in the CMDB\) and create a CDM application as the container for the config data for the service.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: CDM Admin \[sn\_cdm.cdm\_admin\]

## About this task

For the application, you specify the number of deployables to generate and the SDLC environment that the deployables represent. When you upload existing config data into the application, the system maps the data as `[name:value]` pairs \(config data items — CDIs\) in the appropriate node in the data structure of the CDM application. For an overview of the process of preparing a new application to receive config data, see [Preparing an application for config data upload](../concept/cdm-prep-app-for-upload.md).

## Procedure

1.  Select the **Applications** icon \(![Applications icon](../image/icon-applications-nav.png)\) to open the Create new application page and then select **New application**.

    ![Choose how to create the new CDM application](../image/cdm-create-new-app-page.png)

2.  On the **Overview** tab for the new CDM application, fill in additional application details that further identify the service in the CDM.

    The CSDM application model \(name, owner, manufacturer\) functions as the link between DevOps features. There is an SDLC component of the CDM for each CSDM application model.

    | | |
    |---|---|
    |Application name|Unique and meaningful name for the application.|
    |Application model name|Name of the application model.|
    |Maintained by|Groups with access to the application. Only members of these groups can access the application data.|
    |Application description|Description that helps other users understand the purpose, scope, and intent of the application.|
    |Application model owner|Name of the owner of the application model.|
    |Manufacturer|Manufacturer of the application.|

3.  Select **Manage deployables** to open the **Edit deployables** tab where you can configure the deployables.

4.  Select **Create deployables** and then fill in the settings on the Create Deployables dialog box to specify the quantity and environment type of deployables to create and the CMDB services to connect them to.

<table id="table_efn_lrs_xrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Environment

</td><td>

The kind of environment that is configured by the config data in the deployables.

 -   Development
-   Test
-   Production


</td></tr><tr><td>

Connection preference

</td><td>

Option to connect the newly created deployables to the new services. Auto-connect is the only option when creating an application to an existing CMDB entry.

 **Note:** Because the DevOps pipeline applies config data in a deployable only to the services that the deployable is connected to, every deployable must be connected to a service.

</td></tr><tr><td>

Quantity

</td><td>

The number of deployables to create.

 Limit: 100.

</td></tr></tbody>
</table>    When you select **Create**, the system generates an application model in the CMDB and the CDM application with the specified number and types of deployables. The system auto-generates names of the form &lt;AppName\_EnvironmentType\_number&gt;.

5.  On the **Edit deployables** tab, select the card for each deployable in turn and update its settings.

    You connect each deployable to a service in the CMDB. The deployable holds the config data for its associated service.

    The system auto-saves your updates to settings.

<table id="table_zy2_rlt_xrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deployable name

</td><td>

Default name for the deployable. To ensure that the auto-generated names are unique, the system adds a timestamp.

 Rename as needed.

</td></tr><tr><td>

Deployable description

</td><td>

Description that helps other users understand the purpose, scope, and intent of the deployable.

</td></tr><tr><td>

Identifier

</td><td>

Unique identifier that distinguishes this deployable from other deployables that share the same name and possibly many config data settings.

 For example, the production deployable that has the identifier **Pacific** might have different config settings for the `language` setting than the deployable that has the identifier **EU**.

</td></tr><tr><td>

Connected to

</td><td>

Service in the CMDB that the deployable is associated with. Select a service in the **Available services** list.

 Perform one of the following actions:

 -   Link the deployable to a CI in the CMDB: Select the cmdb\_ci and then select **Next**.
-   Create a CI to link to: Select **New**, define the CI, and then select **Next**.
 **Note:** To continue, you must connect each deployable to a service.

</td></tr></tbody>
</table>6.  Click **Next** to view the list of deployables on the **Edit deployables** tab.

    ![Choose how to create the new CDM application](../image/cdm-edit-deployables-tab.png)


## What to do next

The application is not yet structured to accept config data, so the next step is to add the data structure. See [Add the nodes that will contain config data to a new CDM application](cdm-data-structure-add-for-upload.md).

**Related topics**  


[CDM data model](../reference/cdm-data-model.md)

