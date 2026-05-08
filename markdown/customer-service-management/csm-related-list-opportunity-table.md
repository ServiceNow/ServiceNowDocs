---
title: Connect Customer Account and Salesforce Opportunities using a related list
description: Use a related list to link the Customer Account table with Salesforce Account Id, and the Salesforce Opportunity remote table with the same Account Id.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Connect Customer Account and Salesforce Opportunities using a related list

Use a related list to link the Customer Account table with Salesforce Account Id, and the Salesforce Opportunity remote table with the same Account Id.

In this example, create a relationship called Opportunities. Choose the Account table in the **Applies to table** field and the remote opportunity table in the **Queries from table** field. For more information, see Create defined related lists.

![Related list to create Opportunities relationship between the Account table and the Salesforce Opportunity table.](../image/opportunities-relationship-table.jpg)

Add the following code in the **Query with** field:

```
(function refineQuery(current, parent) {

  var sf_account_id = new String(parent.u_salesforce_account_id);

  if (sf_account_id.length == 0)
    sf_account_id = "undefined";

  current.addQuery("u_sf_account_id", sf_account_id);

})(current, parent);

```

This code checks for the presence of the Salesforce Account Id in the Account table and, if it's missing in the record, sets it to `undefined`. The code also includes a query for the Opportunity table column that holds the Salesforce Account Id for the value of this Id from the Account table. This query is invoked when the user opens the list of opportunities associated with the customer account. To see how it is used in the remote table script, see [Selecting a spoke action and preparing the inputs](csm-opportunity-table-script.md#section_select_spoke_actions).

**Parent Topic:**[Using remote tables and the Salesforce spoke](csm-integration-remote-tables.md)

