---
title: Create a catalog item from a GitHub Actions template
description: Enable users to order items from an Employee Center service catalog through a GitHub Actions template.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Integrating GitHub Actions with Cloud-Services-Catalog, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a catalog item from a GitHub Actions template

Enable users to order items from an Employee Center service catalog through a GitHub Actions template.

## Before you begin

Ensure an appropriate GitHub Actions configuration provider exists. For more information, see [Run Discovery on GitHub Actions config provider](run-discovery-on-github-actions-config-provider.md).

Ensure that the workflow of the GitHub Actions adheres to the following syntax:

-   Required input variable: deploymentID
-   Mandatory attribute: run-name

Role required: sn\_cmp\_cloud\_service\_designer

## Procedure

1.  Create a catalog item

    1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

    2.  Navigate to **Design** &gt; **Cloud Catalog Items**.

    3.  Select **New**.

    4.  On the form, fill in the fields.

        |Field Name|Description|
        |----------|-----------|
        |Name|Unique and descriptive name of the catalog item.|
        |Source|Should be set to **Configuration Management Template** list.|
        |Provider Type|Should be set to**GitHub Actions**.|
        |Provider|Name of the GitHub Actions configuration provider.|

    5.  Save the Cloud Catalog item form.

2.  Associate a GitHub Actions template with the catalog item.

    1.  From the Cloud Templates related list, select **New**.

    2.  From the Configuration Installable drop-down list, select the GitHub Actions template.

    3.  Save the ServiceNow Cloud Templates Versions form.

    4.  Select **Activate** to activate the cloud template.

3.  Add or remove catalog item form fields by editing the variable sets associated with the catalog item.

4.  Activate the catalog item by selecting the **Active** check box.

5.  Select **Update**.


## Result

GitHub Actions catalog items can be ordered from the Employee Center catalog order form.

**Parent Topic:**[Integrating GitHub Actions with Cloud-Services-Catalog](../concept/integrating-github-actions-with-cloud-service-catalog.md)

