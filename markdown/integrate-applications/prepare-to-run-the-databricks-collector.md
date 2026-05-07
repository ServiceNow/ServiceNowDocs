---
title: Prepare to run the Databricks collector
description: Complete authentication and permission configuration tasks before running the Databricks metadata collector.Generate a personal access token or service principal secret to authenticate the Databricks connection.Grant necessary permissions for Unity Catalog, Jobs, and system tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Databricks metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Databricks collector

Complete authentication and permission configuration tasks before running the Databricks metadata collector.

## Before you begin

Role required: admin

## Procedure

1.  Generate Databricks credentials.

    For detailed instructions, see [Generate credentials](prepare-to-run-the-databricks-collector.md#).

2.  Configure permissions.

    For detailed instructions, see [Configure permissions](prepare-to-run-the-databricks-collector.md#).


**Parent Topic:**[Databricks metadata collector](../concept/databricks-metadata-collector.md)

## Generate credentials

Generate a personal access token or service principal secret to authenticate the Databricks connection.

### Before you begin

Role required: account admin

**Important:** You must be an Account Admin in Databricks to create and manage service principals.

### About this task

Configure these credentials to enable authentication for the Databricks collector. You can use either a Personal Access Token \(PAT\) or an OAuth service principal.

### Procedure

1.  Generate the required credentials based on your authentication method.

    -   To generate a Personal Access Token \(PAT\):

        1.  In the Databricks workspace, select your username in the top bar and select **Settings**.
        2.  Select **Developer**.
        3.  Next to **Access tokens**, select **Manage**.
        4.  Select **Generate New Token**.
        5.  Enter a comment to identify the token.
        6.  Change the **Lifetime \(days\)** setting if required.

            **Note:** To create a token with the maximum lifetime of 730 days, leave the lifetime field empty.

        7.  Select **Generate**.
        8.  Copy the displayed token and select **Done**. Save this token securely for future use.
        9.  Alternatively, use the [token API](https://docs.databricks.com/api/workspace/tokens#create) to generate a PAT.
    -   To generate a Service Principal secret:

        1.  In the Databricks workspace, select your username in the top bar and select **Settings**.
        2.  Navigate to the **Identity and access** tab.
        3.  Next to **Service principals**, select **Manage**.
        4.  Select **Add service principal**.
        5.  Select **Add new**, provide a name for the service principal, and select **Add**.
        6.  Select the newly created service principal and navigate to the **Secrets** tab.
        7.  Select **Generate secret**.
        8.  Enter the lifetime for the secret and select **Generate**.
        9.  Copy the **Client ID** and **Client secret** from the dialog box.

## Configure permissions

Grant necessary permissions for Unity Catalog, Jobs, and system tables.

### Before you begin

Role required: admin

### About this task

In Unity Catalog, data is secure by default. Grant permissions to the user running the collector to harvest resources. Securable objects in Unity Catalog are hierarchical, and privileges are inherited downward.

### Procedure

1.  Grant Unity Catalog permissions.

    The user requires **USE CATALOG**, **USE SCHEMA**, and **SELECT** permissions on the catalog to access data.

    **Note:** A user with **USE CATALOG** and **BROWSE** permissions can access data but can't retrieve column statistics, system functions, or certain additional table metadata. See the [Databricks documentation](https://docs.databricks.com/data-governance/unity-catalog/manage-privileges/index.html) for details about these permissions.

    1.  Select the catalog to which you want to grant access.

    2.  Select the **Permissions** tab and select **Grant**.

    3.  Select the user and the appropriate permissions, then select **Grant**.

2.  Grant compute resource permissions.

    The user must have **Can Use** permission on the existing cluster or SQL warehouse, or can create their own compute resources.

    1.  Select the **More options** icon on the resource and select **Permissions**.

    2.  Add the user and select the **Can Use** permission.

3.  Grant permissions for Jobs.

    To harvest Jobs, the user running the collector must have **Can View** permissions on the target Jobs. For details about setting Job permissions, see the [Databricks documentation](https://docs.databricks.com/security/auth-authz/access-control/jobs-acl.html).

4.  Enable lineage harvesting from system tables.

    Work with your Databricks admin to enable the `system.access` schema.

    1.  Make a PUT request to the API to enable the schema.

        ```
        curl -X PUT -H "Authorization: Bearer <PAT_Token>" https://<databricks-host>/api/2.1/unity-catalog/metastores/<metastore_id>/systemschemas/access
        ```

        To find the `metastore_id`, navigate to **Catalog** &gt; **Settings** and view the Metastore info section.

    2.  Grant the following permissions to the user running the collector.

        -   **USE SCHEMA** on `system.access`
        -   **SELECT** on `system.access.table_lineage`
        -   **SELECT** on `system.access.column_lineage`
        Example SQL commands:

        ```
        GRANT USE SCHEMA ON SCHEMA system.access to `<userid>`;
                   GRANT SELECT on TABLE system.access.table_lineage to `<userid>`;
                   GRANT SELECT on TABLE system.access.column_lineage to `<userid>`;
        ```


