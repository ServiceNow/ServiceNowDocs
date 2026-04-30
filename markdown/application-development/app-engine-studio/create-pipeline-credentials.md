---
title: Configure environment credentials
description: Configure credentials in your production instance so that the flows used by the App Engine Management Center \(AEMC\) can access different instances.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Pipelines and Deployments configuration tasks, Configure Pipelines and Deployments, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure environment credentials

Configure credentials in your production instance so that the flows used by the App Engine Management Center \(AEMC\) can access different instances.

## Before you begin

You must use a functional user account with admin permissions to create the credentials for use in your pipelines. This user account should have the following characteristics:

-   It should not be associated with a person in your organization.
-   It should not need its password reset regularly.
-   It should be controlled by your administrator.
-   It should have admin privileges on all instances in the pipeline.

You can create a new functional user account specifically for pipeline credentials, or use one that you have previously created with these characteristics. Either way, this user account must be created before you can create the pipeline credentials. For more information about creating this user, see [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Role required: admin

## About this task

Create the pipeline credentials with a functional user account that you created on the Users \[sys\_users\] table. For example, you create a user account called Pipeline Runner and give it admin permissions. This account user name and password are used to set up the credential record.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select **New**.

3.  On the form, change the **Type** to **Credential**.

    Changing the type removes several fields from the form.

4.  On the form, fill in the remaining fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the credential record. For example, Pipeline Credentials.|
    |Application|Scope the record is being created in, which should be **Global**.|
    |ID|Unique ID for the credential record. This field populates automatically based on the name. IDs are written in the form \[scope\_name.credential\_name\], unless the application is in the Global scope, then the ID is just the credential name.|

5.  Select **Submit**.

    The Connections &amp; Credentials Aliases table reopens.

6.  Open the credential that you created to add credential records to it.

7.  On the **Credentials** tab, select **New**.

8.  In the **What kind of Credentials would you like to create?** list, select **Basic Auth Credentials**.

    **Note:** If you want to use OAuth credentials in your pipelines instead, see [Configure OAuth credentials for use in Pipelines and Deployments](configure-oauth-credentials-pipelines-deployments.md).

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the basic auth credential record. For example, Pipeline Credentials.|
    |Order|Order in which the flows you're using read the credential records. For example, if you have multiple credentials for backups, order them like 100, 200, 300, and so on. Flows read from the top of the list.|
    |User name|User name for the functional account. For example, pipeline.runner.|
    |Password|Password for the functional user account.|
    |Active|Option to make the record active.|
    |Credential alias|Alias for the record, repeated from the credential record ID. The alias exists so that only certain users can see what the user name and password are. When flows execute, they use the credential alias so they can install the apps.|

10. Select **Submit**.

11. Repeat this process on each non-production instance in your pipeline.

    For the credential record, use the user name and password that the pipeline should use to access the production instance.


-   **[Configure OAuth credentials for use in Pipelines and Deployments](configure-oauth-credentials-pipelines-deployments.md)**  
Use OAuth credentials in your pipelines to add another level of security to your pipeline. This task helps you create and configure OAuth credentials for use in your pipelines.

**Parent Topic:**[Pipelines and Deployments configuration tasks](../reference/p-and-d-config-tasks.md)

