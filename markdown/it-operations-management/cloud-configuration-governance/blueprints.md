---
title: Cloud Provisioning Blueprints
description: A blueprint is a specialized catalog item template for offering cloud services, or stacks, to cloud users. Blueprints work with any cloud service provider, such as Amazon AWS Cloud or Microsoft Azure Cloud. Blueprints are in restricted usage from the Orlando release.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Cloud Provisioning Blueprints

A blueprint is a specialized catalog item template for offering cloud services, or stacks, to cloud users. Blueprints work with any cloud service provider, such as Amazon AWS Cloud or Microsoft Azure Cloud. Blueprints are in restricted usage from the Orlando release.

## Blueprint components

**Note:**

-   Starting with Orlando, Cloud Provisioning blueprints are available on instances upgraded from a previous release but you cannot create new blueprints. Resource profiles and custom-created blueprints will no longer be supported starting with the Australia release.
-   Use Cloud Provisioning cloud templates to create catalog items in place of blueprints. Cloud Provisioning [cloud templates](../task/create-cloud-template.md) allow you to ingest Azure ARM, AWS CFT, Google Deployment Manager \(GDM\) and Terraform specification syntax in cloud catalog items to run your cloud deployment orchestration.

The blueprint is the mechanism that is passed to the cloud provider to establish the cloud assets. Requesting a cloud catalog item is called launching a stack. After the cloud asset is obtained, it can then be discovered, managed, and maintained.

![Blueprint components](../image/bp-components.png "Blueprint deployment model components")

-   **Resource blocks**

    The cloud resources included in the blueprint \(catalog item\). For example, a resource block can contain a virtual machine, an app that runs on the VM, and information about the datacenter that hosts the VM. Also referred to as resources.

-   **Connections**

    The relationship between resources. For example, the VM has a host relationship with the app. There are two types of connections, containment and attached to.

    -   Containment: a connection where resource block contains another, visually depicted as a top-down relationship as shown in the image. For example, the blueprint container must contain at least one other resource block.
    -   Attached to: a connection between resources that require binding for direct communication to each other, visually depicted as a side-by-side relationship. For example, the binding between a virtual machine and storage forms an attached to relationship.
-   **Operations**

    The actions that are performed on resource blocks or on the resource stack to manage the resources. For example, the cloud user can provision, start, and stop a resource.

-   **Resource operations**

    The steps to perform the operation on the resource. For example, to provision the catalog item, the system must provision the VM and the app that runs on the VM. Click an operation to drill into the resource operations.

-   **Attributes**

    The details of the resource. Attributes can appear on the catalog item form as catalog properties. For example, the blueprint can provide the version of the app to provision to the VM.

-   **Constraints**

    An attribute option to constrain a cloud-agnostic resource block, such as a logical datacenter, to be used with a specific cloud provider. For example, a logical datacenter can be constrained to Amazon AWS Cloud. Later, if you switch or add Microsoft Azure Cloud or another cloud provider, you can change the constraint as needed.


## Planning blueprints

Before creating blueprints, plan the stacks you want to offer in the service catalog. Prepare the following information before you begin development.

-   **Resource blocks**

    Plan the resource blocks you want to use in blueprints. Ensure that the appropriate resource blocks are available to use in blueprints, and add them if necessary.

-   **Service offerings \(stacks\)**

    To plan a service offering or stack, diagram the resource blocks that it needs, and how they are connected.

-   **Cloud accounts and datacenters**

    Obtain a list of the cloud accounts and datacenters that the cloud administrator has configured. Determine whether any are constrained.

-   **Service catalog variables and variable sets**

    Ensure that you have an understanding of how service catalog items use variables and variable sets. Understanding service catalog items and processes help with your understanding of blueprints.


## Start here

[Build a Cloud Provisioning blueprint](../task/create-blueprint-cmp.md)

-   **[Build a Cloud Provisioning blueprint](../task/create-blueprint-cmp.md)**  
Use the blueprint designer to create custom blueprints for the Cloud Provisioning and Governance application. Blueprints are deprecated in the Orlando release.
-   **[Form configuration with blueprints](blueprint-form-configuration.md)**  
Blueprints control what the user sees on the catalog order form. You can configure the form to show or hide fields, populate fields with default values, and otherwise create a unique form for the user based on criteria.

**Parent Topic:**[Cloud Admin Portal](cloud-admin-portal.md)

