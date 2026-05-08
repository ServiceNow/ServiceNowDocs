---
title: Create a Terraform Open Source config provider
description: Create a Terraform Open Source config provider in Cloud Provisioning and Governance. The Terraform Open Source config provider enables Cloud Provisioning and Governance to discover the Terraform Open Source config installables \(Terraform templates\) and detect changes in them.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a Terraform Open Source config provider

Create a Terraform Open Source config provider in Cloud Provisioning and Governance. The Terraform Open Source config provider enables Cloud Provisioning and Governance to discover the Terraform Open Source config installables \(Terraform templates\) and detect changes in them.

## About this task

Starting this release, you can use OpenTofu with Cloud Provisioning and Governance. You must have admin rights to configure the alias name for at the vm host level.Ensure that server is running on Windows or Linux operating system.

## Before you begin

-   Ensure that a supported Terraform Open Source version is installed in the server. Cloud Services Catalog Terraform Connector supports Terraform Open Source versions 1.1.0 through 1.1.9 and 1.2.0 or higher
-   If you want to use a minor or patch version of the Terraform Open Source CLI, ensure that the minor or patch version is added to the workload config provider. For more information, see [Add support for minor or patch versions of the Terraform](../../cloud-management-v2-setup/task/terraform-use-minor-patch-version-cli.md).
-   Ensure that the MID Server can access the Terraform server.
-   Ensure that the MID Server has Terraform capability.
-   As a new user, add Terraform MID capability to provision resources using Terraform Open-source host \(VM\). Add cloud provider specific mid capability \(AWS,Azure,VMware, Google\) to discover resources from cloud after provisioning Terraform Open-source catalog items. For example: If you are provisioning VM using Terraform Open-Source in Google, you would need mid with Terraform and Google capability. Both capabilities can be set on the same or different mids. Mid with Terraform capability should be able to connect to Terraform Host \(VM\) and that with Google capability must be able to reach google cloud. For more information, see Configure MID Server capabilities.
-   Ensure that all the templates are stored in separate directories and all the template directories are in the same base directory.
-   Ensure that Terraform Connector has access to the Terraform registry \(registry.hashicorp.com\).

Role required: cloud\_admin

## Procedure

1.  If you have deployed the Terraform Open Source on a Linux server, create SSH Private Key Credentials for the server in the ServiceNow AI Platform.

    1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

        The Cloud Admin Portal opens in a new browser tab.

    2.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Credentials**.

    3.  Select **New**.

    4.  Select **SSH Private Key Credentials**.

    5.  On the form, fill in the fields.

        For a description of the form fields, see [Cloud Services Catalog Terraform Connector SSH Private Key Credentials form reference](../reference/ccg-terraform-connector-ssh-private-key-credential-form.md).

    6.  Select the Test Credentials related link.

    7.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Target|IP address of the Terraform server for which you are creating the credential.|
        |MID Server|MID Server that can be used to connect with the Terraform server.|

    8.  Select **OK**.

    9.  Select **Submit**.

2.  If you have deployed the Terraform Open Source on a Windows server, create Windows Credentials for the server in the ServiceNow AI Platform.

    1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

        The Cloud Admin Portal opens in a new browser tab.

    2.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Credentials**.

    3.  Select **New**.

    4.  Select **Windows Credentials**.

    5.  On the form, fill in the fields.

        For a description of the form fields, see [Cloud Services Catalog Terraform Connector Windows Credentials form reference](../reference/ccg-terraform-connector-windows-credentials-form.md).

    6.  Select the Test Credentials related link.

    7.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Target|IP address of the Terraform server for which you are creating the credential.|
        |MID Server|MID Server that can be used to connect with the Terraform server.|

    8.  Select **OK**.

    9.  Select **Submit**.

3.  Create a config provider for Terraform Open Source.

    1.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Config Management**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        For a description of the form fields, see [Cloud Services Catalog Terraform Connector Create Config Provider form reference](../reference/cpg-terraform-connector-config-provider-form.md).

    4.  Select **Submit**.


## What to do next

Discover the Terraform templates from the Terraform Open Source server. For more information, see [Run the IaC Discovery](discover-terraform-config-installables-vcs-workspaces.md).

