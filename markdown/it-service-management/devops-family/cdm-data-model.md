---
title: CDM data model
description: The CDM data model is a standardized data structure that supports the broader life cycle of software delivery — automation, quality validation, and CSDM. CDM imports existing config data, validates it using policies that you define, and exports valid config data to your organization's existing DevOps pipeline to implement applications, services, and infrastructure.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Reference, DevOps Config, IT Service Management]
---

# CDM data model

The CDM data model is a standardized data structure that supports the broader life cycle of software delivery — automation, quality validation, and CSDM. CDM imports existing config data, validates it using policies that you define, and exports valid config data to your organization's existing DevOps pipeline to implement applications, services, and infrastructure.

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## CDM data model overview

The CDM data model does not change the way you think about configuration. Rather, you use the CDM REST API and user interface to map your existing JSON, YAML, INI, XML, and other config data into an intuitive data structure that provides the following benefits:

-   Implements rigorous and transparent version and change control.
-   Enables you to encrypt sensitive data and ensures appropriate access control for the data.
-   Enables automated validation of config data.
-   Enables you to reuse config data structures by using variables, including values, and overlaying values.

## Structure of the CDM data model

An application in CDM is the full collection of config data for an application service, application model, or dynamic CI group \[infrastructure\] in the CMDB. The CDM user creates an application record that includes the following empty folders in a standard hierarchical structure. After the system ingests your existing config data, you structure the data into components in the appropriate folder. You create collections of the components and then combine the collections into a deployable — a config dataset \(for a development, test, or production environment\) that can be deployed by your delivery process. Each component, collection, variable, and deployable is a node in the structure.

![Folder structure for a new CDM application](../image/cdm-data-structure.png)

-   **Components**

    Components are the building blocks that typically represent the config data for a logical element of an application or a part of an infrastructure service. For example, a monolithic app, a micro-service, a physical server, or a Docker template.

    A component can include descendent components, either direct or included. A component can include variables that can take on different values in collections and deployables.

    You can group components into a library of shared components.

    **Tip:** It is often useful to define a default value for a variable in a component or collection. This is a powerful strategy because you can create a broad variety of deployables from a small set of components and collections. Deployables that inherit a component or collection can use overrides, overlays, and variable settings to meet the needs of the environment type. For example, the `Development` deployable can use the same components and collections as the `Test` deployable. `Development` uses the default *database* variable value. `Test`, in contrast, uses a different value that is appropriate for the test environment.

-   **Components Vars folder**

    The components **Vars** folder can contain variables that any CDI in the **Components** folder can use. There is only one components **Vars** folder.

-   **Collections**

    A collection is the set of components that together define a release — You can think of a collection as a release composition.

    A collection can include variable or override settings that are specific to the particular version. For example, the VM config data used in release-1 is different from the data used in release-2. release-1 might use the value `2Gb` for the *memory* setting \(`"memory": "2Gb"`\) and release-2 might specify a different value \(`"memory": "4Gb"`\). In addition, a collection might include config settings that do not appear in its components. Such values are called overlays.

    A collection might represent a particular version of an application, localization, or feature set. For example, a collection named `collection-2` might include the set of components or component versions that represent the `Release 2.0` functionality for the application. In contrast, a collection named `collection-3` that represents the `Release 3.0` functionality might include the same set of components or component versions, additional components or component versions, and other variable, override, and overlay settings.

-   **Collections Vars folder**

    The collection **Vars** folder can contain variables that any CDI in the **Collections** folder can use. Each collection has one collection **Vars** folder. A collection variable has higher precedence than a component variable.

-   **Deployables**

    You add and configure deployables in the data structure. A deployable is a config dataset \(for a DEV, TEST, or PROD environment\) that can be deployed by your delivery process. Each deployable in an application represents the configuration of a service in the CMDB.

    A deployable is made up of the collection or set of collections that define the release for a particular environment. The combination of collections+environment link to an application service in the CMDB or to an infrastructure service.

    A deployable can include variable or override settings that are specific to the environment. For example, the `database` variable has one value in the development environment and a different value in the production environment. An override value in the production deployable might specify a required container parameter that is not needed in the development environment.

    An example deployable named `DEV-2` would include the `collection-2` collection and would specify variable, override, and overlay settings that are specific to the development environment for release 2.0. In contrast, the deployable named `PROD-2` would also include the `collection-2` collection but, instead, would specify settings that are specific to the production environment for release 2.0.

    When you are happy with a changeset, you can save and commit the changes. The system checks for conflicts with the committed changesets of other users. If there are no conflicts, the system persists the changes and then generates a snapshot of every deployable that is affected by the changes. A snapshot represents a potential exportable config data set. The system validates config data by executing policies against each snapshot and returning the validation results.

-   **Deployable Vars folder**

    The deployable **Vars** folder can contain variables that any CDI in the **Deployables** folder can use. Each deployable has one deployable **Vars** folder. A deployable variable has higher precedence than a collection variable.


## Example

In the following diagram of the example BookStore application, the numbers identify the relationships among components, collections, and deployables.

1.  Components are grouped to form collections that represent environments or versions of environments. The FS2 \(feature set 2\) collection has config data for Core version 2 of the application that is currently being developed and tested. FS1, in contrast, holds the earlier Core version 1 that has been thoroughly tested and is currently running the application in the production environment.
2.  In the example, both FS2 \(the collection that is used in test environments\) and FS1 \(the collection that is used in the production environment\) use config data for both **S3** and a particular **VM template**. Both the FS1 and FS2 collections, therefore, inherit these two components. Because the collections represent different feature sets, it is probably the case that FS1 and FS2 use variables or overrides to specify a few different settings for the components.
3.  Each deployable includes the collection that is appropriate for its environment \(development, test, or production\). In the example, the TEST deployable uses the FS2 collection, the newer version of the feature set and other config settings that is used in test environments. The PROD deployable, in contrast, uses FS1 in the production environment. FS1 is the earlier version of the collection of config data that had been validated for production.

    In each deployable, variables are set to values that are appropriate for the environment. For example, in PROD, the *database* variable is set to `prod1` \(the production database\). The TEST deployable, however, specifies one of the databases that is used by the testing team, `test3`.


This diagram is simplified. In your implementation, deployables can include multiple collections, variable and override settings, and overlay settings \(settings that do not appear in the components and collections that make up the deployable\). In addition, you might have several deployables for each environment type.

![How components and collections supply content that you can build into deployables for a variety of environments](../image/cdm-app-dynamics.png)

## Definitions

-   **CDI**

    A config data item \(CDI\) is simple a key-value node.

-   **Variable**

    A variable is a key-value item that can be referenced within a CDI.

-   **Parent nodes and child \(leaf\) nodes**

    -   CDIs and variables are key-value items. CDIs and variables can only be child nodes.
    -   Components, collections, deployables, and folders nodes can be parent nodes—nodes that can have key-value items or other parent nodes.
    **Note:**

    Starting with Configuration Data Management version 4.2, you can define a node using any UTF-8 character, including the forward slash \(`/`\).

-   **Name path**

    The name path is the complete folder path of the selected node in the list. In REST API, you can provide name path in array in the following formats:

    -   Backslash format: For example - testApp/deployables/Development1/cdi1

        **Note:** If your node name contains a backslash \("/"\), you can't use this format.

    -   Backend name path with replacement characters: For example - testApp�deployables�Development1�cdi1
    -   Array: For example - \['testApp','deployables','Development1','cdi1'\]
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

-   **Changesets and Snapshots**

    When you commit changes to a CDM application, the system persists the changes as a changeset of the application. The system then also generates a snapshot of every deployable that is affected by the changes. A snapshot represents a potential exportable config data set. The system validates config data by executing policies against each snapshot and returning the validation results. Snapshots that pass validation and that are published can be exported to the release pipeline as config data.

-   **Shared components and Component libraries**

    Shared components in Configuration Data Management enables you to use a component across several applications.

    For better organization, these shared components are managed in Component libraries. These component libraries improve consistency and maintainability by ensuring a single source of truth for a component's config data across applications.

-   **File nodes**

    A file node is created when you attach a file to the config data model of a CDM app or a component library. It contains a link to the attached file. Using file nodes, you can attach files of any MIME type supported on ServiceNow AI Platform.


-   **[Contextual variables for config data](cdm-context-var.md)**  
Contextual variables are out-of-the-box variables delivered by ServiceNow that enable you to use the context of a node to define a variable.

**Parent Topic:**[DevOps Config reference](../../devops-config/reference/devops-config-reference.md)

**Related topics**  


[Preparing an application for config data upload](../concept/cdm-prep-app-for-upload.md)

[Create and update a deployable](../task/cdm-deployable-define.md)

