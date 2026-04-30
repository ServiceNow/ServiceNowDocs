---
title: Ansible Spoke
description: Integrate your ServiceNow instance with Ansible Tower. Automate Ansible Tower tasks when events occur in ServiceNow.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Ansible Spoke

Integrate your ServiceNow instance with Ansible Tower. Automate Ansible Tower tasks when events occur in ServiceNow.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## IntegrationHub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Ansible spoke v2.2.9 is the latest version.

## Supported version

This spoke was built for Ansible Tower v2, but may be compatible with later versions.

## Spoke requirements

-   Ansible Tower
-   If you are using custom OAuth application:
    -   Ansible Tower administrator credentials to create a custom application
    -   Application information such as Client ID and Client Secret
-   If you are using basic authentication, credentials of the user with System Administrator role to log in to Ansible Tower. To configure the basic authentication, see [Configure a REST message with basic auth](https://www.servicenow.com/docs/access?context=t_ConfigureRESTMsgBasicAuth&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

## Spoke actions

The Ansible spoke provides actions to automate Ansible Tower tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Adhoc Command Management|Look up Status From Ad-Hoc Command by ID|Retrieves the run status from the ad-hoc command.|
|Run An Ad-Hoc Command|Runs an ad-hoc command on the target devices.|
|Credential Management|Look up Credential Details Stream|Retrieves the list of credentials from the Ansible Tower environment.|
|Look up Credentials Details by ID|Retrieves details of the required credential in the Ansible Tower environment.|
|Credential Type Management|Look up Credential Type Details by ID|Retrieves details of the required credential type in the Ansible Tower environment.|
|Look up Credential Type Details Stream|Retrieves the list of credentials in the Ansible Tower environment.|
|Inventory Management|Look up Hosts From Inventory by ID|Lists hosts from the inventory in Ansible Tower environment.|
|Look up Instance Groups From Inventory by ID|Lists instance groups from inventory.|
|Look up Inventory Details by ID|Retrieves details of the required inventory from Ansible Tower.|
|Look up Inventory Details Stream|Retrieves inventory details from Ansible Tower.|
|Inventory Script Management|Look up Inventory Script Details Stream|Retrieves the list of inventory scripts from Ansible Tower.|
|Look up Inventory Scripts Details by ID|Retrieves details of the required inventory script from Ansible Tower.|
|Inventory Source Management|Look up Inventory Source Details by ID|Retrieves details of the required inventory source from Ansible Tower.|
|Look up Inventory Source Details Stream|Retrieves inventory source details stream from Ansible Tower.|
|Job Management|Cancel Job|Cancels the required job in the Ansible Tower environment.|
|Look up Job Details by ID|Retrieves details of the specific job in the Ansible Tower environment.|
|Look up Job Details Stream|Retrieves the list of job details.|
|Look up Jobs Stream|Retrieves the list of jobs.|
|Relaunch Job|Relaunches job in the Ansible Tower environment.|
|Schedule Job|Schedules a job.|
|Metadata Retrieval|Get Credentials|Retrieves credentials in the Ansible Tower environment.|
|Get Inventories|Retrieves inventories in the Ansible Tower environment.|
|Get Projects|Retrieves projects in the Ansible Tower environment.|
|Get Additional Input Fields|Retrieves list of fields that can be used as a dynamic template or dynamic object.|
|Get Entity Data|Retrieves data from the required entity.|
|Organization Management|Look up Organization Details by ID|Retrieves details of the required organization from Ansible Tower.|
|Look up Organization Stream|Retrieves details of organizations from Ansible Tower.|
|Project Management|Look up Project Details by ID|Retrieves details of the required project from Ansible Tower.|
|Look up Projects Stream|Retrieves details of projects from Ansible Tower.|
|Record Management|Create Record|Creates a record in the Ansible Tower environment.|
|Delete Record|Deletes the required record in the Ansible Tower environment.|
|Update Record|Updates details of the required record in the Ansible Tower environment.|
|Role Management|Look up Role Details by ID|Retrieves details of the required role in Ansible Tower environment.|
|Look up Roles Stream|Retrieves details of the roles in the Ansible Tower environment.|
|Look up Teams by Role Stream|Retrieves details of the teams associated with the required role.|
|Look up Users by Role Stream|Retrieves details of the users with the required role.|
|Team Management|Look up Team Details by ID|Retrieves details of the required team.|
|Look up Teams Stream|Retrieves details of the teams in the Ansible Tower environment.|
|Template Management|Create Job Template|Creates a job template.|
|Launch Job Template|Launches a job template.|
|Look up Job Templates Stream|Retrieves the list of job templates.|
|User Management|Associate User to Organization|Associates or disassociates the required user to an organization.|
|Associate User to Team|Associates or disassociates the required user to a team.|
|Create User|Creates a user in the Ansible Tower environment.|
|Delete User|Deletes user in the Ansible Tower environment.|
|Look up User Details by ID|Retrieves details of the required user from Ansible Tower.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Ansible spoke](../task/setup-ansible.md#).

