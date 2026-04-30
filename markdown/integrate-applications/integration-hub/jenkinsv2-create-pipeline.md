---
title: Create a pipeline project in Jenkins
description: Create a pipeline projects in Jenkins to add the endpoint URL in Jenkinsfile that is generated in your ServiceNow instance and enable webhooks to connect with your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-28"
reading_time_minutes: 1
breadcrumb: [Set up triggers for the Jenkins spoke, Jenkins v2 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a pipeline project in Jenkins

Create a pipeline projects in Jenkins to add the endpoint URL in `Jenkinsfile` that is generated in your ServiceNow instance and enable webhooks to connect with your ServiceNow instance.

## Before you begin

-   Ensure that you install Jenkin in the local environment.
-   Ensure that Maven and GitHub are installed in the Jenkins account.
-   Ensure that these plugins are installed in the Jenkins account.
    -   Pipeline
    -   Git plugin
    -   Git client
    -   Http request
    -   Credentials
    -   Warnings
    -   Coverage
-   In GitHub, generate a classic personal access token and copy the value.

    Ensure that you select the scopes for the personal access token.

    -   repo
        -   repo:status
        -   repo\_deployment
        -   public\_repo
        -   repo:invite
        -   security\_events
    -   write:packages
        -   read:packages
    For more information about creating a classic personal access token, see [Creating a personal access token \(classic\)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic) in [GitHub Docs](https://docs.github.com/en).

    For the list of supported events, see the [Spoke triggers](../concept/jenkins-spoke.md#section_ccf_fn2_t3c) section.

-   Role required: admin

## Procedure

1.  From the Jenkins Dashboard, select **+ New Item**.

2.  On the form, enter a name to identify the pipeline and select **Pipeline**.

3.  Click **OK**.

    The pipeline is created and its configuration options are displayed.

4.  Under **Configure**, click **Pipeline**.

5.  On the form, fill these values.

<table id="table_yn5_yld_t3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Definition

</td><td>

Select **Pipeline script from SCM**.

</td></tr><tr><td>

SCM

</td><td>

Select **Git**.

</td></tr><tr><td>

Repository URL

</td><td>

Provide GitHub repository URL.

</td></tr><tr><td>

Credentials

</td><td>

Create the GitHub credential record and select it.1.  Click **+Add**.
2.  Select **Username with password** and click **Next**.
3.  For **Username**, enter the GitHub username.
4.  For **Password**, paste the personal access token that is generated in GitHub.
5.  For **ID**, provide a unique ID to identify the credentials.
6.  For **Description**, enter a description for the credentials.
7.  Click **Create**.
8.  Select this record for **Credentials**.


</td></tr><tr><td>

Branch Specifier \(blank for 'any'\)

</td><td>

Specify the required branch.

</td></tr><tr><td>

Script path

</td><td>

Relative location within the checkout of your Pipeline script.**Important:** In `Jenkinsfile`, paste the endpoint URL that was generated after you configured triggers in your ServiceNow instance. For more information, see [Configure triggers in ServiceNow instance](jenkinsv2-conf-triggers-s.md).

![](../image/jenkinsv2-file.jpg)

</td></tr></tbody>
</table>6.  Click **Save**.


