---
title: Associate the Terraform input parameters with the Cloud Provisioning and Governance catalog item
description: Create a JSON file to store the variables that are used in the template file so that you can map them to discovered resources, pools, and filters. You can use variables or parameters from the Terraform template to map to fields on the catalog item provision form.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Associate the Terraform input parameters with the Cloud Provisioning and Governance catalog item

Create a JSON file to store the variables that are used in the template file so that you can map them to discovered resources, pools, and filters. You can use variables or parameters from the Terraform template to map to fields on the catalog item provision form.

## Before you begin

Role required: cloud\_designer

## About this task

Cloud Services Catalog Terraform Connector supports this capability for Terraform Open Source, Terraform Enterprise, and Terraform Cloud.

**Important:** When you use Terraform templates to create catalog items, the Location value specifies the datacenter or region to provision the configuration items and stacks. Use the metadata file to map other variables based on discovered resources, networks, profiles, pools and filters, and so on.

To auto-populate form fields in the catalog creation form while using Terraform templates, do the following:

-   Specify or define the key value pairs in the JSON file for variables that are defined in the Terraform template.
-   Configure variables to auto-populate fields and data in the **Cloud User Portal** &gt; **Cloud Catalog** &gt; **New** &gt; **Provision** page.

For more information on binding a parameter to a resource pool, see [Bind a parameter to a resource pool](../../cloud-management-v2/task/bind-param-snpool.md).

## Procedure

1.  In the directory or repository that is the basis for the catalog item, create a JSON file.

    **Important:** Name the JSON file `metadata.snc` and store it in the same directory or repository as the template \(.tf\) file. This naming convention enables discovery and parsing of the `metadata.snc` JSON file as part of the config installable.

2.  Specify the equivalent pool and filter as the data type for the Terraform variable in the `metadata.snc` JSON file.

    ```
    
      "Metadata": {
        "SNC::Parameter::Metadata": {
          "rgName": {
            "datasource": "ServiceNow::Pools:: ResourceGroupPool.getByLDC"
          },
          "Network": {
            "datasource": "ServiceNow::Pools::NetworkPool.getObjectsByLDC"
          },
          "Subnet": {
            "datasource": "ServiceNow::Pools:: SubnetPool.getObjectsByNetwork",
            "datasourceFilter": { "Network": "Network" }
          }
        }
      }
    
    ```

    The value that you specify in the variable field of the `metadata.snc` file is populated in the Provision section of the of the catalog item form.

    The following image shows the fields in the Provision tab of the catalog form. The values are auto-populate based on the variables defined in the `metadata.snc` file.

    ![Auto-populated values on Provision tab](../image/catalog-item-fields-metadata.png "Example: Auto-populated values on the Provision section of the catalog creation form")


**Parent Topic:**[Using Cloud Services Catalog Terraform Connector](../../cloud-management-v2/concept/using-ccg-terraform-connector.md)

