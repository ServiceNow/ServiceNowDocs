---
title: Support for continuous delivery \(configuration management\)
description: The Cloud Provisioning and Governance application supports integration with continuous delivery solutions \(also known as configuration management\). Ansible is supported as the default config management provider.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Support for continuous delivery \(configuration management\)

The Cloud Provisioning and Governance application supports integration with continuous delivery solutions \(also known as configuration management\). Ansible is supported as the default config management provider.

The Cloud Provisioning and Governance application supports configuration management providers in two ways:

-   **Application profile based approach**: Create an application profile for an entity and in the order catalog form, select that profile to deploy that entity. Each profile has a config installable. You can create multiple application profiles- as an example, one for PostgreSQL and one for Apache. Each profile can be mapped to a configuration management provider. In the Cloud User Portal, based on the profile you select, a configuration grid appears populated with attributes and values for that specific configuration management provider. You can modify any values in the order form and provision the entity.
-   **Resource block based approach**: Use a resource block, like Apache2, in a blueprint to represent an entity that a configuration management provider manages. The same resource block can be used to support more than one entity of the same kind. As an example, an Apache2 resource block can be used to support multiple Apache2 servers. In the order catalog form, select a provider type and then select a provider. Based on the specific provider, configuration management attributes and values appear. Once you provision the entity, you can save the configuration of the resource block and store it in the CMDB for future use.
-   **Post-provisioning actions during catalog deployment**: Users can call ansible job as a post-provisioning step in any catalog which deploys a VM. This will be executed as a day-2 operation once the VM installation is completed. For more information on the processes, see [https://www.servicenow.com/community/itom-blog/cpg-calling-ansible-job-as-post-provision-step-for-cloud-catalog/ba-p/2271552](https://www.servicenow.com/community/itom-blog/cpg-calling-ansible-job-as-post-provision-step-for-cloud-catalog/ba-p/2271552) and [https://www.servicenow.com/community/itom-blog/cpg-calling-ansible-job-as-day2-operation/ba-p/2270969](https://www.servicenow.com/community/itom-blog/cpg-calling-ansible-job-as-day2-operation/ba-p/2270969).

**Important:** Starting with the Orlando release, the cloud provisioning blueprints are available on instances upgraded from a previous release but you cannot create new blueprints. Existing blueprints and catalog items from those blueprints remain unaffected and continue to work.

## What to do

<table id="table_myg_bq3_lfb"><thead><tr><th>

Step

</th><th>

Goal

</th><th>

See these topics

</th></tr></thead><tbody><tr><td>

1. Create credentials for Ansible.

</td><td>

Enable Cloud Provisioning and Governance to access the configuration provider with the necessary credentials.

</td><td>

[Configure Ansible Tower user name and password](../../cloud-management-v2/task/configure-ansible-creds.md)

</td></tr><tr><td>

2. Create the workload provider type, and then create the provider.

</td><td>

Configure Cloud Provisioning and Governance to work with the configuration management provider of your choice. Then run discovery on the provider, using the credentials you provide, to find the resources that the provider already owns.

</td><td>

[Create a workload provider type](../../cloud-management-v2/task/create-workload-provider-type.md) and [Create an Ansible configuration management provider and run Discovery](../../cloud-management-v2/task/create-chef-or-ansible-cfg-provider.md)

</td></tr><tr><td>

3. Create an application profile with a mapping

</td><td>

Create the profile that defines the application that the configuration management provider manages. The profile is based on the discovered inventories in the provider.

</td><td>

[Create an application profile](../../cloud-management-v2/task/create-app-profile.md)

</td></tr><tr><td>

4. Create a blueprint

</td><td>

Create a blueprint with **BootstrapNode**, **Register Node**, and **ExecuteConfigPackages** operations on the virtual resource that the configuration provider manages. You can also customize the input parameters on the form to allow the user to select important inputs, like the application profile template, organization, and credential ID.

</td><td>

 

</td></tr><tr><td>

5. Provision a resource from the Cloud User Portal

</td><td>

The resource should provision, with the stack status indicating the **BootstrapNode**, **Register Node**, and **ExecuteConfigPackages** steps.

</td><td>

 

</td></tr></tbody>
</table>