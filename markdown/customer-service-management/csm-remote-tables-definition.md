---
title: Remote tables and definition
description: Once you have the spoke custom actions working, you need to create a remote table that describes the schema for the data to be retrieved from the Salesforce Opportunity table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Remote tables and definition

Once you have the spoke custom actions working, you need to create a remote table that describes the schema for the data to be retrieved from the Salesforce Opportunity table.

Create a remote table as shown in the following example.

![Salesforce Opportunity remote table listing data in columns.](../image/remote-table-salesforce-opportunity.jpg)

Create the script definition for the remote table \(u\_st\_salesforce\_opportunity\), which does the following:

-   Uses the spoke custom actions to pull data from the Opportunity table in the Salesforce instance.
-   Maps the response from Salesforce into the remote table columns.

**Parent Topic:**[Using remote tables and the Salesforce spoke](csm-integration-remote-tables.md)

