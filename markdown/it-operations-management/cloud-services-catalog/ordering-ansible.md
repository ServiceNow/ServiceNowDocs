---
title: Order an Ansible job template
description: Use Cloud Services Catalog to order an Ansible job template called from the catalog item.
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating Ansible with Cloud Services Catalog, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Order an Ansible job template

Use Cloud Services Catalog to order an Ansible job template called from the catalog item.

## Before you begin

Role required: cloud\_service\_user

## About this task

You can use the Ansible Job template deployment form to call an Ansible job template and run it via a ServiceNow catalog item for deployment.

## Procedure

1.  Navigate to **Employee Center** &gt; **Cloud Services** &gt; **Integrations** &gt; **CSC Ansible Automation**.

    ![Ansible Job template deployment form.](../image/ansible-template-form.png "Ansible Job template deployment form")

<table id="table_qmb_hgt_41c"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

UserGroup

</td><td>

User group that is assigned to the user.

</td></tr><tr><td>

Provision

</td><td>

Provisioning details. Select the Workload Config Provider and ApplicationProfile from the Ansible Tower.

</td></tr><tr><td>

Choose Service Account

</td><td>

Pipeline. For Amazon Web Services, the Location list is displayed when you select **Service Account**. The location is not required for Discovery in Microsoft Azure.**Tip:**

You can expose an extra variable that was saved in a JSON format at the Ansible tower location or region and use it in the template for provisioning. This extra variable is overridden by the value that you selected in the Location list. By using this extra variable, you ensure that provisioning and Discovery are at the same location.

These settings ensure that the correct resources that are related to the stack are populated in CMDB. You can run Discovery based on those settings.

</td></tr><tr><td>

Choose Cloud Location

</td><td>

Service account that is associated logical datacenter \(LDC\) for Discovery.

</td></tr><tr><td>

Extra Variables

</td><td>

Extra variables that you can modify even if the values are automatically filled in and masked.

</td></tr></tbody>
</table>2.  Set up the identifying tags.

    The DeploymentID field is read-only and auto-generated for the order. The DeploymentID is assigned as a tag to all the provisioned resources if you added it as a tag in the Azure DevOps pipeline template of the stacks in the cloud. The DeploymentID is also assigned as a tag to the stack. If the pipeline has any of these three variables \(Application, BusinessService or CostCenter\), they are displayed in the General info in the Ansible Job Template form UI.

3.  Select the field values from the list to be updated in the pipeline variables.

    These entries are considered for the current order only.

    **Note:** You can do only the resource level actions on a provisioned stack because the stack level action is turned off. The previous stack is marked as obsolete if you run the pipeline again, although the resources remain in the cloud.


## What to do next

Verify that a blueprint approval policy \(CSC Content Approval Policy Ansible\) is applied. This policy mandates that approval must be obtained from the Change management group before any provisioning can take place.

**Parent Topic:**[Integrating Ansible with Cloud Services Catalog](../concept/integrating-ansible-with-cloud-services-catalog.md)

