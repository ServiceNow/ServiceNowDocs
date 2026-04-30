---
title: Add credentials to an image template
description: When you add credentials to an image template, the credentials are inherited by all VMs that are provisioned using the template.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add credentials to an image template

When you add credentials to an image template, the credentials are inherited by all VMs that are provisioned using the template.

## Before you begin

-   Role required: cloud\_admin
-   A set of [basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) must exist.

## Procedure

1.  Perform one of the following actions:

    -   If an OS profile is mapped to the virtual machine template:
        1.  Open the OS profile \(**Manage** &gt; **Resource Profiles**\).
        2.  In the OS Profile Mappings related list, click the **Name** of the template in the **Image Template** column.
    -   For VMware templates, navigate to **All** &gt; **Configuration** &gt; **VMware** &gt; **Virtual Machine Templates**.
2.  On the Image form, select the basic authentication **Credentials**.

3.  Click **Update**.


