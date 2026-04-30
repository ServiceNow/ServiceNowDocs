---
title: Create an OAuth JWT API endpoint for external clients \(machine to machine integration\)
description: OAuth JWT bearer token enables the client web applications to authenticate with your instance seamlessly using the inbound JWT grant type instead of requiring the end user to manually log in or share the password.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Create an OAuth JWT API endpoint for external clients \(machine to machine integration\)

OAuth JWT bearer token enables the client web applications to authenticate with your instance seamlessly using the inbound JWT grant type instead of requiring the end user to manually log in or share the password.

## Before you begin

Generate a JSON Web Token \(JWT\) with the following claims at the client side:

-   `aud`: Must match the value of the Client ID.
-   `sub`: Must be a user identifier, such as the user's mail that you want to associate the token with.
-   `iss`: Recommended matching the value of the Client ID. If the `aud` and `iss` isn’t matching, then add the `iss` value in the claim validation.
-   `exp`: Any desired expiration.

![Example decoded JSON Web Token](../image/example-jwt.png "Example decoded JSON Web Token")

## Configuration in ServiceNow

## About this task

Since using the JWT grant type doesn’t include the password in the request, it enables a greater security between web services. For example, you can develop an external application and use tokens to authenticate inbound requests to your ServiceNow instance.

Role required: admin

For more information about JSON Web Tokens, see [https://jwt.io/](https://jwt.io/).

## Procedure

1.  Add the public key of the client app to the **sys\_certificate** table.

2.  Set up the configuration in your ServiceNow instance to verify the incoming JWT.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Select **Create an OAuth JWT API endpoint for external clients**.

    3.  Complete the form with information about your token.

<table id="table_jp5_ych_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique name that identifies the application that you require JWT OAuth access for.

</td></tr><tr><td>

Client ID

</td><td>

The auto-generated unique ID of the application. The system uses the value of this field to retrieve the public or shared key and validate the JWT. The value of this field should match the value of the issuer and audience claims in the JWT.

</td></tr><tr><td>

Client Secret

</td><td>

The shared secret string that both the instance and the client application or website use to authorize communications with one another. Leave this field empty to have the instance auto-generate a client secret. To display existing client secrets, select the lock icon.**Note:** If **Public Client** is selected, you can omit the **Client Secret**.

</td></tr><tr><td>

User Field

</td><td>

Field in the User \(sys\_user\) table that the system uses to match the value of the subject claim in the JWT. For example, if you add a token that has a subject claim value of user.name@example.com, then you would set the **User Field** to **Email**. This field tells the system to search the email field for the user.name@example.com value and use the matching user record in the inbound request.

</td></tr><tr><td>

Enable JTI Verification

</td><td>

Select to require a new token every token exchange. Default: Selected.

</td></tr><tr><td>

Application

</td><td>

Read-only application scope. This field is auto-populated.

</td></tr><tr><td>

Accessible from

</td><td>

Cross-scope access policy. For more information, see [Application access settings](https://www.servicenow.com/docs/access?context=c_ApplicationAccessSettings&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

Access Token Lifespan

</td><td>

Amount of time that the token is valid. Unit: Seconds

</td></tr><tr><td>

Token Format

</td><td>

Format of the token to generate. The format determines the structure of a token and the information it includes.

</td></tr><tr><td>

Subject Claim

</td><td>

Field in the User \(sys\_user\) table that's used to populate the value of the subject \(sub\) claim of a JWT token. The sub claim is a piece of information that identifies the subject, or user, of the JWT token. This field only applies if the **Token Format** is JWT.

</td></tr><tr><td>

Clock Skew

</td><td>

Allowed time difference between the server and client clocks when validating the `exp` and `nbf` claims in the JWT.Unit: Seconds

 Default: 300

</td></tr><tr><td>

Enforce Token Restrictions

</td><td>

Select to only enable tokens to be used with APIs set to enable the authentication profile. You can set grant access using an API access policy. For more information, see [Create REST API access policy](../../../integrate/authentication/task/create-api-access-policy.md).Default: Unselected.

</td></tr><tr><td>

Comments

</td><td>

Additional information to associate with the application.

</td></tr><tr><td>

Public Client

</td><td>

Add this field to the form if the JWT client is public. When selected, you don’t need to include a **Client Secret**.Default: Unselected.

</td></tr><tr><td>

Client Type

</td><td>

Choose the client type, based on the type of your client. Options:-   **iframe Embedded**
-   **Integration as a User**
-   **Integration as a Service**
To know more, see [Configure client type for OAuth and SSO records](../../../integrate/authentication/concept/client-type.md).

</td></tr></tbody>
</table>    4.  Save the form.

    5.  Add records to the JWT Verifier Maps related list to verify the JWT signature.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the JWT-mapping record.|
        |Kid|Key ID from the JWT.|
        |Shared Key|The shared key for the specified key ID.|
        |Application|Read-only application scope.|
        |Sys certificate|Certificate record in the X.509 Certificates \(sys\_certificate\) table. The certificate that was uploaded in step 1.|

    6.  Add any custom claims associated with your JWT to the OAuth JWT Claim Validations related list.

        You don’t need to add records for the following required claims:

        -   iss
        -   aud
        -   sub
        -   exp
        **Note:**

        -   If the `aud` and `iss` isn’t matching, then add the `iss` value in the claim validation.
        -   For certificates, you can add multiple verifier maps associated with multiple keys.
        |Field|Description|
        |-----|-----------|
        |My external client|Auto-populated with the OAuth JWT record.|
        |Claim Value Type|Data type of the claim value.|
        |Claim Name|Name of the claim you want to add.|
        |Claim Value|Value of the claim.|
        |Application|Read-only application scope.|

3.  Send a cURL request containing the JWT token to obtain an access token from your instance.

    The following is a sample cURL command requesting an access token:

    ```
    $ curl -d"grant_type= urn:ietf:params:oauth:grant-type:jwt-bearer
    &client_id=be3aeb583ace210011c15b24a43e25d8
    &client_secret=client_password
    &assertion= eyJraWQiOiJzYW1wbGVrZXlpZCIsInR5cCI6IkpXVCIsImFsZyI6IlJTMjU2In0.eyJhdWQiOiI5YzZlMmQxNzU0MzMyMDEwMDFhMTE4Y2FhMGVhMmE0MyIsInN1YiI6ImFkbWluQGV4YW1wbGUuY29tIiwiaXNzIjoiOWM2ZTJkMTc1NDMzMjAxMDAxYTExOGNhYTBlYTJhNDMiLCJleHAiOjE2MjI3MDI1MjYsImlhdCI6MTYyMjcwMjQ2NiwianRpIjoiNWRkMGUxYzctYjY1Ny00YmQ4LTlkY2UtMTdhZDdlZmUwNmFiIn0.PDoffnN2nq9ZNdxhOTLNbzlls4C1gsacahWr0kmPcGJDUJ_OQunmY5YXfpqkASiZixcQDS4kMwyqK9bha1-SnPOXq7zCIlJGCGFOv_OjEpQvMqmiKtLVk3jCsD03eXSoR4V-EzoCChiXpK87K5tMfM5k0YV9KfrxgvjUipgfni5N0JeyqkssMXBdkuE90XW_hBCo9AMMQm6J2PNMWb2O_O8rOX06KHuc4-Ip8wcRZ8a_bndCSmHl8Em7v4DvqTkLzlnF_-BXuM3T7nTI21cDXQKqZnqzzriu8irlAsscJFTxkh-_Ynei5RgYtL_Mvx2-HDO-XGofBhlAY2t9K36sz71HHqFZr5qCOIOAPguNzAy5-MOuZjOU_kH6ugIRycaNMDRjaU7gOvUHEERw3d0sI20OChIWOryBSwdTs7lgB1WzsJWCNVo81ssc2yko3jPoygt90tMwI_6A-4J-mlgq_fS_SvPUAqq_2UUJfVOTT5WGeq58cXfwRJmsDo49IhL3kXDVWT2gxaqhEdBQEW16UmRoTUzRs9A9sOm18y3skmOVtnEOm-MlJMFQZ754UMzbiH0ZsMmk1ivCGIjex5J0_lDjKElWF5RHGz3YShCoa4JKDZsqYMvIk1SvzyQXjuFqPdS2vzg2m1eKGUwr3m6uNs_HflcDystwVdMZ7nLlBG4"
    https://instancename.service-now.com/oauth_token.do
    ```

    If the JWT client is a public client, such as the Mobile SDK, then you can omit the client\_id and client\_secret parameters from the request. The following is a sample cURL command requesting an access token that omits the client\_id and client\_secret:

    ```
    $ curl -d"grant_type= urn:ietf:params:oauth:grant-type:jwt-bearer
    &assertion= eyJraWQiOiJzYW1wbGVrZXlpZCIsInR5cCI6IkpXVCIsImFsZyI6IlJTMjU2In0.eyJhdWQiOiI5YzZlMmQxNzU0MzMyMDEwMDFhMTE4Y2FhMGVhMmE0MyIsInN1YiI6ImFkbWluQGV4YW1wbGUuY29tIiwiaXNzIjoiOWM2ZTJkMTc1NDMzMjAxMDAxYTExOGNhYTBlYTJhNDMiLCJleHAiOjE2MjI3MDI1MjYsImlhdCI6MTYyMjcwMjQ2NiwianRpIjoiNWRkMGUxYzctYjY1Ny00YmQ4LTlkY2UtMTdhZDdlZmUwNmFiIn0.PDoffnN2nq9ZNdxhOTLNbzlls4C1gsacahWr0kmPcGJDUJ_OQunmY5YXfpqkASiZixcQDS4kMwyqK9bha1-SnPOXq7zCIlJGCGFOv_OjEpQvMqmiKtLVk3jCsD03eXSoR4V-EzoCChiXpK87K5tMfM5k0YV9KfrxgvjUipgfni5N0JeyqkssMXBdkuE90XW_hBCo9AMMQm6J2PNMWb2O_O8rOX06KHuc4-Ip8wcRZ8a_bndCSmHl8Em7v4DvqTkLzlnF_-BXuM3T7nTI21cDXQKqZnqzzriu8irlAsscJFTxkh-_Ynei5RgYtL_Mvx2-HDO-XGofBhlAY2t9K36sz71HHqFZr5qCOIOAPguNzAy5-MOuZjOU_kH6ugIRycaNMDRjaU7gOvUHEERw3d0sI20OChIWOryBSwdTs7lgB1WzsJWCNVo81ssc2yko3jPoygt90tMwI_6A-4J-mlgq_fS_SvPUAqq_2UUJfVOTT5WGeq58cXfwRJmsDo49IhL3kXDVWT2gxaqhEdBQEW16UmRoTUzRs9A9sOm18y3skmOVtnEOm-MlJMFQZ754UMzbiH0ZsMmk1ivCGIjex5J0_lDjKElWF5RHGz3YShCoa4JKDZsqYMvIk1SvzyQXjuFqPdS2vzg2m1eKGUwr3m6uNs_HflcDystwVdMZ7nLlBG4"
    https://instancename.service-now.com/oauth_token.do
    ```

    The instance returns the access token in its response:

    ```
    {
        "access_token": "KynMY2H0uwWkRc8g8YLXjnQxWbH5_wbnSiLsnaOoKw61GZkkV0ytZP74uF7hJyjfsWfaaFijqQzq2kcABNJxNA",
        "scope": "useraccount",
        "token_type": "Bearer",
        "expires_in": 1799
    }
    ```

    **Note:** The inbound JWT grant type doesn’t include refresh tokens.

4.  Make a REST API call to access a resource using the access token.

    The following is a cURL command to access the incident table using the token.

    ```
    $ curl -H "Authorization: Bearer KynMY2H0uwWkRc8g8YLXjnQxWbH5_wbnSiLsnaOoKw61GZkkV0ytZP74uF7hJyjfsWfaaFijqQzq2kcABNJxN" 
    https://instancename.service-now.com/api/now/v1/table/incident
    ```


## Result

The system retrieves the access token in the REST call and enables access to the requested resource.

