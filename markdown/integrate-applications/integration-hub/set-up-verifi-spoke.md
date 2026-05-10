---
title: Set up Verifi Spoke
description: Integrate the ServiceNow instance and Verifi account by using the JWT authentication to authenticate ServiceNow requests.Create a connection and credential record for the Verifi Spoke application. The Verifi Spoke connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Verifi Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Verifi Spoke

Integrate the ServiceNow instance and Verifi account by using the JWT authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Verifi spoke.
-   Role required: admin.

## About this task

JSON Web Tokens \(JWTs\) enable the capability to configure server-to-server API interactions between ServiceNow and external API providers without requiring any user intervention.

## Procedure

1.  Generate a JSON Web Token \(JWT\).

    Create a JWT for your instance by using this link to enable JWT authentication. For Verifi Spoke, generate the authorization by using the *VerifiAuthorizationTokenGenerator* script. For more information, see [Generate a JSON Web Token \(JWT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/Scoped-API-generate-JWT.md).

2.  Create credential records for the Verifi Spoke.

    Create a connection and credential record for the Verifi Spoke application. The Verifi Spoke connection and credential alias uses these credentials to authorize actions. For more information, see [Create a connection and a credential record for the Verifi Spoke](set-up-verifi-spoke.md#).


## Create a connection and a credential record for the Verifi Spoke

Create a connection and credential record for the Verifi Spoke application. The Verifi Spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

-   A shared secret for signing the authentication token.
-   Create a JSON Web Token \(JWT\) key. Associate a JWT provider with the signing configuration by referring to a JWT key.
-   An Issuer ID assigned by Verifi. The ID is included in the request headers and authentication token to identify the issuer making API calls.
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the **Verifi** record.

    The Connection &amp; Credential Aliases page opens.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the alias. An alias can only contain the alpha, number, and underscore characters.|
    |ID|Unique identifier for the Connections &amp; Credentials alias, based on the format `sn_verifi_spoke.Verifi`.|
    |Application|Application scope against which the Connection &amp; Credentials alias is assigned. The current session scope that you last selected in the application picker appears. For example, **Verifi Spoke** appears if it is the current scope for this session.|
    |Type|Alias type. Select **Connection and Credential**.|
    |Connection type|Name of the connection type, either Basic, HTTP, JDBC, JMS, or Kafka. The default is HTTP.|
    |Support Multiple Active Connections|Designator that indicates whether the alias supports multiple active connections. Add connections by using the Connections table and associate them to the alias by using the Connections related list.|
    |Default Retry Policy|Retry policy for the alias. For more information, see [Retry policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/retry-policy.md).|
    |Configuration Template|Configuration template to use to create a connection and credential record.|

4.  Select **Save**.

    The Connections and Connection Attributes related list appears.

    |Related List|Description|
    |------------|-----------|
    |Connections|Related connection records associated with this alias. After creating the alias, you can define the connection records and associate them with the alias. If **Support Multiple Active Connections** is selected, you can associate more than one connection with an alias.|
    |Connection Attributes|Attributes for the connection. Define the data that is specific to a connection and use it in an Integration Hub integration step.|
    |Child Aliases|Child aliases that are associated with the parent alias. After creating a connection and credential alias, you can create a child alias to configure multiple connections for the same application integration.|

5.  If you want to create a new credential and connection associated with your credential alias, under **Related Links**, select **Create New Connection &amp; Credential**.

    In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Please Enter the Connection Information|
    |Connection Name|Name of the connection.|
    |Connection URL|URL used for connecting to the server on which Verifi Spoke is installed.|
    |Issuer|An Issuer ID that you copied while setting up the Verifi Spoke by using the JWT authentication type.|
    |API Version|API version that the related spokes are built for. The default value is `4.0`.|
    |JWT Provider|JWT Provider that you provided while setting up the Verifi Spoke spoke by using the PAT authentication type.|

6.  If you want to create a child alias for your connection and credential alias, under the Child Aliases related list, select **New**.

    1.  Enter a name for the child alias and select **Submit**.

        The child alias inherits the properties from the parent alias. You can then configure a child alias to contain its own set of connection and credential information.


### Result

A connection and credential record is created in the ServiceNow instance.

