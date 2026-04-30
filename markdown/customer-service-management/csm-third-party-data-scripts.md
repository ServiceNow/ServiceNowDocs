---
title: Third-party data integration sample script
description: The remote table script can be designed to pull records from a third-party application. This script is called when a query to access data in the remote table is made.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Third-party data integration sample script

The remote table script can be designed to pull records from a third-party application. This script is called when a query to access data in the remote table is made.

In order to use a remote table with IntegrationHub, you need to identify the IntegrationHub spoke that works with the third-party application. The spoke consists of the Flow Designer actions that were created to bring various subsets of the data from that application.

For example, if you need to bring account information from the Salesforce application, you would use the Salesforce spoke and the **Get All Accounts** action. See below for an example of the remote table script that accesses this action.

```
(function executeQuery(v_table, v_query) {
  try {
    // prepare inputs for the spoke actions 
    // Get All Accounts action does not have any inputs).
    var inputs = {};

    // call spoke action
    var outputs = sn_fd.FlowAPI.executeAction(
                                "sn_salesforce_spok.get_all_accounts", inputs);

    // check if Action was completed successfully
    if (outputs.status != "Success") {
      throw new Error(outputs.errorMessage);
    }

    // extract payload from the action outputs
    var accounts = outputs.accounts.data;

    // map action output data to the remote table columns and Sys Id
    for (var i = 0; i < accounts.length; i++) {
      v_table.addRow({
        "u_sf_account_id": accounts[i].name,
        "u_sf_account_name": accounts[i].label,
        // assign remote table Sys Id to the primary key of the third-party
        // record
        "sys_id": accounts[i].name,
      });
    }

  // process errors 
  } catch (error) {
     gs.addErrorMessage("Error trying to retrieve  Salesforce Accounts." +
                        "Please contact System Administrator.");
     gs.addErrorMessage("System Error: " + error.message);
  }

})(v_table, v_query);

```

**Note:** Not all IntegrationHub actions can be invoked from the remote table scripts. Specifically, Data Stream Actions cannot be called from the scripts. If the action you would like to use is a Data Stream Action, you might need to create your own action based on the REST step. An easy way to create an action is to copy an existing action and then modify it to accomplish your goal. You can find an example of custom spoke actions in this topic: [Create Salesforce spoke actions to retrieve Opportunities for use in the remote table definition](../concept/csm-integration-salesforce-spoke.md).

