---
title: Update remote information in the system of record
description: This integration scenario illustrates how to update a system of record within the bank application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration use cases, Developer resources, Financial Services Operations \(FSO\)]
---

# Update remote information in the system of record

This integration scenario illustrates how to update a system of record within the bank application.

In this scenario, a script in a ServiceNow workflow makes a request to the remote bank application to update a customer's credit card limit. If the new limit is approved, the customer limit is updated in the bank application \(system of record\).

**Note:** There are cases where the same information, such as a customer's credit card limit, is in both the system of record on a remote system and in the ServiceNow database. Whenever querying this type of information, ensure that you always use the information in the system of record, as the information in the ServiceNow database may not be current. Use your discretion as to whether you update this information in both data stores. This use case does not update the information in the Credit Card Account \[sn\_bom\_cred\_card\] table.

**Note:** This scenario assumes the bank application exposes the REST endpoint POST /api/card/updateLimit that handles the update request from the ServiceNow workflow.

![FSO case flow that shows how to update a system of record within the bank application](../image/fso-update_external_record-flow.png)

The table that is accessed in this scenario is the [Consumer](../reference/fso-int_guide-table_defs.md#csm_consumer) \[csm\_consumer\] table which contains the business-to-customer records.

The following diagram shows the flow of the REST API calls for this use case and provides brief remarks on any required processing. It assumes that you have used the steps outlined in [Lookup remote information in the system of record](fso-int_guide-agt_table_lookup.md) to obtain the customer account information.

<table id="table_rmq_ywq_bpb"><tbody><tr><td>

![Workflow that shows the REST API calls that are used to obtain the customer account information.](../image/fso-update_ext_record-swim_diagram.png)

</td><td>

1.  Script in the workflow requests the associated consumer record and uses that information to obtain the information needed to request the associated Credit Card Account record.
2.  Script in the workflow calls the POST /api/card/updateLimit endpoint on the bank application to request that the associated customer's credit limit be increased.
3.  Bank application returns the status of the request.
4.  Status update

</td></tr></tbody>
</table>## Example code

The follow is a JavaScript example that performs the steps outlined above:

```
// Shows how to  request the increase the credit limit for a specified card
// This code assumes there is a REST endpoint 'api/card/updateLimit' on the bank application system

// REST call to the /api/card/updateLimit endpoint to request 
// an update to the customer's credit card limit
function updateCreditLimit(requestBody) {

  var request = new sn_ws.RESTMessageV2();
  request.setHttpMethod('post');
  request.setEndpoint('/api/card/updateLimit');
  request.setRequestBody(JSON.stringify(requestBody));
  var response = request.execute();

  var responseBody = response.getBody();
  var responseObj = JSON.parse(responseBody);

  return responseObj;
}

// The following is the data object sent to the /api/card/updateLimit endpoint
// to increase the credit limit for the card
var requestBody = {
  'cardNumber': 'xxxx-xxxx-xxxx-5896',
  'accountNumber': 'xxxxxxxxxxxx9590',
  'oldLimit': 'USD 5000',
  'newLimit': 'USD 10000',
  'requestType': 'Increase_limit',
};

updateCreditLimit (requestBody);
```

