---
title: Get Opportunities for Account Id custom action
description: The Get Opportunities for Account Id action retrieves opportunity records for the specific Salesforce account. This action is invoked when the agent views a Salesforce opportunity available for the customer account based on the Salesforce account associated with it.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create Salesforce spoke actions to retrieve opportunities for use in the remote table definition, Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Get Opportunities for Account Id custom action

The **Get Opportunities for Account Id** action retrieves opportunity records for the specific Salesforce account. This action is invoked when the agent views a Salesforce opportunity available for the customer account based on the Salesforce account associated with it.

This action is similar to the **Get All Opportunities** action.

## Action inputs

In addition to the maximum number of records to be returned by the query, this action also takes a Salesforce Account Id as input to be used as a query parameter. The value of this parameter is provided by the relationship that links the customer account and the Salesforce opportunity through the associated Salesforce Account Id. For more information, see [Create defined related lists](csm-account-opportunities-action.md).

The specific relationship needed for the reference example is also described in the [Using a related list to create the connection between the Customer Account and Salesforce Opportunities](../concept/csm-related-list-opportunity-table.md) topic.

The Salesforce Account Id action input parameter has no default value.

![Inputs screen showing the action inputs and their default values.](../image/get-opportunities-account-id-action.jpg)

Action Outline with Inputs: Pre Processing script, REST step, Post Processing script. Action Input showing Label, Name, Type, and a toggle for Mandatory.

## Pre-processing step

The pre-processing script step takes the action input as its own.

![Pre-processing step screen showing the action inputs with pill pickers to generate a queries.](../image/get-opportunities-account-id-pre-processing.jpg)

The Pre-Processing step script creates a SELECT query similar to the one created for the **Get All Opportunities** action with the addition of the check against the Salesforce Account Id.

```
(function execute(inputs, outputs) {
  
  outputs.query = "query/?q=SELECT+Name,Id,AccountId,CloseDate,Amount,” +
                  “StageName,Probability,Type+FROM+Opportunity”         +
                  
                  "+WHERE+AccountId='" + inputs.salesforce_account_id + "

                  “+LIMIT+” + inputs.max_number_of_opportunity_records; 
  
})(inputs, outputs);

```

The pre-processing output is a query, similar to the **Get All Opportunities** action.

## REST step, post-processing step, and action outputs

These steps and outputs are the same as for the **Get All Opportunities** action.

**Parent Topic:**[Create Salesforce spoke actions to retrieve opportunities for use in the remote table definition](../concept/csm-integration-salesforce-spoke.md)

