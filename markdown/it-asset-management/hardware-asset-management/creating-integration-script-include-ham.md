---
title: Creating an integration script include for third-party carrier applications
description: In order to integrate with a ServiceNow instance, a third-party carrier application must have a script include that extends the base class ITAMShipmentIntegration script on its ServiceNow instance to receive the shipment tracking number from the customer's ServiceNow instance and respond with the carrier-related details.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Track shipments using the integration framework, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
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

![ITAMShipmentIntegration script include with ITAM processResponse function](../image/script-incl-sample-carrier.png "Sample ITAMShipmentIntegration script include with the default processResponse function provided by the IT Asset Management application")

![ITAMShipmentIntegration script include with custom processResponse function](../image/script-incl-custom-carrier.png "Sample ITAMShipmentIntegration script include with custom processResponse function")

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

**Parent Topic:**[Track shipments using the integration framework](tracking-shipments-using-integration-framework.md)

**Related topics**  


[Connect your ServiceNow instance with a shipping carrier application](../task/associate-shipping-carrier-int-profile.md)

[Remove a shipping carrier from an integration profile](../task/remove-shipping-carrier.md)

[Create a carrier integration profile](../task/create-carrier-integration-profile.md)

[View the carrier integration profile details](../task/view-integration-profiles.md)

[Test the integration with the carrier API](../task/test-carrier-api-integration.md)

[Create a shipping carrier record](../task/create-shipping-carrier.md)

[View hardware asset shipment details](../task/view-hardware-asset-shipments.md)

[Stale shipments](stale-shipments.md)

[Track a hardware asset shipment](../task/track-hardware-asset-shipments.md)

