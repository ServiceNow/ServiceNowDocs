---
title: Create Salesforce spoke actions to retrieve opportunities for use in the remote table definition
description: The Salesforce spoke provides actions to retrieve metadata of the opportunity record and create a new opportunity.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create Salesforce spoke actions to retrieve opportunities for use in the remote table definition

The Salesforce spoke provides actions to retrieve metadata of the opportunity record and create a new opportunity.

Other than Data Stream Actions, there is no action to get a set of the opportunity records based on a given search criteria. You need to create your own actions to accomplish the stated goal of the reference example. See [Reference Salesforce integration using remote tables](data-integration-salesforce-example.md).

To create a new action, copy an existing action and modify it to suit your needs. For example, you can copy the **Get All Accounts** action and modify it to retrieve opportunity records.

For this example, you will create three new Salesforce spoke actions:

-   Get All Opportunities
-   Get Opportunities for Account Id
-   Get Opportunity Details

Each action includes three steps:

1.  A pre-processing script step that creates a query.
2.  A REST step that executes the query.
3.  A post-processing script step that evaluates the response from the query.

**Note:** You can test all actions from the Flow Designer before you attempt to connect them to the remote table.

-   **[Get All Opportunities custom action](../reference/csm-get-all-opportunities-action.md)**  
The **Get All Opportunities** action retrieves opportunity records from the Salesforce application. This action is invoked when the user views the remote Opportunity table.
-   **[Get Opportunities for Account Id custom action](../reference/csm-account-opportunities-action.md)**  
The **Get Opportunities for Account Id** action retrieves opportunity records for the specific Salesforce account. This action is invoked when the agent views a Salesforce opportunity available for the customer account based on the Salesforce account associated with it.
-   **[Get Opportunities Details custom action](../reference/csm-details-opportunities-action.md)**  
The **Get Opportunities Details** action retrieves a single Opportunity record from the Salesforce application based on the record Id. This action is invoked when the user opens the form for the Opportunity record in the remote table.

**Parent Topic:**[Using remote tables and the Salesforce spoke](csm-integration-remote-tables.md)

