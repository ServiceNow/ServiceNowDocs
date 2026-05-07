---
title: Prepare to run the dbt Cloud collector
description: Configure dbt Cloud and create authentication tokens before running the collector.Obtain required IDs from dbt Cloud URLs for collector configuration.Create a personal access token for metadata harvesting.Create a service account token with the required permissions for metadata harvesting.Enable documentation generation in dbt Cloud job settings. This setting must be enabled to successfully harvest dbt resources.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [dbt Cloud metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the dbt Cloud collector

Configure dbt Cloud and create authentication tokens before running the collector.

## Before you begin

Role required: none

## About this task

Complete these preparation tasks before running the dbt Cloud collector.

## Procedure

1.  Obtain the required IDs from dbt Cloud.

    See [Obtain account, project, job, and run IDs](prepare-to-run-dbt-cloud-collector.md#).

2.  Create an API token based on your dbt Cloud plan.

    -   Enterprise plan: See [Create a service token](prepare-to-run-dbt-cloud-collector.md#)
    -   Team plan: See [Create a user token](prepare-to-run-dbt-cloud-collector.md#)
3.  Enable documentation generation in job settings.

    See [Update job execution settings](prepare-to-run-dbt-cloud-collector.md#).


**Parent Topic:**[dbt Cloud metadata collector](../concept/dbt-cloud-metadata-collector.md)

## Obtain account, project, job, and run IDs

Obtain required IDs from dbt Cloud URLs for collector configuration.

### Before you begin

Role required: none

### About this task

You’ll use this information when configuring the collector for metadata harvesting.

### Procedure

1.  Obtain the Account ID and Project ID.

    1.  Navigate to **Deploy** &gt; **Jobs**.

    2.  Copy the Account ID and Project ID from the URL.

        URL format:

        ```
        https://cloud.getdbt.com/deploy/<accountID>/projects/<projectID>/jobs
        ```

2.  Obtain the Environment ID and Environment Name.

    1.  Navigate to **Deploy** &gt; **Environments**.

    2.  Select the environment that you want to run the collector against.

    3.  Copy the Environment ID from the URL or note the Environment Name from the page title.

        URL format:

        ```
        https://cloud.getdbt.com/deploy/<accountID>/projects/<projectID>/environments/<environmentID>
        ```

3.  Obtain the Job ID.

    1.  From the Jobs section, select the job associated with your environment.

    2.  Copy the Job ID from the URL or note the Job name from the page title.

        URL format:

        ```
        https://cloud.getdbt.com/deploy/<accountID>/projects/<projectID>/jobs/<jobID>
        ```

4.  : Obtain a specific Job Run ID.

    By default, the collector harvests from the most recent successful job run. To harvest from a specific run, complete these steps.

    1.  From the Job page, select a specific job run.

    2.  Copy the Job Run ID from the URL.

        URL format:

        ```
        https://cloud.getdbt.com/deploy/<accountID>/projects/<projectID>/runs/<jobRunID>
        ```


## Create a user token

Create a personal access token for metadata harvesting.

### Before you begin

Role required: admin

Plan required: Team.

### About this task

The Team plan doesn’t support service account tokens. You must create a personal access token using a dedicated user account.

### Procedure

1.  Create a dedicated user account for the collector.

2.  Assign the Admin role to the user account.

3.  Log in as the dedicated user.

4.  Navigate to **Profile** &gt; **Access Tokens**.

5.  Generate a Personal Access Token.

6.  Copy the token value.

    You’ll use this token value for the dbt Cloud API key when configuring the collector.


### What to do next

See the [dbt Cloud user tokens documentation](https://docs.getdbt.com/docs/dbt-cloud-apis/user-tokens) for additional information.

## Create a service token

Create a service account token with the required permissions for metadata harvesting.

### Before you begin

Role required: admin

Plan required: Enterprise.

### About this task

For Enterprise accounts, service account tokens are commonly used for production systems.

### Procedure

1.  Create a service account token.

    Follow the steps in the [dbt Cloud service tokens documentation](https://docs.getdbt.com/docs/dbt-cloud-apis/service-tokens).

2.  Assign roles to the service account token.

    -   Account Viewer: Assigned at the account level
    -   Job Viewer: Assigned at the project level for each project to collect metadata from
3.  Copy the token value.

    You’ll use this token value for the dbt Cloud API key when configuring the collector.


## Update job execution settings

Enable documentation generation in dbt Cloud job settings. This setting must be enabled to successfully harvest dbt resources.

### Before you begin

Role required: admin

This setting must be enabled to successfully harvest dbt resources.

### Procedure

1.  Navigate to **Deploy** &gt; **Jobs**.

2.  From the **Environment** list, select the environment you want to run the collector against.

3.  Select the job associated with your environment.

4.  Select **Settings**.

5.  Under **Execution Settings**, select **Generate docs on run**.


