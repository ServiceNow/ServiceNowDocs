---
title: Configure Ansible Tower user name and password
description: Configure Ansible Tower credentials to access the Ansible Automation Engine through your instance.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Configure Ansible Tower user name and password

Configure Ansible Tower credentials to access the Ansible Automation Engine through your instance.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **Credentials**, and then click **New**.

2.  Click **Ansible Tower Credentials**.

3.  Fill out the form fields \(see table\):

    To integrate Cloud Provisioning and Governance with the Ansible configuration management account, you must configure the user name and password for the administrator account in Ansible.

    |Field|Description|
    |-----|-----------|
    |Name|Provide a descriptive name.|
    |User name/Password|Enter the authentication credentials for the Ansible Tower user with administrator rights.|

    **Note:** You do not need to configure the other fields.


