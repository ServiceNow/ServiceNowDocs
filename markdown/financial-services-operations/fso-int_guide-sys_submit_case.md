---
title: External systems submitting a case request
description: This use case illustrates how the ServiceNow Financial Services Operations \(FSO\) product can receive case requests from an external system, such as online or mobile banking application, core banking systems, or other CRM tools.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration use cases, Using the developer guide, Financial Services Operations \(FSO\)]
---

# External systems submitting a case request

This use case illustrates how the ServiceNow Financial Services Operations \(FSO\) product can receive case requests from an external system, such as online or mobile banking application, core banking systems, or other CRM tools.

Any system that can handle making REST API calls can implement this scenario to create customer cases in FSO. In this scenario, the fields consumer, financial account, category, short description, and notes are sent from the external system.

![FSO case flow showing requests from external systems.](../image/fso-external_case_req.png)

The table that is accessed in this scenario is the Loan Service Case \[sn\_bom\_loan\_service\].

The following diagram shows the flow of the REST API calls for this scenario and provides brief remarks on the processing.

<table id="table_rmq_ywq_bpb"><tbody><tr><td>

![Flow diagram shows how an agent creates a loan case record and the flow of various REST API calls for processing. the case.](../image/fso-external_case_req-swim_diagram.png)

</td><td>

1.  In the bank application, define the information necessary to create the loan case record, and then call the [POST /now/table/\{table\_Name\}](https://www.servicenow.com/docs/access?context=c_TableAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) REST endpoint on your ServiceNow instance.
2.  The Table API attempts to write the posted information to the Loan Service Case \[sn\_bom\_loan\_service\] table.
3.  The Table API returns the results of the POST request.

</td></tr></tbody>
</table>## Example code

The follow is a JavaScript example that generates the necessary REST API call information and then sends the POST request to your ServiceNow instance.

```
// Construct the REST call to POST the creation of the loan service case on the ServiceNow instance
// 
function createRecord(tableName, requestBody) {

  var client = new XMLHttpRequest();
  client.open('post', 'http://<instance.servicenow.com>/api/now/tableName);
  client.setRequestHeader('Accept', 'application/json');
  client.setRequestHeader('Content-Type', 'application/json');

  client.onreadystatechange = function() {
    if (this.readyState == this.DONE) {
      console.log(this.status + this.response);
    }
  };

  client.send(JSON.stringify(requestBody)); // Send the POST request to the ServiceNow instance
}

// Create the requestBody object to send to the Table API to create the loan service case.
// This is the typical minimum data that should be passed. You can write to any of the record fields except those
// starting with 'sys_' - these are system generated read-only fields.

var tableName = ‘sn_bom_loan_service’;
var requestBody = {
  'consumer': '8938984kljhkhg34j5689903498u5',  // Sys_id of the associated consumer
  'sold_product': '9590349760hkjhi3450983405033', // Sys_id of the customer loan account. 
  'assignment_group': '5469813sae32135s5d55d5d6s6sdd',  // Sys_id of the group to assign the case to
  'contact_type': 'web',  // Communication method used by customer to contact agent
  'product': '54666s6s46s6d6e4116b1f3rgt',  // Sys_id of the product model of the asset associated to the case.
  'service_definition': '989300jfkh8403jf87uj3h9-03i984n4', // Sys_id of the definition of service associated with this account. 
  'short_description': 'Request for loan forgiveness' // Short description for the loan case
};

createRecord(tableName, requestBody);
```

