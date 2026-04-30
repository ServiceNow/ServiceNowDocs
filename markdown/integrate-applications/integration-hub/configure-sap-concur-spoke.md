---
title: Configure the SAP Concur spoke
description: Configure the SAP Concur spoke to integrate your ServiceNow instance with SAP Concur. After integration, you can create flows and automate actions on SAP Concur. For example, you can create a flow so that when a trigger occurs, it gets itinerary details based on the trip ID.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-03-13"
reading_time_minutes: 3
breadcrumb: [SAP Concur Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure the SAP Concur spoke

Configure the SAP Concur spoke to integrate your ServiceNow instance with SAP Concur. After integration, you can create flows and automate actions on SAP Concur. For example, you can create a flow so that when a trigger occurs, it gets itinerary details based on the trip ID.

## Before you begin

Role required: admin

## Procedure

1.  Configure the SAP Concur Event Subscription Service alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select Connections.

    3.  Turn on the Outbound tab.

    4.  In the Search all connections field, enter `SAP Concur`.

    5.  On the SAP Concur Event Subscription Service card, select **View Details**.

    6.  Select **Configure**.

    7.  Fill the form.

<table id="table_gtr_dkr_xyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection record. The default and read-only name of the first connection record is the SAP Concur Event Subscription Service. To create a record with your custom name, select **Add Connection**.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to SAP Concur APIs in the format `https://www-{region}.api.concursolutions.com`.

</td></tr><tr><td>

Version

</td><td>

API version.

</td></tr><tr><td>

Token URL

</td><td>

Token URL to get the OAuth token in the format `https://{region}.api.concursolutions.com/oauth2/v0/token.`

</td></tr><tr><td>

Client ID

</td><td>

Client ID generated on SAP Concur.**Note:** If you don't have the client ID, contact your SAP Concur SME.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret generated on SAP Concur.**Note:** If you don't have the client secret, contact your SAP Concur SME.

</td></tr></tbody>
</table>    8.  Select **Configure and get OAuth Token**.

        The OAuth token is generated and the connection record for the SAP Concur Event Subscription Service alias is created.

2.  Configure the SAP Concur v4 APIs alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select Connections.

    3.  Turn on the Outbound tab.

    4.  In the Search all connections field, enter `SAP Concur`.

    5.  On the SAP Concur v4 APIs card, select **View Details**.

    6.  Select **Configure**.

    7.  Fill the form.

<table id="table_tnk_2qr_xyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection record. The default and read-only name of the first connection record is the SAP Concur v4 APIs. To create a record with your custom name, select **Add Connection**.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to SAP Concur APIs in the format `https://{region}.api.concursolutions.com`.

</td></tr><tr><td>

Version

</td><td>

API version.

</td></tr><tr><td>

Token URL

</td><td>

Token URL to get the OAuth token in the format `https://{region}.api.concursolutions.com/oauth2/v0/token.`

</td></tr><tr><td>

Client ID

</td><td>

Client ID generated on SAP Concur.**Note:** If you don't have the client ID, contact your SAP Concur SME.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret generated on SAP Concur.**Note:** If you don't have the client secret, contact your SAP Concur SME.

</td></tr></tbody>
</table>    8.  Select **Configure and get OAuth Token**.

        The OAuth token is generated and the connection record for the SAP Concur v4 APIs alias is created.

3.  Configure the SAP Concur alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select Connections.

    3.  Turn on the Outbound tab.

    4.  In the Search all connections field, enter `SAP Concur`.

    5.  On the SAPConcur card, select **View Details**.

    6.  Select **Configure**.

    7.  Fill the form.

<table id="table_u5j_35r_xyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection record. The default and read-only name of the first connection record is the SAPConcur. To create a record with your custom name, select **Add Connection**.

</td></tr><tr><td>

Connection URL

</td><td>

URL to connect to SAP Concur APIs in the format `https://{region}.api.concursolutions.com`.

</td></tr><tr><td>

Token URL

</td><td>

Token URL to get the OAuth token in the format `https://{region}.api.concursolutions.com/oauth2/v0/token.`

</td></tr><tr><td>

Client ID

</td><td>

Client ID generated on SAP Concur.**Note:** If you don't have the client ID, contact your SAP Concur SME.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret generated on SAP Concur.**Note:** If you don't have the client secret, contact your SAP Concur SME.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

OAuth redirect URL in the format `https://<instancename>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>    8.  Select **Configure and get OAuth Token**.

        The OAuth token is generated and the connection record for the SAPConcur alias is created.


