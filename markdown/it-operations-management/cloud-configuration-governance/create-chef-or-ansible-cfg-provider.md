---
title: Create an Ansible configuration management provider and run Discovery
description: Create an Ansible configuration management provider, and then run Discovery on the provider to find its resources.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create an Ansible configuration management provider and run Discovery

Create an Ansible configuration management provider, and then run Discovery on the provider to find its resources.

## Before you begin

-   Ensure to have an Ansible server and [Ansible credentials](configure-ansible-creds.md).
-   If you want to use Ansible Tower version 3.6.x or higher, ensure to set the mid.cmp.ansible.api\_version property to V2. You can access this property under the Properties section of the Mid Server module.
-   Role required: cloud\_admin

## About this task

**Important:** Starting with the Orlando release, the cloud provisioning blueprints are available on instances upgraded from a previous release, but you cannot create a blueprint. Existing blueprints and catalog items created from those blueprints remain unaffected and continue to work.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Config Management**.

2.  Select **New**.

3.  On the form fill in the fields.

    **Note:** Most information required to create an Ansible configuration management provider comes from the Ansible Tower server settings.

<table id="table_gy2_2wg_sz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the configuration provider.

</td></tr><tr><td>

Organization

</td><td>

Ansible Tower organization for access controlYou can obtain this information from the configuration management provider console.

</td></tr><tr><td>

URL

</td><td>

URL of the Ansible Tower.Enter the full URL of the Ansible Tower including the `https://<IP>` protocol.

</td></tr><tr><td>

Provider

</td><td>

Configuration provider type.Select **Ansible Tower** from the drop-down list.

</td></tr><tr><td>

Server Type

</td><td>

Ansible Tower server type.

</td></tr><tr><td>

Credential

</td><td>

Credentials to access the Ansible server. For more information on creating credential for Ansible server, see [Ansible credentials](configure-ansible-creds.md).

</td></tr><tr><td>

Version

</td><td>

Version of the configuration provider you are creating. **Note:** For Ansible Tower versions higher than 3.1.2, select 3.4.0 from the list.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select the Ansible Tower configuration provider card.

    ![Config providers](../image/config-providers.png)

6.  Select **Discover Now** to find the resources in the Ansible configuration management provider.

    **Note:** If you provision or otherwise change resources through the configuration management provider interface, you must manually run discovery again through the Config Providers page. You cannot create a scheduled discovery for configuration management providers.

    The discovered resources appear under **Entities**.

    The following Ansible Tower resources are discovered:

    -   **Ansible Inventory**: Displays the discovered applications and virtual resources.
    -   **Cfg Installable**: Displays theactual components that run when the applications install. For Ansible, the items in this list are job templates, which are also referred to as runlists in this form.
    ![Example Ansible inventories](../image/ansible-inventory.png "Example Ansible Inventory")

    ![Ansible resources](../image/cfg-ansible-resources.png "Ansible config installables (job templates)")

7.  Select **Ansible Inventory** to explore the contents.

    **Note:** Communicate the supported applications to users so they can select the correct application from the **Hostgroup** field in the Cloud User Portal. The **Hostgroup** field shows all possible applications \(called Groups in Ansible\), not just the ones that the configuration management provider supports. Therefore, the provisioning fails when the user selects an unsupported application.

    ![Ansible Tower groups within an inventory](../image/ansible-tower-groups.png "Ansible Tower groups within an inventory")


## What to do next

After a user provisions a resource, the Stack Status indicates how the system runs through the Create node, Bootstrap, and ExecuteConfigPackage steps. You can obtain the IP address of a virtual machine in the User Portal by navigating to **Stacks** &gt; **\{category\}** and selecting the new virtual machine. Open the configuration management provider server to see the newly provisioned resource on the node that the user specified.

