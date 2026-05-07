---
title: Prepare to run the Tableau collector
description: Set up API access, authentication, and permissions before running the collector.Enable the Metadata API on Tableau Server to allow metadata collection.Create a Tableau user with admin permissions and generate a Personal Access Token.Set up a Connected App in Tableau for JWT authenticationCreate a YAML file to map database hostname aliases to canonical names.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Tableau metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Tableau collector

Set up API access, authentication, and permissions before running the collector.

## Before you begin

Role required: admin

## About this task

The collector uses the Tableau Metadata API to harvest metadata. You must enable the API \(for Tableau Server\), configure user permissions, and choose an authentication method. Optionally, configure hostname mapping for database aliases.

## Procedure

1.  Enable the Metadata API on Tableau Server.

    See [Enable Tableau Metadata API](prepare-to-run-tableau-collector.md#).

    **Note:** The Metadata API is enabled by default for Tableau Cloud. This step applies only to Tableau Server.

2.  Configure user permissions and create a Personal Access Token.

    See [Configure Tableau user permissions](prepare-to-run-tableau-collector.md#).

3.  Configure JWT authentication using a Connected App.

    See [Configure Tableau JWT authentication](prepare-to-run-tableau-collector.md#).

4.  Configure hostname mapping for database aliases.

    See [Set up a YAML file for hostnames mapping](prepare-to-run-tableau-collector.md#).


**Parent Topic:**[Tableau metadata collector](../concept/tableau-metadata-collector.md)

## Enable Tableau Metadata API

Enable the Metadata API on Tableau Server to allow metadata collection.

### Before you begin

Role required: admin

You must have:

-   Tableau Server 2019.3 or later
-   Account with Server Admin role in Tableau Server
-   REST API enabled \(not disabled\)

**Note:** The Metadata API is enabled by default for Tableau Cloud. This procedure applies only to Tableau Server.

### About this task

The Tableau collector uses the Metadata API to harvest metadata from Tableau Server. By default, this API is disabled on Tableau Server and must be enabled using the Tableau Services Manager \(TSM\) command line interface.

### Procedure

1.  Open a command prompt as an admin on the initial node where Tableau Services Manager \(TSM\) is installed in the cluster.

2.  Run the following command to enable the Metadata API.

    ```
    tsm maintenance metadata-services enable
    ```

3.  Enable derived permissions if you do not have the Data Management license.

    Derived permissions allow you to see related external assets. For detailed instructions, see the [Tableau documentation](https://help.tableau.com/current/server/en-us/dm_perms_assets.htm#derived).


### Result

The Metadata API is now enabled on Tableau Server and ready for metadata collection.

## Configure Tableau user permissions

Create a Tableau user with admin permissions and generate a Personal Access Token.

### Before you begin

Role required: admin

You must have permissions to create users and assign roles in Tableau Server or Tableau Cloud.

### About this task

The Tableau collector requires a user account with administrative privileges to access and harvest metadata. Create a dedicated user account and generate a Personal Access Token \(PAT\) for authentication.

### Procedure

1.  Create a new user in Tableau with admin permissions.

    -   For Tableau Server, assign the Server Admin role. See the [Tableau documentation](https://help.tableau.com/current/server/en-us/users_site_roles.htm) for details
    -   For Tableau Cloud, assign the Site Admin role. See the [Tableau documentation](https://help.tableau.com/current/online/en-us/permission_license_siterole.htm) for details
2.  Create a Personal Access Token \(PAT\) for the user.

    For detailed instructions on creating a PAT, see the [Tableau documentation](https://help.tableau.com/current/server/en-us/security_personal_access_tokens.htm).

3.  Save the Personal Access Token securely.

    You will need this token when configuring the Tableau metadata collector.


## Configure Tableau JWT authentication

Set up a Connected App in Tableau for JWT authentication

### Before you begin

Role required: admin

You must have permissions to create and manage Connected Apps in Tableau.

**Important:** The APIs to fetch workbook revisions and datasource revisions are not supported by JWT authentication.

### About this task

Configure a Connected App to use JWT \(JSON Web Token\) authentication with the Tableau collector. The Connected App provides the client ID, secret ID, and secret value needed to generate JWT tokens.

### Procedure

1.  Log in to the Tableau instance.

2.  Navigate to **Settings**.

3.  Create a Connected App.

    For detailed instructions, see the [Tableau documentation](https://help.tableau.com/current/server/en-us/connected_apps.htm).

4.  Enable the Connected App.

5.  Generate a secret in the Connected App.

6.  Save the Connected App credentials.

    Record the following values for use when configuring the Tableau collector:

    -   Client ID
    -   Secret ID
    -   Secret value
    These credentials are used to generate JWT tokens for authentication.


## Set up a YAML file for hostnames mapping

Create a YAML file to map database hostname aliases to canonical names.

### Before you begin

Role required: admin

### About this task

Use a hostname mapping file when you have multiple server names \(aliases\) for the same database instance and the database collector uses a different alias than the one defined in the Tableau connection. This optional configuration maps database hostnames to canonical names for consistent IRI coining.

### Procedure

1.  Create a YAML file named hostnames.yml.

2.  Add hostname mapping entries to the file.

    Use the following format:

    ```
    mappingValues:
                            - originalHostname: "<Original_HostName>"
                            canonicalHostname: "<canonical_HostName>"
    ```

    Example: If your Tableau source uses db-server-01.company.local but you want to use db.company.com as the hostname during database object IRI coining:

    ```
    mappingValues:
                            - originalHostname: "db-server-01.company.local"
                            canonicalHostname: "db.company.com"
    ```

    **Note:** You can use environment variables in the file for sensitive information such as passwords.

3.  Save the hostnames.yml file.

4.  Pass the YAML file to the collector using the Hostnames mapping file option.

    Use the Hostnames mapping file option when running the collector to upload the hostnames.yml file.


### Result

The collector will use the canonical hostname in place of the original hostname when coining database object IRIs.

