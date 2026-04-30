---
title: Cloud Provisioning and Governance: Terraform Connector Terraform Catalog Item Task form reference
description: Use the Terraform Catalog Item Task form to specify the action you want to take to resolve the catalog item change task.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cloud Provisioning and Governance: Terraform Connector reference, Cloud Provisioning and Governance: Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Cloud Provisioning and Governance: Terraform Connector Terraform Catalog Item Task form reference

Use the Terraform Catalog Item Task form to specify the action you want to take to resolve the catalog item change task.

<table id="table_o2q_xcp_w5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog Item Task Action

</td><td>

Action that you want to take.-   Update catalog item with this template version

Select this option to update the catalog item with this template version. A new version of the template is created and activated while the existing template version is retired and rendered inactive.

-   Create catalog item with this template

Select this option to create a catalog item with the existing catalog item name and append the catalog item name with a number. For example, if your catalog item is named `Linux VM`, the new catalog is created with the name `Linux VM 1`. The catalog item is automatically activated and available for provisioning from the Cloud User portal.


</td></tr><tr><td>

Assignment Group

</td><td>

The assignment group to which you're assigning the catalog item task.

</td></tr><tr><td>

Assigned to

</td><td>

The user to whom you're assigning the task.

</td></tr><tr><td>

Short Description

</td><td>

Brief description of the task.

</td></tr><tr><td>

Approval

</td><td>

The approval status of the task.

</td></tr><tr><td>

Work Notes

</td><td>

Any notes that you want to enter for the task record.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Provisioning and Governance: Terraform Connector reference](cpg-terraform-connector-reference.md)

