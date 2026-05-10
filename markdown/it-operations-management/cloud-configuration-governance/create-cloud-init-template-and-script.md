---
title: Create cloud initialization script templates and a script
description: Create cloud initialization templates and a script to use during VM provisioning.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Cloud scripts and cloud script templates, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create cloud initialization script templates and a script

Create cloud initialization templates and a script to use during VM provisioning.

## Before you begin

Role required: cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Scripts** &gt; **Cloud Script Templates**.

2.  Click **New**, enter the name and content of the script, and then click **Submit**.

    Create as many script templates as needed.

3.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud Scripts**.

4.  Click **New**.

5.  Enter a descriptive name and create script that uses the template name in the following line of code \(scriptName is the name of the template\):

    ```
    templateResolver.getTemplate(scriptName);
    ```

    **Note:** For more information, see [Cloud scripts and cloud script templates](../concept/cloud-scripts-and-templates.md).

6.  Click **Submit**.


## What to do next

To run a script at the time a virtual resource is provisioned, map the script to an OS profile. To run a post-provisioning script, create a blueprint and specify the script in the Execute Script operation. See [Example: Post-provision cloud script](create-cloud-init-script-example.md) for an example.

