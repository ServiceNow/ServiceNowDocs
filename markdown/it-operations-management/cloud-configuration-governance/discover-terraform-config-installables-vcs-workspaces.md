---
title: Run the IaC Discovery
description: Run the Infrastructure as Code \(IaC\) discovery to identify the resources of the Terraform environment.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Run the IaC Discovery

Run the Infrastructure as Code \(IaC\) discovery to identify the resources of the Terraform environment.

## Before you begin

-   Ensure that you have the appropriate API credentials for the Version Control System \(VCS\) accounts provisioned in the Terraform Enterprise or Terraform Cloud organizations. For more information, see [Create API key credentials for the Terraform account and the supported VCS account](create-vcs-credentials-for-terraform-connector.md).
-   Ensure that Terraform Open Source folders which contain the Terraform templates have unique names. If several Terraform template folders have the same name, multiple change tasks are created even though all the templates mayn't contain variable changes.

Role required: sn.cmp.cloud\_service\_designer

## About this task

Depending on the configuration provider, Cloud Services Catalog Terraform Connector discovers the following resources from the Terraform environment:

-   **Terraform Open Source**

    The IaC Discovery discovers the config installables \(Terraform templates\) from the Terraform Open Source server.

-   **Terraform Enterprise or Terraform Cloud**

    The IaC Discovery discovers the following items:

    -   Workspaces: Terraform workspaces provisioned in the Terraform organization.
    -   VCS: VCS repositories and branches provisioned in the Terraform organization.
    -   Agent pools:

        Terraform Cloud uses agents and agent pools to communicate with on-premise infrastructure. Deploy agents in the same network as your infrastructure to establish a connection between the infrastructure and Terraform Cloud. For more information on agents and agent pools, see [Terraform Cloud agents](https://www.terraform.io/cloud-docs/agents).

        Cloud Services Catalog Terraform Connector discovers the agent pools created in the Terraform Cloud. You can view the discovered agents in the Config Management module for your config provider. On the catalog order form, an agent pool filter enables you select an active agent to communicate with the private VMware infrastructure.

        **Note:** You can see agent pools option in the config management form and the catalog order form when the following conditions are met:

        -   You have created the VMware agent pools in the Terraform Cloud organization.
        -   You have VMware templates for Terraform Enterprise.
    -   Cfg installables: Terraform templates stored in the repositories of the VCS account provisioned the Terraform organization.

        **Note:** To discover the Terraform templates from the VCS, Cloud Services Catalog Terraform Connector requires the API key credentials of the VCS account.


## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

    The Cloud Admin Portal opens in a new browser tab.

2.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Config Management**.

3.  Select the Terraform provider card.

4.  Select **Discover Now**.

    **Note:** You can't cancel the IaC Discovery job after triggering it.

5.  To use Cloud Services Catalog Terraform Connector with Terraform Enterprise or Terraform Cloud, discover the Terraform templates stored in the provisioned VCS.

    1.  Select the **Tfe Vcs** tab.

    2.  From the Tfe Vcs list, select the VCS account that contains the Terraform templates you want to use for Cloud Provisioning and Governance catalog item creation.

    3.  From the Credentials drop-down list, select the API credential of the selected VCS account.

    4.  From the Related Links, select **Find Branches and Repositories**.

    5.  Repeat step [5.b](discover-terraform-config-installables-vcs-workspaces.md#cpg-tf-connector-select-vcs-record) to [5.d](discover-terraform-config-installables-vcs-workspaces.md#cpg-tf-connector-find-vcs-repo-branches) for all VCS accounts that contain the Terraform templates you want to use for Cloud Provisioning and Governance catalog item creation.

6.  Create an Infrastructure as Code \(Iac\) discovery schedule.

    IaC discovery schedule helps to discover new Terraform templates, workspaces, agent pools, and VCS branches for the specified config provider. It also detects changes in the already discovered Terraform templates. When Cloud Services Catalog Terraform Connector detects a change in the template variable or the template metadata, it automatically creates IaC change tasks for the affected catalog items.

    1.  On the Cloud Admin portal, navigate to **Manage** &gt; **IaC Discovery**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_wqs_cv5_p5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name of the IaC Discovery schedule.

</td></tr><tr><td>

Provider

</td><td>

Config management provider for which you are creating the discovery schedule.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the schedule.

</td></tr><tr><td>

Run

</td><td>

Frequency of schedule execution.Configure the schedule execution frequency in the Run field and its associated form fields.

</td></tr></tbody>
</table>    4.  Select **Submit**.


## What to do next

-   [Use multiple repositories structure with Terraform Connector app](use-multiple-repositories-structure-with-terraform-connector.md) with IaC Discovery
-   If Cloud Services Catalog Terraform Connector discovers new Terraform templates that you want to use for cloud resource provisioning, create a catalog item from the discovered template. For more information, see [Create a catalog item from the Terraform template](catalog-item-terraform-template.md).
-   If Cloud Services Catalog Terraform Connector has discovered changes in an existing template, take one of the following actions to resolve the associated IaC change task:

    -   Update the affected catalog item per the updated Terraform template.
    -   Deactivate the affected catalog item, and then create a catalog item per the updated template.
    For more information, see [Manage the Terraform template-based catalog items](create-or-update-terraform-based-catalog-item.md).


