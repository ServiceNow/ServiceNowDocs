---
title: Using remote tables and the Salesforce spoke
description: Create Salesforce spoke actions that you can use to test the third-party data integration. Then use these actions in the remote table definition.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Using remote tables and the Salesforce spoke

Create Salesforce spoke actions that you can use to test the third-party data integration. Then use these actions in the remote table definition.

-   **[Using the IntegrationHub Salesforce spoke](../task/config-csm-integration-salesforce.md)**  
Use the Salesforce spoke to integrate a Salesforce account with your ServiceNow instance.
-   **[Create Salesforce spoke actions to retrieve opportunities](csm-integration-salesforce-spoke.md)**  
The Salesforce spoke provides actions to retrieve metadata of the opportunity record and create a new opportunity.
-   **[Remote tables and definition](csm-remote-tables-definition.md)**  
Once you have the spoke custom actions working, you need to create a remote table that describes the schema for the data to be retrieved from the Salesforce Opportunity table.
-   **[Example script that queries the Opportunity table](csm-opportunity-table-script.md)**  
This example script queries the opportunity table using the **Get All Opportunities**, **Get Opportunities for Account Id**, and **Get Opportunity Details** custom actions.
-   **[Connect Customer Account and Salesforce Opportunities using a related list](csm-related-list-opportunity-table.md)**  
Use a related list to link the Customer Account table with Salesforce Account Id, and the Salesforce Opportunity remote table with the same Account Id.

**Parent Topic:**[Reference Salesforce integration using remote tables](data-integration-salesforce-example.md)

