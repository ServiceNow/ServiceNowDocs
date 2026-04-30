---
title: Integrating Ansible with Cloud Services Catalog
description: Integrate Ansible with Cloud Services Catalog as a Day 1 activity. With this activity, you can deploy an Ansible job template via a ServiceNow catalog item.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Integrating Ansible with Cloud Services Catalog

Integrate Ansible with Cloud Services Catalog as a Day 1 activity. With this activity, you can deploy an Ansible job template via a ServiceNow catalog item.

As a cloud\_service\_user, you can access the config provider and job templates and deploy a job template through a catalog item.

<table id="simpletable_lz2_bfp_fyb"><thead><tr><th>

Day 0 support

</th><th>

Day 1 support

</th><th>

Day 2 support

</th></tr></thead><tbody><tr><td>

1.  Retrieve the resources from the cloud and update the CMDB
2.  Verify that there are no errors. If errors are displayed, then the Discovery or job template deployment has failed

</td><td>

1.  Order an Ansible job template from Service Catalog
2.  Reference the discovered Microsoft Azure pipelines that are specific to Ansible
3.  Select inputs that are needed for the release deployment pipeline
4.  Submit a catalog
5.  Publish an Out Of Box catalog item as Cloud Services Catalog content
6.  Select the job templates that you have access to and deploy them

</td><td>

1.  Fix the mapping of Out Of Box via Cloud Services Catalog content
2.  Update documentation on limiting the job template to run on a specific host
3.  Test and document how to support the job template deployment on unmanaged nodes
4.  Start your Day 2 support for Ansible AWX

</td></tr><tr><td>

Store in CMDB as referrable objects.

</td><td>

1.  Wait for the order approval
2.  Track the progress of your template order
3.  Update CMDB with the deployed resources

</td><td>

1.  Ensure all the Day 2 support actions execute successfully
2.  Switch between the blue \(current application\) and green \(new application\) environment

</td></tr></tbody>
</table>-   **[Set up Ansible as a Day 1 task](../task/setting-up-ansible-as-day-one-task.md)**  
Set up the Ansible console as a Day 1 task before you run Discovery and deploy a job template via a ServiceNow catalog item by using the Cloud Services Catalog application.
-   **[Run Discovery on the Ansible config provider](../task/running-discovery-on-ansible-config-provider.md)**  
Add the Ansible config provider and run Discovery to discover what's in the inventory, the host group, and the available job templates.
-   **[Order an Ansible job template](../task/ordering-ansible.md)**  
Use Cloud Services Catalog to order an Ansible job template called from the catalog item.

**Parent Topic:**[Configuring Cloud Services Catalog](configuring-csc.md)

