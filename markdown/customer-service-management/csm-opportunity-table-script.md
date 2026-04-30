---
title: Example script that queries the Opportunity table
description: This example script queries the opportunity table using the Get All Opportunities, Get Opportunities for Account Id, and Get Opportunity Details custom actions.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Example script that queries the Opportunity table

This example script queries the opportunity table using the **Get All Opportunities**, **Get Opportunities for Account Id**, and **Get Opportunity Details** custom actions.

The example script consists of three distinct parts:

1.  The first part selects the correct custom action and prepares inputs for it.
2.  The second part makes a call to the action.
3.  The third part processes the outputs of the action.

## Selecting a spoke action and preparing the inputs

In this section of the script, select one of the three custom actions that you prepared to get opportunities from the Salesforce application:

-   **Get All Opportunities**
-   **Get Opportunities for Account Id**
-   **Get Opportunity Details**

You can decide which action to call based on the parameters included in `v_query` function argument.

```
/****** Choose action and prepare action inputs *****/
var action = null;
var inputs = {};

// look up opportunity by salesforce record id
if (v_query.isGet()) {

  action = "get_opportunity_details";
  inputs.salesforce_opportunity_record_id = v_query.getSysId();
      

// look up opportunities by salesforce account id
} else if (v_query.getParameter("u_sf_account_id")) {

    if (v_query.getParameter("u_sf_account_id") == "undefined") {
      gs.addInfoMessage(“Opportunities cannot be retrieved because “ +
                        “this “Account does not have associated “    +
                        “Salesforce Account. Please contact System “ +
                         “Administrator.");
      return;

    } else {
      action = "get_opportunities_for_account_id";
      inputs.salesforce_account_id = v_query.getParameter("u_sf_account_id");
    }

// look up all opportunities
} else {
  action = "get_all_opportunities";
}

```

Note that this script configures an information message if the Salesforce account is undefined when it is required by the action. The undefined value comes from the relationship that is described in [Using a related list to create the connection between the Customer Account and the Salesforce Opportunities](csm-related-list-opportunity-table.md).

When the Salesforce account is undefined, there is nothing to query for in this case and the function returns without calling the spoke action.

## Calling the spoke action

In this section of the script, call the action using the names of the Salesforce spoke and the selected action and store the outputs of the call.

```
/***** Call action *****/
var outputs =
        sn_fd.FlowAPI.executeAction("sn_salesforce_spok." + action, inputs);

```

## Processing the action output

In this section of the script, process the outputs starting with the check for errors.

```
/***** Process action outputs *****/
if (outputs.status != "Success") {
throw new Error(outputs.error_message);
}

```

If the query does not return any errors, the script needs to process the returned records and add them as rows into the remote table. Map the Salesforce Opportunity fields into the remote table columns.

```
var opportunities = outputs.opportunities.data;

 for (var i = 0; i < opportunities.length; i++) {
  var opportunity = opportunities[i];
  v_table.addRow({
    "u_sf_amount": opportunity.Amount,
    "u_sf_close_date": opportunity.CloseDate,
    "u_sf_name": opportunity.Name,
    "u_sf_probability": opportunity.Probability + "%",
    "u_sf_account_id": opportunity.AccountId,
    "u_sf_stage": opportunity.StageName,
    “u_sf_type": opportunity.Type,
    "sys_id": opportunity.Id,
  });
}

```

Note that the Salesforce opportunity record Id is assigned to the remote table sys\_id. This ensures that lists and forms for the remote table function properly and that we are able to extract the record Id using `v_query.getSysId()` the next time that the remote table script is invoked.

Then display the information message if it was passed by the query.

```
if (outputs.info_message) {
  gs.addInfoMessage(outputs.info_message);
}

```

## Putting the remote table script sections together

The three sections of the script are included in the try-catch block to provide for error handling.

```
(function executeQuery(v_table, v_query) {

  try {

    // place code here from: <Selecting a spoke action and preparing the inputs>

    // place code here from: <Calling the spoke action>

    // place code here from: <Processing the action output>  	
        
  } catch (error) {
    gs.addErrorMessage("Error retrieving  Salesforce Opportunities. “ +
                       “Please contact System Administrator.");
    gs.addErrorMessage("System Error: " + error.message);
  }

})(v_table, v_query);

```

**Parent Topic:**[Using remote tables and the Salesforce spoke](csm-integration-remote-tables.md)

