---
title: Using external connections with OAuth support
description: External connections allow enrichments to retrieve data from third-party systems to enhance configurations. When security requires OAuth, you can set up an OAuth handshake using client credentials to authenticate and access external APIs. This approach ensures secure data exchange for tasks such as pricing updates or attribute population during configuration.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Using external connections with OAuth support

External connections allow enrichments to retrieve data from third-party systems to enhance configurations. When security requires OAuth, you can set up an OAuth handshake using client credentials to authenticate and access external APIs. This approach ensures secure data exchange for tasks such as pricing updates or attribute population during configuration.

Enrichments are scripts that run outside the rules engine and affect configurations in CPQ. There are five types of enrichments that can be enabled in a CPQ environment:

-   On configure/reconfigure
-   On BOM response
-   Validation
-   Picklist extension pricing
-   On request

External connections get data for a CPQ configuration from something outside CPQ. External connections can only be called from an enrichment.

Occasionally, an external connection requires an OAuth handshake for security purposes. For example, you may need to populate a field or an enrichment script with data from a third-party application, such as pricing or other attributes.

To set an OAuth external connection, follow these steps:

1.  Define the external connection by visiting Admin &gt; Utilities &gt; External Connections.

    ![External connections user interface](../images/cpq-enrichments-external-connections.png)

2.  Define your authentication token.
    -   If the external connection calls an open API, no authentication token is needed.
    -   If the external connection is Salesforce, CPQ takes care of the authentication token for you.
    -   If the authentication supports a bearer token, insert the bearer token provided by the external service for the purposes of authentication.
    -   If the authentication requires OAuth authentication:

        1.  Select OAuth - Client Credentials Flow
        2.  Insert the client ID
        3.  Insert the client secret
        4.  Insert the token URL field
        Required OAuth inputs:

<table id="table_jhn_jnh_bhc"><thead><tr><th>

Field

</th><th>

Type

</th><th>

Description

</th><th>

Validations

</th></tr></thead><tbody><tr><td>

Client ID \(Required\)

</td><td>

varchar \(unlimited\)

</td><td>

Holds the client ID created for CPQ with the authorization server

</td><td>

Not empty

</td></tr><tr><td>

Client secret \(Required\)

</td><td>

varchar \(unlimited\)

</td><td>

Holds a tokenized reference to the client secret

 The actual value is stored in the GCP secret store, except in dev environments, where the value is stored directly

</td><td>

Not empty

</td></tr><tr><td>

Token URL \(Required\)

</td><td>

varchar \(unlimited\)

</td><td>

The URL of the authorization server to exchange the client ID/secret with for a token

</td><td>

Not empty

</td></tr><tr><td>

Scope \(Optional\)

</td><td>

varchar \(unlimited\)

</td><td>

Optional - can be used to specify the scopes sent with the token request

</td><td>

None

</td></tr></tbody>
</table>3.  Specify the parameters that need to be passed to the destination server in the Path input.

    Parameter variables can be used to dynamically define the path. An example path is `/v4/latest/{{inputVariable}}`, where `{{inputVariable}}` is the section of the path that is used as the parameter variable.

    If a path is using a parameter variable, use `encodeURIComponent()` in your enrichment script when you define the variable. For an example, see the following code.

    ```
    let inputs = {"inputVariable":encodeURIComponent(cfgRequest.baseCurrency.value)};
    let results = External.exchangeRatesAPI(inputs);
    var resultsMap = results.body.rates;
    ```

    Line 1 defines the variable, referencing the parameter variable from our external connection “inputVariable”. A CPQ field that stores the data we want is wrapped in encodeURIComponent and completes the inputVariable path.

    Line 2 and 3 then trigger the external connection `exchangeRatesAPI` using the defined input. Additional scripting is required for the call to be narrowed down to retrieve the desired data and set a field, if that is a desired use case.

    A timeout limit is needed. We suggest 500 milliseconds as a starting point. If you find that the external connection regularly exceeds this limit, you can increase this value. However, this may slow the performance of the end-user configuration.

    The following enrichment script uses an external connection. This bill of materials \(BOM\) enrichment queries a powerPricing API with customer data. With the customer-specific rate date retrieved from the service, the enrichment adjusts the pricing of existing ProductList records.

    ```
    var powerInputs = {"membershipCode":cfg.eCMembershipCode, "icp":cfg.eCICPNumber}; let powerResponse = External.powerPricing(powerInputs);
    
    let dailyCharge = 0; let ratesArr = [];
    
    if(powerResponse.status == 200) {
    
    for(var record of powerResponse.body) { if(record.chargeType == cfg.expectedUsage) {
    
    dailyCharge = record.dailyCharges; ratesArr = record.rates;
    
    }
    
    }
    
    for(var prod of ProductList) { if(prod.id=="electricBillEstimator") {
    
    let addedPrice = dailyCharge * cfg.serviceDurationInDays; prod.price = addedPrice;
    
    }
    
    if(prod.id=="Standard Rate" || prod.id=="Low Rate") { prod.price = dailyCharge;
    
    }
    
    }
    
    for(var rateVal of ratesArr) {
    
    ProductList.id = "Additional Charge Per KWH: " + rateVal.name; ProductList.quantity = 1;
    ductList.bomType="Manufacturing"; ProductList.orderNumber = 2;
    
    ProductList.price = rateVal.rate; ProductList.notes = rateVal.measure;
    ductList.parentProduct="electricBillEstimator"; ProductList.next();
    
    }
    
    }
    
    return ProductList;
    ```


