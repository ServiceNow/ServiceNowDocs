---
title: Configure your pipeline environments
description: Set up your app development production and non-production environments \(for example, development, test, and/or staging\) by adding the URLs and credentials used to access each instance.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration tasks, Configure Pipelines and Deployments, Configure, App Engine Management Center, Governing app development, Building applications]
---

# Configure your pipeline environments

Set up your app development production and non-production environments \(for example, development, test, and/or staging\) by adding the URLs and credentials used to access each instance.

## Before you begin

Role required: admin

**Note:** Only users with the System Administrator \(admin\) role can define instance credentials for environments. Users with the App Engine Administrator \[sn\_app\_eng\_notify.app\_engine\_admin\] role can view environment records; however, the **Instance credential** field is not visible.

## Procedure

1.  In your production instance, navigate to **All** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Environments**.

2.  Select **New**.

    ![Creating a new environment](../image/new-environment-purple.png "Environment - new record")

3.  On the form, fill in the fields.

<table id="environment-form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the environment. Enter a name that distinguishes the instance as a development, test, or production environment. For example, if you're defining a development environment, you could include `Dev` in the name.

</td></tr><tr><td>

Instance Type

</td><td>

The type of environment you are defining:-   Sandbox
-   Development
-   Testing
-   Staging
-   Production


</td></tr><tr><td>

Instance URL

</td><td>

Web address of your ServiceNow instance.

</td></tr><tr><td>

Instance ID

</td><td>

The instance\_id sys\_property for the instance.**Note:** The Instance ID is automatically generated when you complete all of the other fields and select **Validate**.

</td></tr><tr><td>

Application

</td><td>

Application scope of the environment.

</td></tr><tr><td>

Instance credential

</td><td>

Authentication data related to the instance that you're configuring as an environment.**Note:** If you are using OAuth 2.0 credentials, select the appropriate credential for the instance record. For example, on your development instance record, select the OAuth Dev credential, and for your test instance record, select the OAuth Test credential.

</td></tr><tr><td>

Is Controller?

</td><td>

Identifies if this instance is a controller. This should be selected for the production environment record where you plan to manage deployment requests. For more information, see [Configure your controller instance](config-controller-instance.md).

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Repeat the previous steps as you define each remaining environment in your pipeline.

    For example, if you defined a production environment, repeat the procedure again to define a development environment. Then repeat the procedure once more to define a test environment.


