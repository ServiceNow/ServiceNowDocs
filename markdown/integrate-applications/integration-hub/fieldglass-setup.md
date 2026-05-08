---
title: Set up the SAP Fieldglass spoke
description: Integrate the ServiceNow instance and SAP Fieldglass account using API keys to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [SAP Fieldglass Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the SAP Fieldglass spoke

Integrate the ServiceNow instance and SAP Fieldglass account using API keys to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate SAP Fieldglass spoke.
-   Role required: admin

## Procedure

1.  Configure the connection and credential alias record for the SAP Fieldglass buyer instance.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the record, **SAPFieldGlassBuyer**.

    3.  Click the Create New Connection &amp; Credential related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Please Enter the Connection Information|
        |Name|Name to identify the connection record. For example, `SAP Fieldglass Buyer Connection`.|
        |Connection URL|URL of the SAP Fieldglass buyer instance.|
        |Please Enter the Credential Information|
        |Name|Name to identify the credential record. For example, `SAP Fieldglass Buyer Credential`.|
        |User name|User name to log in to your SAP Fieldglass buyer instance.|
        |Password|Password to log in to your SAP Fieldglass buyer instance.|
        |APIKey|API key of your SAP Fieldglass buyer instance.|

    5.  Click **Create**.

2.  Configure the connection and credential alias record for the SAP Fieldglass supplier instance.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    2.  Open the record, **SAPFieldGlassSupplier**.

    3.  Click the Create New Connection &amp; Credential related link.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Please Enter the Connection Information|
        |Name|Name to identify the connection record. For example, `SAP Fieldglass Supplier Connection`.|
        |Connection URL|URL of the SAP Fieldglass supplier instance.|
        |Please Enter the Credential Information|
        |Name|Name to identify the credential record. For example, `SAP Fieldglass Supplier Credential`.|
        |User name|User name to log in to your SAP Fieldglass supplier instance.|
        |Password|Password to log in to your SAP Fieldglass supplier instance.|
        |APIKey|API key of your SAP Fieldglass supplier instance.|

    5.  Click **Create**.

3.  Create flow to generate buyer token.

    1.  Navigate to **Flow Designer** &gt; **Designer**.

    2.  Create a flow and include the Get Buyer Token spoke action.

        For more information about creating flows, see Building flows.

    3.  Select the buyer credential record for **Credentials \[SAP Fieldglass Buyer Credentials\]**.

        ![Generate buyer token](../image/fieldglass-buyer-token.png)

    4.  Test the flow.

        After successful execution, these fields are auto-populated in the SAP Fieldglass Buyer credential record:

        -   **Access Token**: Access token is generated.
        -   **Token Status**: Status is set to **Active**.
        -   **Expiry**: Expiry date and time of the access token is displayed.
4.  Create flow to generate supplier token.

    1.  Navigate to **Flow Designer** &gt; **Designer**.

    2.  Create a flow and include the Get Supplier Token spoke action.

        For more information about creating flows, see Building flows.

    3.  Select the supplier credential record for **Credentials \[SAP Fieldglass Supplier Credentials\]**.

    4.  Test the flow.

        After successful execution, these fields are auto-populated in the SAP Fieldglass Supplier credential record:

        -   **Access Token**: Access token is generated.
        -   **Token Status**: Status is set to **Active**.
        -   **Expiry**: Expiry date and time of the access token is displayed.

