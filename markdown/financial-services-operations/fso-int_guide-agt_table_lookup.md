---
title: Lookup remote information in the system of record
description: This use case illustrates how to use a REST API call to lookup financial transaction details for a customer’s mortgage account on a remote banking system \(system of record\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration use cases, Developer resources, Financial Services Operations \(FSO\)]
---

# Lookup remote information in the system of record

This use case illustrates how to use a REST API call to lookup financial transaction details for a customer’s mortgage account on a remote banking system \(system of record\).

A call center agent responds to a customer inquiry and creates a new FSO case using a ServiceNow form. In that form, they manually enter the consumer, financial account, category, and short description information, and any associated notes.

Using the consumer and financial account information, a script within the ServiceNow form calls a remote REST endpoint on the remote banking system \(bank application\) to obtain the financial transaction details. It then displays these details in the ServiceNow form so that the agent can verify the information before manually entering the remainder of the required case information. Once complete, the FSO case is cached on the ServiceNow instance.

**Note:** This use case assumes the bank application exposes the REST endpoint GET /api/getTransactions that returns the requested consumer details and their associated financial account.

The following is an example of what the financial transaction details received from the remote bank application might look like when they appear on the FSO case form:

The following diagram shows the application flow for this use case scenario and provides brief remarks on any required processing. In this implementation, the data obtained from the remote bank application is store in remote tables. [Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md) are only cached in memory, they are never stored in the ServiceNow database tables. You can also implement this scenario by writing the remote data to the corresponding ServiceNow database tables. The [s](fso-int_guide-agt_submit_case.md) scenario illustrates how to store data in the ServiceNow database tables using the [GlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md) API.

<table id="table_rmq_ywq_bpb"><tbody><tr><td>

 

</td><td>

1.  The agent enters the required information on the FSO form. Using this information, formulate the REST call /api/getTransactions using the [RESTMessageV2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_RESTMessageV2API.md) API and send it to the remote bank application to obtain the customer's financial transaction details.
2.  The remote bank application processes the request and returns the specified customer's financial transaction details.
3.  The financial transaction details are cached on the ServiceNow instance in remote tables using the [v\_table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/v_tableAPI.md) API.
4.  The transaction details are then displayed on the FSO form.

</td></tr></tbody>
</table>## Example code

The follow code example shows how to use the [RESTMessageV2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_RESTMessageV2API.md) API to create and execute the REST call to the external bank application. It then store the return results in a [remote table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md) using the [v\_table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/v_tableAPI.md) API. Before you can use the v\_table API you must activate the Remote Tables \(com.glide.script.vtable\) plugin.

```
(function executeQuery (v_table, v_query) {
// Parameters needed in the request body of the REST endpoint
  var requestBody = {
    'financial_account':v_query.getParameter('financial_account')
  };

  // Instantiate the RESTMessageV2 object
  var request = new sn_ws.RESTMessageV2();
  // Set the HTTP method as "GET"
  request.setHttpMethod('get');
  // URL of the endpoint on the bank application
  request.setEndpoint('https://<yourbankapphost>/api/getTransactionDetails');
  // Request body as a string
  request.setRequestBody(JSON.stringify(requestBody));
  // Call the REST endpoint
  var response = request.execute();
  // Get the response body
  var responseBody = response.getBody();
  // Parse the response body into an object
  var responseObj = JSON.parse(responseBody);

  // Store the response body into a virtual table
  v_table.addRow({
    sys_id: gs.generateGUID(),
    amount: responseObj.amount,
    description: responseObj.description,
    posting_date: responseObj.posting_date,
    transaction_date: responseObj.transaction_date
  });

}) (v_table, v_query);
```

## Example code

The follow code example shows how to query a remote table and display it in the FSO form.

```
function getRequiredInfo() {

  // Instantiate a GlideRecord object with the remote table containing the financial transaction details.
  var now_GR = new GlideRecord('transaction_details_remote_table');

  // Create a query to obtain the desired financial account
  now_GR.addQuery('financial_account', g_form.getValue('financial_account'));

  // Execute the query
  var result = now_GR.query(); 

  // Display the data in the FSO form
  var data = [];
  data ['amount'] = result.amount;
  data ['description'] = result.description;
  data ['posting_date'] = result.posting_date;
  data ['transaction_date'] = result.transaction_date;

  return data;
}

getRequiredInfo();
```

