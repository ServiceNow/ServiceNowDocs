---
title: Preparing an application for config data upload
description: An application in CDM is the full collection of config data for an application service, application model, or dynamic CI group \[infrastructure\] in the CMDB. After you upload your source config data, the application can support all potential deployables that make up each version of the development, test, and production environments of the service.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Uploading your config data, Configuring DevOps Config, DevOps Config, IT Service Management]
---

# Preparing an application for config data upload

An application in CDM is the full collection of config data for an application service, application model, or dynamic CI group \[infrastructure\] in the CMDB. After you upload your source config data, the application can support all potential deployables that make up each version of the development, test, and production environments of the service.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## Overview: Preparing an application to accept uploaded config data

You follow this general process to prepare an application to accept the upload of config data:

1.  On the **Apps** tab, you, a user with the CDM Admin \[sn\_cdm.cdm\_admin\] role, create an application record.

    The system generates an application that includes several standard folders in a hierarchical structure. You will map your existing config data into this data structure to enable the benefits that are described in [CDM data model](../reference/cdm-data-model.md).

    ![Data structure for a new application. You will add your config data as nodes in the appropriate folder](../image/cdm-data-structure.png)

    The application supports creation of multiple deployables. For example, you might create a deployable for each typical environment: Development, Test, and Production. You might also create multiple versions of each deployable for each environment type.

2.  Working in the CDM code editor, you now create a changeset — a draft copy of the application that you can edit.
3.  While working in the changeset, you create the following types of nodes in the appropriate folders. This process models the config data, that is, it prepares the application to map your source config data into the CDM data structure.

    **Note:**

    Starting with Configuration Data Management version 4.2, you can define a node using any UTF-8 character, including the forward slash \(`/`\).

4.  Now that the structure is in place, you use the REST APIs or the CDM code editing panel to upload your existing configuration data into the changeset. The process is described in [Uploading your config data](cdm-upload-process.md). For more information, see CdmApplicationsAPI, CdmChangesetsAPI, and CdmSnapshoAPI.

    **Note:** If you're uploading an XML or CSV file to import your existing config data into CDM, the CDM parser parses the data in a specific way. For more information, see [Parsing of XML files in CDM](cdm-parsing-xml-file.md) and [Parsing of CSV files in CDM](cdm-parsing-csv-file.md).

    You can upload the following types of datasets: component variables, components, collections, and deployables.

    -   **Components**

        Components are the building blocks that typically represent the config data for a logical element of an application or a part of an infrastructure service. For example, a monolithic app, a micro-service, a physical server, or a Docker template.

        A component can contain variables that can take on different values in collections and deployables. More detailed instructions appear in [Define or update a component](../task/cdm-component-define.md).

    -   **Collections**

        A collection is the set of components that together define a release — You can think of a collection as a release composition.

        A collection can contain variable or override settings that are specific to the particular version. For example, the VM config data used in release-1 is different from the data used in release-2. release-1 might use the value `2Gb` for the *memory* setting \(`"memory": "2Gb"`\) and release-2 might specify a different value \(`"memory": "4Gb"`\). In addition, a collection might include config settings that do not appear in its components. You might think of such values as "overlays".

    -   **Deployables**

        A deployable is a config dataset \(for a development, test, or production environment\) that can be deployed into your CI/CD pipeline as a service. Each deployable in an application configures a service in the CMDB. For example, you might create three deployables, one for each environment type: Development, Test, and Production.

        A deployable is made up of the collection or set of collections that define the release for a particular environment. The combination of collections+environment link to an application service in the CMDB or an infrastructure service.

        A deployable can contain variable or override settings that are specific to the environment. For example, the `database` variable has one value in the development environment and a different value in the production environment. An override value in the production deployable might specify a required container parameter that is not needed in the development environment.

5.  After the data is uploaded, you return to CDM. You update variable and override values so that the relatively small set of components and collections can provide config data for all three deployable environments. For example, the `Development` deployable can use the same components and collections as the `Test` deployable. `Development` uses the default *database* variable value. `Test`, in contrast, uses a different value that is appropriate for the test environment.
6.  Now, save and commit the changeset. The system performs the following actions:
    -   Determine whether there are conflicts with other earlier commits. If the system reports a conflict, you must resolve it and recommit or create a changeset and redo your changes. For more information on conflict resolution, see [Conflicts between changeset commits](cdm-changeset-conflicts.md).
    -   Push all changes into the data model of the application \(the config data is persisted\).
    -   Generate a snapshot of each deployable that is affected by the changes in the changeset. The system validates config data by executing specified policies against a snapshot. At the moment that the snapshot is created, the snapshot can be published and used to export the config data. Snapshots are permanent records that cannot be edited.

The source config data is now held in CDM tables. You can now manage the data as needed: map policies to each deployable so that the snapshots can be validated, validate the data in a snapshot \(apply the policies\), export config data, and so on.

**Note:** You can map policies to an empty deployable, but that is not a typical procedure.

**Related topics**  


[Define or update a component](../task/cdm-component-define.md)

[Define or update a collection in an application](../task/cdm-collection-define.md)

[Create and update a deployable](../task/cdm-deployable-define.md)

[Changesets and version control in CDM](cdm-changesets-version-control.md)

[Conflicts between changeset commits](cdm-changeset-conflicts.md)

[Validating and correcting configuration data](cdm-validating-cfg-data.md)

