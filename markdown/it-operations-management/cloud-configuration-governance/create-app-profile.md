---
title: Create an application profile
description: An application profile specifies application software to install on newly-provisioned resources. Users can select applications when they request a stack. Use application profiles when you integrate with configuration management \(continuous delivery\) providers such as Ansible playbooks.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resource Profiles, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create an application profile

An application profile specifies application software to install on newly-provisioned resources. Users can select applications when they request a stack. Use application profiles when you integrate with configuration management \(continuous delivery\) providers such as Ansible playbooks.

## Before you begin

-   You must have a cloud account with datacenters. You must run Discovery on the service accounts to populate the datacenters.
-   Role required: sn\_cmp.cloud\_admin

## About this task

This example shows an application profile mapping for a Tomcat server on Ansible.

![An example profile](../image/application-profile-mapping-example.png)

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Profiles**.

2.  In the **Profiles** list, select **Application Profile** and then click **New**.

    ![Application profile](../image/application-profile.png)

3.  Enter a unique and descriptive **Name** and **Description** for the profile and then click **Submit**.

    The profile is created.

4.  Map the profile to a template.

    1.  In the list, click the profile that you created.

    2.  In the **Application Profile Mappings** related list, click **New**, fill in the form, and then click **Submit**.

<table id="table_ztx_4f3_jfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workload Config Provider

</td><td>

Select a configuration management provider to associate with the profile.

</td></tr><tr><td>

Application Template \[sn\_cmp\_application\_template\]

</td><td>

Select a template that the profile should be mapped to. If you ran Discovery on the Configuration Provider, the templates are already populated.

 The resource type associated with an application profile is `sn_cmp_application_template`.

 Click the reference icon \(![Reference icon](../../../common/image/icon-reference.png)\) to view the details of the template.

 To create a new template:

1.  Click the reference icon \(![Reference icon](../../../common/image/icon-reference.png)\) to open the Application Templates list.
2.  Click **New** and then fill in the Application Template form:
 -   **Name**: Enter a descriptive name for the template.
-   **Template ID**: Enter an ID to use for the template.
-   **Config runlist provider**: Click the list, select a table from the **Table name** list, and then select records for the table from the **Document** list.
-   **Config runlist**: Specify a configuration runlist.
-   **Provider instance**: Select a provider instance.


</td></tr></tbody>
</table>5.  Create as many mappings as needed.


**Related topics**  


[Discover all datacenters in a service account on-demand](../../cloud-management-v2-setup/task/disco-datacntrs-in-srv-acct-1.md)

