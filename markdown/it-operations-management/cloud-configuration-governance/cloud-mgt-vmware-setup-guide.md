---
title: Day 1 setup guide for VMware on Cloud Provisioning and Governance
description: To set up Cloud Provisioning and Governance for the very first time, you perform the procedures in this "Day 1" setup guide. Be sure to perform the procedures in order. After you have performed Day 1 setup, you can perform optional Day 2 setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Day 1 setup guide for VMware on Cloud Provisioning and Governance

To set up Cloud Provisioning and Governance for the very first time, you perform the procedures in this "Day 1" setup guide. Be sure to perform the procedures in order. After you have performed Day 1 setup, you can perform optional Day 2 setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.

## Request the Cloud Provisioning and Governance application

The Cloud Provisioning and Governance application is available as a separate subscription and requires the Cloud Provisioning and Governance plugin \(com.snc.cloud.mgmt\). See [Request the Cloud Provisioning and Governance application](../task/request-plugin-cloud-mgt-1.md).

## Roles required to set up Cloud Provisioning and Governance

-   Operations in the VMware Console require the VMware administrator role.
-   Operations in Cloud Provisioning and Governance require the sn\_cmp.cloud\_admin role.

## About terms that Cloud Management uses

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings.

## Quick overview of the setup process

Your setup process includes these tasks:

-   If needed: Request the Cloud Provisioning and Governance application.
-   Assign appropriate roles to cloud users.
-   Set up the MID Servers that will handle secure communications with the provider API endpoints.
-   On the provider portal, collect your account settings and the credentials that the Discovery process will use \(through a MID Server\) to programatically access your provider accounts. Securely associate the account settings and credentials with a service account in Cloud Provisioning and Governance.
-   Set up a cloud account to represent your entire managed cloud infrastructure and set up a service account that works with one of your provider accounts. You specify which datacenters in the service account should be included in the cloud account. \(Later, on "Day 2", you can set up additional cloud accounts and service accounts from the same or other providers.\)
-   Cloud Provisioning uses CMDB data to help users request and manage cloud resources and to help you manage your cloud infrastructure. To populate the CMDB with resource data for all datacenters, you manually run the Discovery process on each datacenter in the service account. Then, to ensure that the data continues to be updated, you configure Discovery to run on a regular schedule. Your cloud account might look like this:

    ![Structure of a cloud account on Day 1](../image/cloud-acct-day-1.png "Structure of a cloud account on Day 1")

-   Providers offer services that can auto-update the CMDB whenever a create/modify/terminate life-cycle change or configuration update occurs to a resource. You can configure the service to integrate directly with Cloud Provisioning and Governance.

## What you will do to integrate Cloud Provisioning and Governance with your VMware cloud accounts

Detailed instructions for each procedure follow this overview.

-   **1. Assign roles to VMware users of Cloud Provisioning and Governance**

    You assign Cloud Provisioning and Governance roles to user groups and to individual users based on user activities and responsibilities.

-   **2. Create the credential and service account that will access your VMware data**

    To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery, you first create an account in the VMware Console. You then securely store the credentials in a service account in your instance. A service account is a secure record on your instance that stores the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter.

-   **3. Discover all datacenters in a service account on-demand**

    Discovery uses the information in the service account to identify all logical datacenters associated with the provider account.

-   **4. Set up cloud accounts for VMware**

    A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

-   **5. Set capacity limits on user requests for resources**

    Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.


-   **vSphere**

    -   Enterprise or Enterprise Plus Edition 5.5 or newer.
    -   Enable the vSphere environment for Distributed Resource Scheduling \(DRS\).
    -   Place datastores under Storage DRS.
    When provisioning Windows virtual machines, read and modify the named customization specifications.

-   **ESXi hosts**

    If the IP address of a virtual machine is set manually using a script or post-init scripts run on the VM, then you must allow HTTPS traffic between the MID Server and the ESXi host for the VM.

    Enable NTP time sync. Enable the NTP client for the hypervisor on the vSphere web client. See the [vSphere documentation](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vcenterhost.doc/GUID-8756D419-A878-4AE0-9183-C6D5A91A8FB1.html) for more information.

-   **vCenter server requirements**

    vCenter 5.5 or 6.0 Standard or Foundation edition.

-   **vCenter access requirements**

    Minimum permissions for the user that connects to vSphere through the instance:

    -   Datastore: All
    -   Datastore Cluster: All
    -   Folder: Create, Delete
    -   Global: Cancel task, License
    -   Host &gt; Local operations: Create/Delete/Reconfigure virtual machines
    -   Profile-driven storage: All
    -   Network: Assign network
    -   Resource: Apply recommendation; Create/Modify/Assign/Remove virtual machines.
    -   Virtual machines: All
-   **vCenter credentials**
    -   Username
    -   Password
    -   URL or IP address of the vCenter server that the instance access through the MID Server.
    -   vCenter instance UUID. See [Create the credential and service account that will access your VMware data](../task/vmware-create-creds-cloud-mgt-1.md) for instructions on how to obtain the UUID.

## Next steps

When you have finished all Day-1 and Day-2 procedures in this setup guide, see the [Cloud Provisioning and Governance administration guide](../../cloud-management-v2/concept/cloud-configuration.md) for information on using the Cloud Provisioning and Governance application in your organization.

