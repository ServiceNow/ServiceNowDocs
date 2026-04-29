---
title: Get All Opportunities custom action
description: The Get All Opportunities action retrieves opportunity records from the Salesforce application. This action is invoked when you view the remote Opportunity table.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Retrieve opportunities, Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Get All Opportunities custom action

The **Get All Opportunities** action retrieves opportunity records from the Salesforce application. This action is invoked when you view the remote Opportunity table.

## Action inputs

The **Get All Opportunities** action takes a single integer parameter that identifies the maximum number of records to be returned by the query. The REST-based actions can’t accommodate pagination and, for this reason, it’s important to limit the number of records returned from the third-party application. It isn’t recommended to place more than 1,000 records in the remote table. The default number of records is 500.

![Inputs screen for the Get All Opportunities action showing the action input and its default value.](../image/get-all-opportunities-action-input.jpg)

## Pre-processing step

The pre-processing script step takes the action input as its own.

![Pre-processing step screen showing the action input with a pill picker to generate a query.](../image/get-all-opportunities-pre-processing.jpg)

The pre-processing script creates a SELECT query for all opportunities limited by the maximum number of records allowed. This query is based on the Salesforce Object Query Language \(SOQL\).

```
(function execute(inputs, outputs) {
  
  outputs.query = "query/?q=SELECT+Name,Id,AccountId,CloseDate,Amount,” +
                  “StageName,Probability,Type+FROM+Opportunity”;

  outputs.query = outputs.query +
                  “+LIMIT+” + inputs.max_number_of_opportunity_records; 
  
})(inputs, outputs);

```

You must specify the fields from the opportunity records that you’re interested in. This example uses the following fields: Name, Id, Account Id, Close Date, Amount, Stage Name, and Probability. To see the full list of available fields, use the **Get Opportunity Fields** action.

You can also control the ordering of the query search by adding the ORDERED BY keyword and value for ASC or DESC order direction. For example, you can add the following line to the script before the line specifying the LIMIT. It makes the query return the first 500 records with the most recent Close Date.

```
outputs.query = outputs.query + “+ORDERED+BY+CloseDate+DESC”;
```

The pre-processing output is a query.

![Output variable section showing the query parameter as an output.](../image/get-all-opportunities-pre-processing-output.jpg)

## REST step

The REST step is a standard REST step from the Salesforce spoke REST-based actions. You don’t need to make any changes. Make sure that it points to the correct Connection Alias.

![REST step screen showing connection details and request details for verification.](../image/get-all-opportunities-rest.jpg)

## Post-processing step

The post-processing script step takes the action input and REST step output as its inputs.

![Post Processing step screen showing the inputs, including the action input and input variables.](../image/get-all-opportunities-post-processing.jpg)

The post-processing script checks the query response for errors, sets the error message if needed, extracts opportunity data from the response body, and creates an information message to indicate that not all data was retrieved from the Salesforce due to the number of records limitation.

```
(function execute(inputs, outputs) {

  try{
    var response = JSON.parse(inputs.res_body);
  } catch(e) {
    outputs = errorHandler(inputs, outputs);
  }


  function createOutputJson(inputs, outputs) {
    try{
      outputs.records = { data: response.records };
      outputs.status = "Success";

      if ( outputs.records.data.length ==   
           inputs.max_number_of_opportunity_records ) {
        outputs.info_message = "Opportunity retrieve operation was “ +
                               “limited to" +
                               inputs.max_number_of_opportunity_records +
                               " records.";
      }      
    } catch(e) {
      outputs = errorHandler(inputs, outputs);
    }
    return outputs;
  }


  function errorHandler(inputs, outputs) {
    outputs.status = "Error";
    outputs.error_message = "Unknown Error. “ + 
                            “Please check error log for more information";

    if(inputs.res_body.contains("message"))
      outputs.error_message = response[0].message;

    return outputs;
  }

  if(inputs.status_code == "200")
    outputs = createOutputJson(inputs, outputs);
  else
    outputs = errorHandler(inputs, outputs);

})(inputs, outputs);

```

The following are outputs of the post-processing step.

![Output variable screen within the Post Processing step showing records, error_messages, info_messages, and status variables.](../image/get-all-opportunities-post-processing-output.jpg)

## Action outputs

Action outputs consist of the query status, error and information messages, and opportunity records. See the preceding screenshot for the action outputs.

**Parent Topic:**[Create Salesforce spoke actions to retrieve opportunities](../concept/csm-integration-salesforce-spoke.md)

