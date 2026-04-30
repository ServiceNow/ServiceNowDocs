---
title: Setting up the ServiceNow University spoke
description: Connect ServiceNow University with Coaching with Learning to pull courses from ServiceNow University into your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ServiceNow University Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Setting up the ServiceNow University spoke

Connect ServiceNow University with Coaching with Learning to pull courses from ServiceNow University into your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the ServiceNow University spoke.
-   Role required: admin.

-   Integrate Coaching with Learning with ServiceNow University. For more information, see [External Content Integration Sources](https://www.servicenow.com/docs/access?context=integration-source-coaching-with-learning-coaching-wfo-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).
-   Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your spoke credentials.

    **Note:** You must have an ITSM Enterprise license subscription to get your spoke credentials.

-   For more information on OAuth Credentials, see [OAuth 2.0 credentials](https://www.servicenow.com/docs/access?context=oauth-2-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Connections&amp;Credentials** &gt; **Connections&amp;Credentials Aliases**.

2.  Select **ServiceNow University**.

3.  Select the **Create New Connection&amp;Credential** related link.

    The **Create Connection and Credential** form appears.

4.  Create the ServiceNow University connection.

    1.  On the form, fill in the fields.

<table id="table_ld3_smc_fbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Connection Information**

</td></tr><tr><td>

Connection Name

</td><td>

A unique name for the connection; for example, ServiceNow University Connection.

</td></tr><tr><td>

Connection URL

</td><td>

The ServiceNow server to retrieve the API information.**Default value**: [https://api.servicenow.com](https://api.servicenow.com).

</td></tr><tr><td>

API Version

</td><td>

Version of the connection URL to connect to the connection server.**Default value**: v1

</td></tr><tr><td>

Ocp-Apim-Subscription-Key

</td><td>

Encryption key for the ServiceNow University subscription. Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your encryption key.

</td></tr><tr><td colspan="2">

**OAuth Credential Information**

</td></tr><tr><td>

Credential Name

</td><td>

A unique name for the credential; for example, ServiceNow University Credential.

</td></tr><tr><td>

Token URL

</td><td>

On your web browser, enter: [https://ssosignon.servicenow.com/oauth2/ausxfcnusg830r7kp0x7/v1/token](https://ssosignon.servicenow.com/oauth2/ausxfcnusg830r7kp0x7/v1/token)This is the link to the OAuth server token endpoint.

</td></tr><tr><td>

Client Id

</td><td>

The Client ID of the application registered in the third-party OAuth server. Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your Client ID.

</td></tr><tr><td>

Client Secret

</td><td>

The Client Secret of the application registered in the third-party OAuth server. Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your client secret.

</td></tr><tr><td>

Username

</td><td>

User name to access the credential. Contact[nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your user name.

</td></tr><tr><td>

Password

</td><td>

Password to access the credential. Contact [nowlearningapi@servicenow.com](mailto:nowlearningapi_servicenow.com) to get your password.

</td></tr><tr><td>

Scope

</td><td>

Validates the ServiceNow University application programming interface \(API\) based on the parameters set in the application scope.**Default value:** openid email offline\_access

</td></tr></tbody>
</table>    2.  Select **Create and Get OAuth Token**.


## Result

The connection alias you've created appears in the Connection and Credentials related list.

**Important:**

-   You can only have one Connection in the Connections related list. If you are creating another connection, you must make the first one inactive.
-   The OAuth token also displays in the **ServiceNow University Spoke** &gt; **Credentials**. You can have only one active ServiceNow University credential. If you are creating another credential, you must make the first one inactive.

