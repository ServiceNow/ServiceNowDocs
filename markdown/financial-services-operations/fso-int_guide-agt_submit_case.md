---
title: Agent submitting a case
description: This use case illustrates how to enable an agent to submit a case for a known customer.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integration use cases, Developer resources, Financial Services Operations \(FSO\)]
---

# Agent submitting a case

This use case illustrates how to enable an agent to submit a case for a known customer.

In this scenario, from within an FSO complaint form, an agent looks up a customer's account information, which is located on a remote bank application. Once located, it appears within the complaint form and the agent then manually fills in the case details related to the customer's mortgage account and save the complaint case. In the background, the form script saves the customer details and financial account information locally on the ServiceNow instance.

**Note:** This scenario assumes the bank application exposes two REST endpoints GET /api/getConsumerDetails and GET /api/getFinancialAccounts that return the requested consumer details and their associated financial account information.

The ServiceNow tables that are accessed in this scenario are the following:

-   Consumer \[csm\_consumer\]: Contains customer record.
-   Loan Account \[sn\_bom\_loan\_account\]: Contains loan account information for each customer.

    **Note:** Loan Account is a type of Financial Account.


The following is an example of a ServiceNow complaint form \(case form\) that walks an agent through filing a complaint on behalf of a customer. In this form, the agent clicks the Account Search button on the form to locate the customer's account information.

When the agent clicks the **Account Search** a pop-up similar to the following appears. The pop-up allows the agent to lookup the customer's account using any of the displayed search parameters. You can create your own search criteria based on your specific web service. These web services generally come from Customer Master and Account Master systems, CRMs, core banking mainframes, and APIs from core banking software providers such as Fiserv, FIS, Jack Henry, Finastra and others.

The search returns the following accounts for this customer.

The agent selects the appropriate account and the necessary account information is automatically populated in the case form. The agent then adds any additional information needed to submit the customer case and clicks the **Submit** button to save the complaint in the ServiceNow instance.

The following diagram shows the flow of the REST API calls for this use case and provides brief remarks on any required processing.

<table id="table_rmq_ywq_bpb"><tbody><tr><td>



</td><td>

1.  The agent enters the customer lookup information on the complaint form. Using this information, formulate the REST call /api/getConsumerDetails using the [RESTMessageV2](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=australia&pubname=australia-api-reference&ft:locale=en-US) API and send it to the remote bank application to obtain the customer's account details.
2.  The /getConsumerDetails endpoint returns the consumer details or an error if the customer is not located.
3.  Using the [GlideRecord](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) API, create/update the associated customer record in the ServiceNow Consumers \[csm\_consumer\] table with the consumer information.
4.  Using the account information returned by the /api/getConsumerDetails REST call, lookup the customer mortgage record on the remote bank application. Again, use the RESTMessageV2 API to formulate and send the call to the /getFinancialAccounts endpoint on the bank application to obtain the customer's mortgage record.
5.  The /getFinancialAccounts endpoint returns the financial accounts associated with the specified customer.
6.  Using the [GlideRecord](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) API, create/update the associated consumer's financial account information in the ServiceNow financial\_account table.

</td></tr></tbody>
</table>## Example code

The follow is a JavaScript example that performs the steps outlined above:

```
// Fetch consumers for the given first name and last name and associated
// financial accounts from the remote bank application
function fetchConsumers(consumer_fname, consumer_lname) {

  var request = new sn_ws.RESTMessageV2();
  request.setHttpMethod('get');
  request.setEndpoint('api/getConsumerDetails?fname=consumer_fname&lname=consumer_lname');

  var response = request.execute();
  var responseBody = response.getBody();
  var responseObj = JSON.parse(responseBody);
  var consumers = responseObj.consumers;

  // Create a record in the ServiceNow Consumer [csm_consumer] table for the specified consumer
  var consumerDetails = [];
  consumers.foreach(function(consumer){
    var consumerGR = new GlideRecord('csm_consumer');
    consumerGR.initialize();
    consumerGR.setValue('uid', consumer.uid);
    consumerGR.setValue('name', consumer.name);
    consumerGR.setValue('email', consumer.email);
    consumerGR.setValue('mobile', consumer.mobile);
    consumerGR.setValue('address', consumer.address);
    if(consumerGR.update()){
      consumer.sysId = consumerGR.getValue('sys_id');
      consumer.financialAccount = fetchFinancialAccountsForConsumer(consumer);
    }
  });
}
// Fetch financial accounts for the specified consumer
function fetchFinancialAccountsForConsumer(consumer) {

  var financialAccounts = [];
  var request = new sn_ws.RESTMessageV2();
  request.setHttpMethod('get');
  request.setEndpoint('api/getFinancialAccounts/' + consumer);
  var response = request.execute();
  var responseBody = response.getBody();
  var responseObj = JSON.parse(responseBody);
  var financialAccounts = responseObj.financialAccounts;

// Create a record in the ServiceNow financial_account table for each of the customer's financial accounts
  financialAccounts.foreach(function(finAccount){
    var finAccountGR = new GlideRecord('financial_account');
    finAccountGR.initialize();
    finAccountGR.setValue('uid', finAccount.uid);
    finAccountGR.setValue('type', finAccount.type);
    finAccountGR.setValue('number', finAccount.ac_number);
    finAccountGR.setValue('balance', finAccount.balance);

    if(finAccountGR.update()){
      finAccount.sysId = finAccountGR.getValue('balance');
      financialAccounts.push(finAccount);
    }
  });

  return financialAccounts;
}


// The following retrieves an object to display in UI page

fnmae = ‘john’;
lname = ‘brown’;

var consumerObj = fetchConsumers(fname, lname);

consumerObj.foreach(function(consumer){
  // Display the details on the page and populate it in the form as necessary
  console.log(consumer);
});
```

