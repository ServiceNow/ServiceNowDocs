---
title: Set up the SuccessFactors spoke v3.x.x
description: Integrate the ServiceNow instance with your SuccessFactors spoke instance using basic credentials.Create Credential record for the OData APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the OData API.Create Credential record for the SOAP APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the SOAP APIs.Create a Connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.Create a Connection record for the SOAP API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.Customise the sample flows as per your requirement to synchronize data between your SuccessFactors and ServiceNow instances.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [SuccessFactors Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the SuccessFactors spoke v3.x.x

Integrate the ServiceNow instance with your SuccessFactors spoke instance using basic credentials.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the SuccessFactors spoke.
-   Enable these system properties:
    -   **glide.pf.rest.response\_payload\_max\_size**: The maximum value is, `10240`.
    -   **com.snc.process\_flow.reporting.serialized.val\_size\_limit**: The maximum value is, `16384`.
    -   **com.glide.transform.json.max-partial-length**: The maximum value is, `65536`.
-   Role required: admin.

**Note:** SuccessFactors will be deprecating basic authentication by Nov 2026 and hence, everyone must use OAuth SAML, which SuccessFactors spoke v4.10.0 supports.

-   If you are installing the SuccessFactors spoke for the first time, install SuccessFactors spoke v4.10.0. For more information about setting up SuccessFactors spoke v4.10.0, [Set up the SuccessFactors spoke v4.x.x](setup-successfactors.md#).
-   If you are using an earlier version of the SuccessFactors spoke, migrate to SuccessFactors spoke v4.10.0. For more information, see [Migrate to SuccessFactors spoke v4.10.0](migrate-successfactors.md).

## Create Credential record for the OData API

Create Credential record for the OData APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the OData API.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **Basic Auth Credentials**.

    A blank Basic Auth Credentials form displays.

4.  On the form, fill these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `SAPSF OData Credentials`.|
    |User name|User name with the OData API permission in this format: `<username>@<SAP-SuccessFactors-CompanyID>`.|
    |Password|Associated password.|
    |Active|Option to actively use the credential record.|
    |Order|Order to apply this credential. For example, enter `100`.|

5.  Click **Submit**.


### Result

The credential record to authorize actions using the OData API is created.

## Create Credential record for the SOAP API

Create Credential record for the SOAP APIs in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these credentials to authorize actions using the SOAP APIs.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **SuccessFactors SOAP Credentials**.

    A blank SuccessFactors SOAP Credentials form displays.

4.  On the form, fill these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `SAPSF Comp Emp Credentials`.|
    |User name|User name with the SOAP API permission.|
    |Password|Associated password.|
    |Active|Option to actively use the credential record.|
    |Order|Order to apply this credential. For example, enter `100`.|

5.  Click **Submit**.


### Result

The credential record to authorize actions using the SOAP API is created.

## Create Connection record for the OData API

Create a Connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **SuccessFactors OData API**, for example, **SuccessFactors\_Odata**.

3.  From the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  On the form, fill these values.

<table id="table_ol3_3nt_wkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `SF_REST`.

</td></tr><tr><td>

Credential

</td><td>

Credential record you created for the OData API. For example, `SAPSF OData Credentials`.

</td></tr><tr><td>

Connection URL

</td><td>

SuccessFactors service root URL. For example, `https://apisalesdemo4.successfactors.com/odata/v2`.**Note:** If you are using an SAP Cloud account, see [List of SAP SuccessFactors API Servers](https://help.sap.com/docs/SAP_SUCCESSFACTORS_PLATFORM/93f95815070049ebaaff042d8322d518/af2b8d5437494b12be88fe374eba75b6.html) in [SAP Help Portal](https://help.sap.com/docs/) to select the correct endpoint that is needed to target the API server.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection record.

</td></tr></tbody>
</table>5.  Click **Submit**.


### Result

The connection record for the OData API in SuccessFactors is created.

## Create Connection record for the SOAP API

Create a Connection record for the SOAP API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **SuccessFactors SOAP API**, for example, **SuccessFactors\_Comp\_Emp**.

3.  From the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  On the form, fill these values.

<table id="table_ol3_3nt_wkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, `SF_REST`.

</td></tr><tr><td>

Credential

</td><td>

Credential record you created for the SOAP API. For example, `SAPSF Comp Emp Credentials`.

</td></tr><tr><td>

Connection URL

</td><td>

SuccessFactors connection URL. For example, `https://salesdemo4.successfactors.com/sfapi/v1/soap`.**Note:** If you are using an SAP Cloud account, see [List of SAP SuccessFactors API Servers](https://help.sap.com/docs/SAP_SUCCESSFACTORS_PLATFORM/93f95815070049ebaaff042d8322d518/af2b8d5437494b12be88fe374eba75b6.html) in [SAP Help Portal](https://help.sap.com/docs/) to select the correct endpoint that is needed to target the API server.

</td></tr><tr><td>

Active

</td><td>

Option to actively use the connection record.

</td></tr></tbody>
</table>5.  In the **Attributes** tab, provide these fields.

    |Field|Description|
    |-----|-----------|
    |Company Id|Immutable Company ID of your SuccessFactors instance.|
    |Flow Timeout \(seconds\)|Maximum time in seconds up to which data can be received from SuccessFactors during the flow execution. If the time taken to retrieve data from SuccessFactors exceeds the timeout duration, the flow or subflow is cancelled. Default value is, `30`.|

6.  Click **Submit**.


### Result

The connection record for the SOAP API in SuccessFactors is created.

## Synchronize data between SuccessFactors and ServiceNow

Customise the sample flows as per your requirement to synchronize data between your SuccessFactors and ServiceNow instances.

### Todo entity

The SuccessFactors spoke provides sample flows to synchronize data bi-directionally for the todo entity. The sample flow, Run SuccessFactors Integration Flow can customised to retrieve data from SuccessFactors, while the Create Todo and Update Todo flows creates or updates the todo records in SuccessFactors when events occur in ServiceNow. While customising the sample flows, ensure that you provide appropriate triggers to retrieve and save future updates using transform maps.

### Other default entities

For these entities, the sample flow, Run SuccessFactors Integration Flow, can be customised to retrieve data from SuccessFactors:

-   Department
-   Location
-   Job Profile
-   Workers Profile
-   Effective Workers Profile
-   Job History Including Secondary Assignments

To create or update records in SuccessFactors for these entities when events occur in ServiceNow:

-   Create flows or subflows as per your choice or customise the sample flows and subflows.
-   Use Metadata Retrieval and Record Management actions in your flows.
-   Ensure that you provide appropriate triggers to retrieve and save future updates using transform maps.

### Other SuccessFactors entities

Depending on the SuccessFactors permissions and configurations, you can also synchronize data of other entities as per your requirement.

