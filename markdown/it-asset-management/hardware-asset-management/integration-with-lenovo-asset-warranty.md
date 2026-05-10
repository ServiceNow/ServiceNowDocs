---
title: Integration with Lenovo for asset warranty details
description: The Lenovo Asset Warranty Flow enables you to get the warranty information of hardware assets by connecting to the Lenovo Warranty API.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Integration with Lenovo for asset warranty details

The Lenovo Asset Warranty Flow enables you to get the warranty information of hardware assets by connecting to the Lenovo Warranty API.

Integration with Lenovo has the following requirements:

-   The Hardware Asset Management application \(sn\_hamp\) must be activated.
-   The Lenovo Spoke \(sn\_lenovo\_spoke\) installed on your ServiceNow instance from the ServiceNow Store. For detailed information, see [Lenovo Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/lenovo-spoke.md).
-   The Client ID from Lenovo to connect to the Lenovo Warranty API.

    **Note:** If you don’t have a Client ID, contact your organization's Lenovo sales or service representative.

-   A Lenovo connection. If you don't have this connection, it must be created using the Lenovo \[sn\_lenovo\_spoke.Lenovo\] connection and credential alias. For more information, see [Connect to the Lenovo Warranty API](../task/connect-to-lenovo-api.md).

**Note:** For details on the input and response fields of the Lenovo Warranty API, see the "Warranty" topic in the Lenovo WebAPI documentation.

The process involved in fetching the asset warranty details from Lenovo is as follows:

1.  The Download Asset Warranty Information - Lenovo scheduled job that runs every week invokes the Lenovo Asset Warranty Flow that fetches all the hardware assets with the manufacturer as Lenovo.

    **Note:** The Download Asset Warranty Information - Lenovo scheduled job and the Lenovo Asset Warranty Flow are installed with the Hardware Asset Management \(sn\_hamp\) application.

2.  The Lenovo Asset Warranty Flow then invokes the Download Asset Warranty action that resides in the Lenovo Spoke application and passes 1000 serial numbers in a batch.
3.  The Download Asset Warranty action connects your ServiceNow instance to the Lenovo Warranty API by passing the serial numbers and the Client ID. This action also downloads the warranty information for all the serial numbers that are passed.
4.  The Process Warranty Information action in the Lenovo Asset Warranty Flow creates or updates asset warranty records in the Asset Warranty \[sn\_itam\_common\_asset\_warranty\] table using the response from the Lenovo Warranty API.

    The Asset Warranty \[sn\_itam\_common\_asset\_warranty\] table stores the asset warranty details. This table has fields corresponding to the Lenovo API response. Some of the fields of the table are:

    -   **External warranty ID**: Identifies the warranty records of an asset and update the warranty information.
    -   **Active**: Boolean field based on the **Warranty** field value of the Lenovo API response.
    -   **Status**: Indicates whether the warranty is active. This field is populated based on the **Active** field value.
    -   **Start Date** and **End Date**: Indicate the warranty period.

**Note:** Warranty records for excluded assets aren't fetched.

An asset can have multiple warranties associated with it. You can view the warranty information using the Asset Warranties tab on the asset form. You can also view all the asset warranty records from a central location using the Asset warranties list in the Asset operations view. For more information, see [Track the warranty details of your Lenovo assets](../task/view-asset-warranty-details.md).

**Related topics**  


[Receive asset warranty details from Lenovo](receive-warranty-details-lenovo.md)

