---
title: Creating an integration script include for third-party carrier applications
description: In order to integrate with a ServiceNow instance, a third-party carrier application must have a script include that extends the base class ITAMShipmentIntegration script on its ServiceNow instance to receive the shipment tracking number from the customer's ServiceNow instance and respond with the carrier-related details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/creating-integration-script-include-ham.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure shipment tracking, Integrations and advanced configuration, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Creating an integration script include for third-party carrier applications

In order to integrate with a ServiceNow instance, a third-party carrier application must have a script include that extends the base class `ITAMShipmentIntegration` script on its ServiceNow instance to receive the shipment tracking number from the customer's ServiceNow instance and respond with the carrier-related details.

Consider the following when you create the script include:

-   Make sure that the script include is accessible from the Asset Management Common application scope by adjusting the following settings on the application resource record:
    -   Set the **Accessible from** field to **All application scopes**.
    -   Set the **Caller Access** field to **None** to make sure the caller access isn't restricted.
-   The code for communicating with the customer's ServiceNow instance based on the tracking number must be included within the fetchShipmentInfo function.
-   When the API is invoked in the test mode for validating the connection with the customer's ServiceNow instance, the return response from the fetchShipmentInfo method should be a JSON object with the HTTP response code and response message, as follows:

    ```
    {
    httpResponseCode: 200, httpResponseMessage: ‘SUCCESS’
    }
    
    ```

-   When not in the test mode, query the shipments and invoke the processResponse method with the following response format:

    ```
    [
    {
    trackingNumber: ‘’,
    deliveryDate: ‘’,
    pickupDate: ‘’,
    packageStatus: ‘’.
    statusDetail: ‘’,
    trackingURL: ‘’,
    parcelWeight: ‘’,
    deliveryServicesCost: ‘’,
    currency: ‘’
    }
    	]
    
    ```


## ITAMShipmentIntegration script include sample codes

\[Omitted image "script-incl-sample-carrier.png"\] Alt text: ITAMShipmentIntegration script include with ITAM processResponse function

\[Omitted image "script-incl-custom-carrier.png"\] Alt text: ITAMShipmentIntegration script include with custom processResponse function

## fetchShipmentInfo function

The fetchShipmentInfo function receives the tracking numbers from the ServiceNow instance of the customer and invokes the carrier API to fetch the shipment details for all the tracking numbers. Within this function, you must define the business logic that enables your customers to communicate with your carrier APIs based on the tracking numbers. This function processes the response that is received from the carrier API and invokes the post-processing function.

## processResponse function

The processResponse function receives the response from the carrier API and updates the shipment records with the following carrier-related details:

-   Carrier link
-   Carrier status
-   Carrier status detail
-   Carrier pick-up date
-   Carrier delivered date
-   Currency
-   Delivery services cost
-   Parcel weight

You can either use the default processResponse function or define a custom logic to update the shipment records.

**Parent Topic:**[Integration framework configuration for shipment tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/configure-int-frame-shipment.md)

