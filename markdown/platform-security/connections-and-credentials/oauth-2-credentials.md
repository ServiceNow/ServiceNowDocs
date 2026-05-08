---
title: OAuth 2.0 credentials
description: OAuth 2.0 credentials enable ServiceNow to obtain access to user accounts on an HTTP service.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# OAuth 2.0 credentials

OAuth 2.0 credentials enable ServiceNow to obtain access to user accounts on an HTTP service.

These fields are available in the Credentials form for OAuth 2.0.

<table id="table_ezk_y3d_hbb"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential. For example, you might call it **OAuth2 credential**.

</td></tr><tr><td>

Active

</td><td>

Specify whether this credential is active.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

An OAuth profile is a combination of a grant type and at least one scope.

</td></tr><tr><td>

Connect to Auth Server via MID Server

</td><td>

Connects your ServiceNow instance to an on-premise OAuth server that resides behind a firewall through a MID Server. It can also connect your ServiceNow instance to a cloud-based OAuth server through a MID server. When this option is enabled, the request for an OAuth token is sent through the MID Server.**Important:**

-   The option appears when the value in the **Grant type** field in the OAuth Entity Profile is set to either**Client Credentials**, **Authorization Code**, or **Resource Owner Password Credentials**. To learn how to set an OAuth entity profile for a third-party OAuth provider, see [Connect to a third-party OAuth provider](../../../administer/security/task/connect-3rd-party-oauth-provider.md).
-   If you select the **Connect to Auth Server via MID Server** checkbox, you must identify the required MID Server or MID Servers from the **Applies to** list.

</td></tr><tr><td>

Applies to

</td><td>

Specify if the credential record is applicable for all MID Servers, or a specific MID Server. If specific, add the MID servers as necessary.

 **Important:**

Ensure that you are aware of these considerations if you have selected the **Connect to Auth Server via MID Server** check box.

-   Ensure that all the MID Servers selected in Applies to can communicate with the Auth server. This is required to execute the token request against the **Token URL** mentioned in the OAuth provider record \(that is linked to the OAuth entity profile specified in the OAuth 2.0 credential record\).![Token URL in the OAuth provider record.](../image/mid-server-access-token-url.png)
-   Ensure that there is at least one MID Server \(in the MID Servers selected in **Applies to**\) with these configurations:
    -   The value of the **Status** field is **Up**.
    -   The value of the **Validated** field is **Yes**.
    -   The capability of the MID Server is set to **REST** or **ALL**. To learn how to configure the MID server, see [https://www.servicenow.com/docs/access?context=configure-capabilities&amp;version=australia&amp;pubname=australia-integrate-applications&amp;ft:locale=en-US](https://www.servicenow.com/docs/access?context=configure-capabilities&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).![MID Server status.](../image/MidServerDashbardGaugeOAuth2.0.png)

To learn more about these statuses, see [MID Server dashboard](https://www.servicenow.com/docs/access?context=c_MIDServerDashboard&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).


</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

Credential alias

</td><td>

Specify the credential alias that you want to tie to the OAuth 2.0 credential.

</td></tr><tr><td>

Integration Type

</td><td>

Indicates the integration type for the credential. Invoke an API of a third-party with an OAuth request that generates an OAuth token that is system or user specific. Following are the integration types:-   **System**: Pull the token information based on the requester profile. The **System** integration type supports the following authentication mechanisms:
    1.  Security Assertion Markup Language \(SAML\)
    2.  JSON Web Token \(JWT\)
-   **Personal**: Pull the token information that is user-specific. The MID Server user must have the `oauth_admin` role. The **Personal** and **System** integration types support the following grant types:
    1.  Authorization Code
    2.  Resource Owner Password Credentials

 If this **Personal** is selected on the OAuth Requestor Profile page, an additional flag called as **Personal** is displayed.

 **Note:**

-   Any information that is related to a user can only be accessed with user-specific OAuth tokens with the Integration Type as **Personal**.
-   To use the session user-related token, you have to select the **Run As** filed in the Flow properties as **User who initiates session**.

</td></tr></tbody>
</table>