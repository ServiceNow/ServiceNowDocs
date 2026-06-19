---
title: The On Request enrichment
description: Information about an enrichment you shouldn't use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/on\_request\_enrichment.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The On Request enrichment

Information about an enrichment you shouldn't use.

**Important:** The On Request enrichment is almost never a recommended pattern. This enrichment type can make configuration performance dependent on outside systems and result in a less than ideal end user experience. Consult Customer Success about other ways to achieve your desired outcome.

The On Request enrichment enables the same capabilities as the [On Configure/Reconfigure Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/enrichments-on-configure-reconfigure-scripts-how-to-populate-set-values.md), except that it is called after each field change to any field in the enrichment.

In this enrichment, all external API calls time out after five seconds.

General guidelines:

-   Wrap external APIs in validation logic to ensure that they are only called when absolutely necessary.
-   Always validate all data required to run an API before you directly call the API.
-   Use ogic to limit running external APIs.
-   Make sure that any API called in an on request enrichment is able to fully run and respond quickly.

    ```
    // Here we use a boolean field to delay the running of additional code
    if (cfgRequest.runOnRequest == true) {
      cfgRequest.onRequestTextField.value = "On Request Ran";
    }p
    cfgRequest.runOnRequest = false;
    ```

-   Avoid non-performant or long-running APIs.

