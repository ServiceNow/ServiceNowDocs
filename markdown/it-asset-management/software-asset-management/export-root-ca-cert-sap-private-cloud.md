---
title: Export the Root CA certificate from SAP for Private Cloud
description: Export the Root CA certificate from your SAP system and upload it to your ServiceNow instance to establish a trusted HTTPS connection for SAP S/4HANA Cloud, Private Edition integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/export-root-ca-cert-sap-private-cloud.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 2
keywords: [SAP Private Cloud, Root CA certificate, STRUST, OAuth, SSL, S/4HANA]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management, Asset Management]
---

# Export the Root CA certificate from SAP for Private Cloud

Export the Root CA certificate from your SAP system and upload it to your ServiceNow instance to establish a trusted HTTPS connection for SAP S/4HANA Cloud, Private Edition integration.

## Before you begin

-   Confirm that you have the SAP Basis administrator role with authorization to access transaction STRUST.
-   Verify that you have administrator access to your ServiceNow instance to upload the certificate.

Role required: sam\_admin, SAP Basis administrator

## About this task

**Important:** This task is required for all SAP S/4HANA Cloud, Private Edition integrations, regardless of whether you use Basic Auth or OAuth 2.0 as the connection type.

The Root CA certificate establishes trust between your SAP system and the ServiceNow OAuth endpoint over HTTPS. Without this certificate, the SAP system can't verify the identity of the ServiceNow server during data collection.

## Procedure

1.  Export the certificate from SAP.

    1.  Log in to your SAP S/4HANA Private Cloud system using SAP log in details.

    2.  In the **command** field, enter transaction code `STRUST` and press **Enter**.

    3.  In the Trust Manager, expand **SSL Client \(Standard\)** in the left navigation panel.

        \[Omitted image "sap-export-cert-select-standard-ssl-client.png"\] Alt text: Standard SSL Client selected to expand.

    4.  Under Issuer Certificates, locate and select the respective Root CA certificate for the ServiceNow domain.

    5.  In the certificate details panel, select **Export certificate**.

        \[Omitted image "sap-export-root-cert.png"\] Alt text: Icon showing export certificate for root ca certificate.

    6.  In the **Export Certificate** dialog box, select **Base64** as the file format.

        \[Omitted image "sap-export-cert-select-file-format.png"\] Alt text: Dialog box showing two options for file format with Base64 radio button selected.

    7.  Enter a file path and file name for the exported certificate, then select **Save**.

        Save the file in a secure location. You will need it to import the certificate into the MID Server's cacerts keystore.

2.  Import the certificate into the MID Server's cacerts keystore.

    For steps to import, refer to [Add SSL certificates for the MID Server](https://www.servicenow.com/docs/r/servicenow-platform/mid-server/add-ssl-certificates.html).


## Result

The Root CA certificate is stored in your ServiceNow instance. The SAP S/4HANA Private Cloud system can now establish a trusted HTTPS connection to your ServiceNow instance during data collection.

## What to do next

After uploading the certificate, select SAP clients to import data. For more information, see [Select SAP clients to import data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/select-sap-clients-import.md).

**Parent Topic:**[Set up SAP integration to establish a connection with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/setup-sap-integration.md)

