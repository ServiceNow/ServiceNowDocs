---
title: Script include for third-party shipping carrier integrations
description: Before you can integrate the Enterprise Asset Management application with a third-party shipping carrier, that shipping carrier must create a script include that extends the base ITAMShipmentIntegration script. By extending this script, you can connect to the third-party shipping carrier application and retrieve shipment details in real-time.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing enterprise asset shipments, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Script include for third-party shipping carrier integrations

Before you can integrate the Enterprise Asset Management application with a third-party shipping carrier, that shipping carrier must create a script include that extends the base ITAMShipmentIntegration script. By extending this script, you can connect to the third-party shipping carrier application and retrieve shipment details in real-time.

## Structure of the ITAMShipmentIntegration script include

![ITAM Shipment Integration script include](../../hardware-asset-management/image/itam-integration-script.png)

## fetchShipmentInfo function

The fetchShipmentInfo function within the ITAMShipmentIntegration script include retrieves tracking numbers from your ServiceNow instance and then invokes the carrier API to fetch shipment details for those tracking numbers. To enable communication with the carrier API based on tracking numbers, the shipping carrier must define the corresponding business logic within the fetchShipmentInfo function. This function processes responses from the carrier API and then initiates the processResponse function.

## processResponse function

The processResponse function within the ITAMShipmentIntegration script include retrieves responses from the carrier API and then updates your shipment records with the following shipping carrier details:

-   Carrier link
-   Carrier status
-   Carrier status detail
-   Carrier pick-up date
-   Carrier delivered date
-   Currency
-   Delivery services cost
-   Parcel weight

**Important:** The IT Asset Management application automatically defines the business logic within this function. The business logic should not be modified.

**Parent Topic:**[Managing enterprise asset shipments](../concept/manage-shipments-eam.md)

