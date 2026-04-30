---
title: Using a related list to create the connection between the Customer Account and Salesforce Opportunities
description: Use a related list to establish the connection between the Customer Account table that holds the Salesforce Account Id and the Salesforce Opportunity remote table that holds the same Salesforce Account Id.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Using a related list to create the connection between the Customer Account and Salesforce Opportunities

Use a related list to establish the connection between the Customer Account table that holds the Salesforce Account Id and the Salesforce Opportunity remote table that holds the same Salesforce Account Id.

In this example, create a relationship called Opportunities. Choose the Account table in the **Applies to table** field and the remote opportunity table in the **Queries from table** field. For more information, see [Create defined related lists](https://www.servicenow.com/docs/access?context=t_CreateDefinedRelatedLists&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

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

This code checks for the presence of the Salesforce Account Id in the Account table and, if it is missing in the record, sets it to `undefined`. The code also includes a query for the Opportunity table column that holds the Salesforce Account Id for the value of this Id from the Account table. This query is invoked when the user opens the list of opportunities associated with the customer account. To see how it is used in the remote table script, see [Selecting a spoke action and preparing the inputs](csm-opportunity-table-script.md#section_select_spoke_actions).

**Parent Topic:**[Using remote tables and the Salesforce spoke](csm-integration-remote-tables.md)

