---
title: Set up Ansible as a Day 1 task
description: Set up the Ansible console as a Day 1 task before running Discovery and deploying job templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-services-catalog/setting-up-ansible-as-day-one-task.html
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Ansible, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Ansible as a Day 1 task

Set up the Ansible console as a Day 1 task before running Discovery and deploying job templates.

## Before you begin

Set the deploymentID on the extra variables for Ansible job templates.

Select the **Prompt on launch** option next to the variables section in the template. This action allows you to update or override the default extra\_vars with values from the catalog order form when launching the template.

Tag all resources with the deploymentID key to enable Discovery after provisioning.

Role required: admin

## Procedure

1.  Save the extra variables in a JSON format locally, to discover and update Configuration Management Database \(CMDB\).

2.  Create Ansible tower credentials to be used in Ansible Discovery.

    For more information, see [Configure Ansible Tower user name and password](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-configuration-governance/configure-ansible-creds.md).

3.  Allow the extra variables and job templates to be overridden.

    The default Ansible job template must be overridden for the pipeline to work with a Cloud Services Catalog Ansible automation catalog item.


**Parent Topic:**[Integrating Ansible with Cloud Services Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/cloud-services-catalog/integrating-ansible-with-cloud-services-catalog.md)

