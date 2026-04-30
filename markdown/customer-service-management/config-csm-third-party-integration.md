---
title: Configure third-party data integration for CSM
description: Configure the required components to enable the third-party data integration feature for Agent Workspace for CSM.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure third-party data integration for CSM

Configure the required components to enable the third-party data integration feature for Agent Workspace for CSM.

## Before you begin

Role required: admin

## Procedure

1.  Identify the third-party application.

    1.  Verify that it has the corresponding IntegrationHub spoke and that it is activated on your instance.

    2.  Follow the setup instructions specific to the spoke.

        For example, for the Salesforce spoke, follow the instructions in the [Set up Salesforce spoke](https://www.servicenow.com/docs/access?context=setup-sf-spk&version=zurich&pubname=zurich-integrate-applications&section=setup-salesforce&ft:locale=en-US) topic.

2.  Identify the spoke action that retrieves the desired third-party data.

    You can find the list of available actions in the spoke documentation. If an action that performs the desired task does not exist, you can create your own action by copying an existing action and modifying it to suit your needs. You can find an example of the custom spoke actions in [Create Salesforce spoke actions to retrieve Opportunities for use in the remote table definition](../concept/csm-integration-salesforce-spoke.md).

    **Note:** Data Stream Actions cannot be used with the remote table.

3.  Create the remote table on your ServiceNow instance to expose the data from the application through the GlideRecord interface.

4.  Create the remote table script definition to map the data from the third-party table to the remote table.

    1.  Configure error messages if the spoke action call results in an error.

        This error is picked up by the form, list, and field elements and is displayed for the end user when an error occurs. These error messages distinguish between cases where the response from the third-party application has no data and an error while fetching data from the third-party application.

    2.  Configure ACLs on the remote table to provide users and roles with read access to the third-party data.

    3.  Configure ACLs to revoke CREATE, WRITE, and DELETE access on the remote table for all users.

5.  Configure the lists, forms, and fields that pull data from the remote table.

    Once the remote table is set up, you can access data using the GlideRecord interface.

    1.  Use Agent Workspace components to embed third-party pages and reports in iframes as popups or related items.

    2.  Configure UI actions on forms to create deep links to the records in the third-party application.

6.  Perform some lightweight data synchronization prior to using the feature.

    For example, pull in account data from a third-party application using an import set. In the example provided, the Account \(customer\_account\) table has an Account Id column, which is populated with the Id of the account in the third-party application instance. This column is used as the foreign key to pull opportunities for the corresponding account on the third-party application instance.


