---
title: Set up Ansible as a Day 1 task
description: Set up the Ansible console as a Day 1 task before you run Discovery and deploy a job template via a ServiceNow catalog item by using the Cloud Services Catalog application.
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Ansible with Cloud Services Catalog, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Ansible as a Day 1 task

Set up the Ansible console as a Day 1 task before you run Discovery and deploy a job template via a ServiceNow catalog item by using the Cloud Services Catalog application.

## Before you begin

Set the deploymentID on the extra variables for Ansible job templates.

Select the **Prompt on launch** option next to the variables section in the template. If you don't do this action, you can't update or override the default extra\_vars that is defined with the values from the catalog order form, while you are launching the template.

Tag all resources with the deploymentID key to enable Discovery after provisioning.

Role required: admin

## Procedure

1.  Save the extra variables in a JSON format locally, to discover and update Configuration Management Database \(CMDB\).

2.  Create Ansible tower credentials to be used in Ansible Discovery.

    For more information, see [Configure Ansible Tower user name and password](../../cloud-management-v2/task/configure-ansible-creds.md).

3.  Allow the extra variables and job templates to be overridden.

    The default Ansible job template must be overridden for the pipeline to work with a Cloud Services Catalog Ansible automation catalog item.


**Parent Topic:**[Integrating Ansible with Cloud Services Catalog](../concept/integrating-ansible-with-cloud-services-catalog.md)

