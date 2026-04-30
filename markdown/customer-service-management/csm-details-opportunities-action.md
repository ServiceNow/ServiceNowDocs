---
title: Get Opportunities Details custom action
description: The Get Opportunities Details action retrieves a single Opportunity record from the Salesforce application based on the record Id. This action is invoked when the user opens the form for the Opportunity record in the remote table.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create Salesforce spoke actions to retrieve opportunities for use in the remote table definition, Using remote tables and the Salesforce spoke, Reference Salesforce integration using remote tables, Third-party data integration for CSM, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Get Opportunities Details custom action

The **Get Opportunities Details** action retrieves a single Opportunity record from the Salesforce application based on the record Id. This action is invoked when the user opens the form for the Opportunity record in the remote table.

## Action inputs

The **Get Opportunities Details** action takes a single integer parameter that identifies the Salesforce Account ID. This parameter is set by the form based on the sys\_id that was provided to the remote table in the remote table script. For more information, see [Example script that queries the Opportunity table](../concept/csm-opportunity-table-script.md).

![Get Opportunity Details page with Action Input section and Action Outline side panel with: Pre Processing script, REST step, and Post Processing script inputs.](../image/get-opportunity-details-action.jpg)

## Pre-processing step

The pre-processing script step takes the action inputs as its own.

![Pre Processing step:containing fields for Required Runtime, and Input Variables - Name and Value.](../image/get-opportunity-details-pre-processing.jpg)

As with other actions, the pre-processing step creates an opportunity query for the specific parameter. In this case, the match is done against the opportunity record Id. Do not worry about the LIMIT in this query because it returns at maximum a single record.

```
(function execute(inputs, outputs) {
  
  outputs.query = "query/?q=SELECT+Name,Id,AccountId,CloseDate,Amount,” +
                  “StageName,Probability,Type+FROM+Opportunity”         +
                  
               "+WHERE+Id='" + inputs.salesforce_opportunity_record_id + "'"; 
  
})(inputs, outputs);

```

The pre-processing output is a query similar to the other custom actions.

## REST step, post-processing step, and action outputs

These steps and outputs are the same as for the other custom actions except there is no maximum number of records parameter and no information message.

**Parent Topic:**[Create Salesforce spoke actions to retrieve opportunities for use in the remote table definition](../concept/csm-integration-salesforce-spoke.md)

