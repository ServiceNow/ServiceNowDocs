---
title: Set up Ansible as a Day 1 task
description: Set up the Ansible console as a Day 1 task to enable job template deployment through catalog items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/cloud-services-catalog/setting-up-ansible-as-day-one-task.html
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating Ansible with Cloud Services Catalog, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up Ansible as a Day 1 task

Set up the Ansible console as a Day 1 task to enable job template deployment through catalog items.

## Before you begin

Set the deploymentID on the extra variables for Ansible job templates.

Select the **Prompt on launch** option next to the variables section in the template. Without this option, you can't update or override the default extra\_vars when launching the template. The default extra\_vars are defined with values from the catalog order form.

Tag all resources with the deploymentID key to enable Discovery after provisioning.

Role required: admin

## Procedure

1.  Save the extra variables in a JSON format locally, to discover and update Configuration Management Database \(CMDB\).

2.  Create Ansible tower credentials to be used in Ansible Discovery.

    For more information, see [Configure Ansible Tower user name and password](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/configure-ansible-creds.md).

3.  Allow the extra variables and job templates to be overridden.

    The default Ansible job template must be overridden for the pipeline to work with a Cloud Services Catalog Ansible automation catalog item.


**Parent Topic:**[Integrating Ansible with Cloud Services Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-services-catalog/integrating-ansible-with-cloud-services-catalog.md)

