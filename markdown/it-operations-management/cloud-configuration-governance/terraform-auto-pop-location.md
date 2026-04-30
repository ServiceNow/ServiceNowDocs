---
title: Populate the datacenter in Terraform-based catalog items
description: In any request for a catalog item using Terraform templates, the required Location value specifies the datacenter or region where to provision the configuration items and stacks. You can use a variable named region in the Terraform template to map to the Location field on the request form.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Populate the datacenter in Terraform-based catalog items

In any request for a catalog item using Terraform templates, the required Location value specifies the datacenter or region where to provision the configuration items and stacks. You can use a variable named **region** in the Terraform template to map to the Location field on the request form.

## Before you begin

Role required: cloud\_designer

## Procedure

1.  In the template file that is the basis for the catalog item, define a variable named **region**.

    ```
    variable "region" {
                     type="string"
                   }
    ```

    -   The field defined for the **region** variable does not appear on the Provision section of the request form for the catalog item \(the Location field serves that purpose\).
    -   The value that the user specifies for the Location field on the request form configures the datacenter or region for the resource.

**Parent Topic:**[Using Cloud Services Catalog Terraform Connector](../concept/using-ccg-terraform-connector.md)

