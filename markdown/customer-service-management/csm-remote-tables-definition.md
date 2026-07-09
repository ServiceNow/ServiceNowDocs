---
title: Remote tables and definition
description: Once you have the spoke custom actions working, you need to create a remote table that describes the schema for the data to be retrieved from the Salesforce Opportunity table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-remote-tables-definition.html
release: australia
topic_type: concept
last_updated: "2026-06-26"
reading_time_minutes: 1
breadcrumb: [Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Remote tables and definition

Once you have the spoke custom actions working, you need to create a remote table that describes the schema for the data to be retrieved from the Salesforce Opportunity table.

Create a remote table with the following information:

-   Label: Salesforce Opportunity
-   Name: u\_st\_salesforce\_opportunity
-   Application: Global
-   Remote table: true

Create the script definition for the remote table \(u\_st\_salesforce\_opportunity\), which does the following:

-   Uses the spoke custom actions to pull data from the Opportunity table in the Salesforce instance.
-   Maps the response from Salesforce into the remote table columns.

**Parent Topic:**[Using remote tables and the Salesforce spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-integration-remote-tables.md)

