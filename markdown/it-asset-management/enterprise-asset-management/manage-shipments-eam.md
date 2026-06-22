---
title: Managing enterprise asset shipments
description: Track and manage your enterprise asset shipments in real-time by integrating the Enterprise Asset Management application with third-party shipping carriers using the IT Asset Management integration framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/enterprise-asset-management/manage-shipments-eam.html
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Managing enterprise asset shipments

Track and manage your enterprise asset shipments in real-time by integrating the Enterprise Asset Management application with third-party shipping carriers using the IT Asset Management integration framework.

\[Omitted image "itam-carrier-integration-eam.png"\] Alt text: Shipping carrier integration overview.

## Prerequisites

Before you can integrate the Enterprise Asset Management application with a third-party shipping carrier, the shipping carrier must complete the following prerequisites:

-   Enable cross scope access on their third-party application.
-   Create a script include that extends the base ITAMShipmentIntegration script so that you can connect to their third-party application and retrieve shipment details in real-time.
    -   The script include must be available in the IT Asset Management application scope. However, the Caller access isn't restricted and Accessible from fields must be available in All application scopes.
    -   Business logic must be implemented within the fetchShipmentinfo function to enable communication with the carrier API based on tracking numbers. The carrier API is required for connecting to the third-party application and for retrieving shipment details.
    -   The fetchShipmentinfo function must return a JSON object with the following HTTP response code and message:

        ```
        {
        httpResponseCode: 200, httpResponseMessage: ‘SUCCESS’
        }
        
        ```

    -   When the script include is in test mode, the shipping carrier invokes the carrier API to validate your connection to their third-party application. The shipping carrier can then either verify and return the response or query the shipments and invoke the processResponse function using the following response format:

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

        If the shipping carrier invokes the processResponse function, they must return the response after the function completes.

-   Create an integration profile with the appropriate name, carrier API details, and connection details. This integration profile enables you to connect to the third-party application so that you can retrieve shipment details.
-   If the third-party application uses the ServiceNow Credentials \[discovery\_credentials\] table or any other ServiceNow table with Password2 fields, provide a KMF access map policy to enable access to those tables. For more information on KMF access map policies, see [Password2 encryption with the Key Management Framework \(KMF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/platform-encryption/password-2way-encrypted-fields.md).

After the shipping carrier completes these prerequisites, you must complete these additional prerequisites:

-   If the integration profile contains connection details through a connection and credentials alias, update those details as needed so that you can successfully authenticate and connect to the carrier API.
-   Associate the shipping carrier with the integration profile.

-   **[Use Advanced Shipment Notification in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/asn-eam.md)**  
Use Advanced Shipment Notification \(ASN\) to automate and create enterprise asset records for when your assets are in transit.
-   **[Create a shipment carrier record in Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/create-shipment-carrier-record-eam.md)**  
Create a shipping carrier record in the Enterprise Asset Workspace to associate the carrier with an integration profile.
-   **[Script include for third-party shipping carrier integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/script-include-shipping-carrier-integrations-eam.md)**  
Before you can integrate the Enterprise Asset Management application with a third-party shipping carrier, that shipping carrier must create a script include that extends the base ITAMShipmentIntegration script. By extending this script, you can connect to the third-party shipping carrier application and retrieve shipment details in real-time.
-   **[Integrate with a third-party shipping carrier in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/integrate-shipping-carriers-eam.md)**  
Integrate the Enterprise Asset Management application with a third-party shipping carrier so that you can track the real-time status of your enterprise asset shipments.
-   **[View integration profiles for third-party shipping carriers in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/view-shipping-carrier-integration-profiles-eam.md)**  
View the integration profiles for your third-party shipping carriers in the Asset operations view of the Enterprise Asset Workspace. These integration profiles enable you to connect to third-party shipping carrier applications so that you can retrieve shipment details for your enterprise assets.
-   **[Associate a third-party shipping carrier with an integration profile in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/associate-shipping-carrier-integration-profile-eam.md)**  
Associate a third-party shipping carrier with an integration profile so that you can successfully connect to that shipping carrier.
-   **[Remove a third-party shipping carrier from an integration profile in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/remove-shipping-carrier-integration-profile-eam.md)**  
Remove a third-party shipping carrier that you no longer want to associate with an integration profile.
-   **[Test the integration profile for a third-party shipping carrier in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/test-shipping-carrier-integration-profile-eam.md)**  
Test the integration profile for a third-party shipping carrier so that you can mitigate any connection issues that arise.
-   **[View and add enterprise asset shipments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/view-enterprise-asset-shipments.md)**  
Use the Shipments list to view all active enterprise asset shipments from a central location. If an existing shipment doesn’t appear on the list, you can add it manually.

**Parent Topic:**[IT Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/it-asset-management.md)

