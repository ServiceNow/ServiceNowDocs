---
title: Create an external connection
description: Create an external connection in CPQ to enable enrichments to retrieve data from an external system for use in configuration rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-external-connection.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up External connections for configuration rules, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create an external connection

Create an external connection in CPQ to enable enrichments to retrieve data from an external system for use in configuration rules.

## Before you begin

Role required: admin

## About this task

External connections are used in configuration rules only. They can only be called from an enrichment script. After you configure an external connection, reference it in your enrichment script using `External.*connectionName*(inputs)`, where *connectionName* is the unique name of the connection.

\[Omitted image "cpq-enrichments-external-connections.png"\] Alt text: External Connections list view in CPQ Administration

**Note:** To call an external system from a transaction rule instead, add a connection. For more information, see .

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Utilities** &gt; **External Connections**.

2.  Select **+New** to create a new external connection.

3.  In the **Authentication type** field, select the credential method that the external system requires, then complete the fields for that authentication type.

<table><thead><tr><th align="left" id="d103299e146">

Authentication type

</th><th align="left" id="d103299e149">

Action

</th></tr></thead><tbody><tr><td id="d103299e155">

**No authentication**

</td><td>

No additional fields are required. The external connection calls the API without credentials.

</td></tr><tr><td id="d103299e164">

**Bearer token**

</td><td>

In the **Authentication token** field, enter the bearer token provided by the external service.

</td></tr><tr><td id="d103299e176">

**OAuth - Client credentials flow**

</td><td>

Complete the following fields:-   **Client ID**: Client identifier created for CPQ with the authorization server.
-   **Client secret**: Tokenized reference to the client secret. The actual value is stored in the GCP secret store. In development environments, the value is stored directly.
-   **Token URL**: URL of the authorization server where CPQ exchanges the client ID and secret for an access token.
-   **Scope**: Scopes to include in the token request. This field is available only when OAuth - Client credentials flow is selected in the Authentication type field.


</td></tr></tbody>
</table>4.  In the **Path** field, enter the path to append to the host URL, including any parameter variables for dynamic segments.

    Use double curly braces to define a parameter variable in the path. For example:

    ```
    /v4/latest/{{inputVariable}}
    ```

    In your enrichment script, pass the variable as a key-value pair in the inputs object and wrap the value in `encodeURIComponent()` to ensure the value is URL-safe:

    ```
    let inputs = {"inputVariable": encodeURIComponent(cfgRequest.baseCurrency.value)};
    let results = External.exchangeRatesAPI(inputs);
    ```

5.  In the **Timeout** field, enter the maximum time in milliseconds that CPQ waits for a response from the external system.

    Start with 500 milliseconds. If the external connection regularly exceeds this limit, increase the value, keeping in mind that higher timeouts may slow the end-user configuration experience.

6.  Select **Save**.


## Result

The external connection is saved and available to call from enrichment scripts.

## BOM enrichment using an external pricing connection

The following on-BOM-response enrichment calls a `powerPricing` external connection to retrieve customer-specific rate data and apply it to `ProductList` records. The connection accepts two input variables — `membershipCode` and `icp` — and returns a pricing response that the script uses to set prices on individual products.

```
var powerInputs = {"membershipCode": cfg.eCMembershipCode, "icp": cfg.eCICPNumber};
let powerResponse = External.powerPricing(powerInputs);

let dailyCharge = 0;
let ratesArr = [];

if (powerResponse.status == 200) {

  for (var record of powerResponse.body) {
    if (record.chargeType == cfg.expectedUsage) {
      dailyCharge = record.dailyCharges;
      ratesArr = record.rates;
    }
  }

  for (var prod of ProductList) {
    if (prod.id == "electricBillEstimator") {
      let addedPrice = dailyCharge * cfg.serviceDurationInDays;
      prod.price = addedPrice;
    }
    if (prod.id == "Standard Rate" || prod.id == "Low Rate") {
      prod.price = dailyCharge;
    }
  }

  for (var rateVal of ratesArr) {
    ProductList.id = "Additional Charge Per KWH: " + rateVal.name;
    ProductList.quantity = 1;
    ProductList.bomType = "Manufacturing";
    ProductList.orderNumber = 2;
    ProductList.price = rateVal.rate;
    ProductList.notes = rateVal.measure;
    ProductList.parentProduct = "electricBillEstimator";
    ProductList.next();
  }

}

return ProductList;
```

**Related topics**  


[Set up External connections for configuration rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/external-connections.md)

