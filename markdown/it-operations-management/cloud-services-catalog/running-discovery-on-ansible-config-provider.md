---
title: Run Discovery on the Ansible config provider
description: Add the Ansible config provider and run Discovery to discover what's in the inventory, the host group, and the available job templates.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating Ansible with Cloud Services Catalog, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Run Discovery on the Ansible config provider

Add the Ansible config provider and run Discovery to discover what's in the inventory, the host group, and the available job templates.

## Before you begin

Do this procedure only if you have Ansible Tower credentials.

Role required: none

## Procedure

1.  Navigate to **Cloud Admin Portal** &gt; **Manage** &gt; **Credentials** &gt; **New** &gt; **Ansible Tower Credentials**.

2.  On the form, fill in the fields as per the information received from the Ansible Tower.

    ![New record for Ansible Tower credentials.](../image/ansible-tower-new.png "Ansible Tower credentials")

3.  Select **Submit**.

4.  Create a config provider by selecting **New**.

    ![Create Config Provider form to use for creating an Ansible Config Provider.](../image/ansible-config-provider.png "Create Config Provider form")

    **Important:**

    Infrastructure as Code \(IaC\) Discovery is supported. You can discover job templates, inventory, and groups.

5.  Run the Discovery to discover all projects and extra variables in an organization.

    ![Ansible Discovery.](../image/ansible-config-provider-discover.png "Ansible Discovery")


## Result

You’re all set to take the next steps to order an Ansible item.

**Parent Topic:**[Integrating Ansible with Cloud Services Catalog](../concept/integrating-ansible-with-cloud-services-catalog.md)

