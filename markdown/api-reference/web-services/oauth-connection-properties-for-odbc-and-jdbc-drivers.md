---
title: OAuth connection properties for ODBC and JDBC drivers
description: Set these properties on the ODBC or JDBC driver to connect to Live Connect using OAuth instead of a username and password.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/oauth-connection-properties-for-odbc-and-jdbc-drivers.html
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [OAuth]
breadcrumb: [Reference, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# OAuth connection properties for ODBC and JDBC drivers

Set these properties on the ODBC or JDBC driver to connect to Live Connect using OAuth instead of a username and password.

## ODBC custom property keys

Add these keys as semicolon-separated key-value pairs along with the existing URL key. For the complete configuration procedure, see [Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-odbc-driver.md).

|Key|Description|
|---|-----------|
|UseOAuth|Set to true to connect using OAuth instead of a username and password.|
|OAuthClientId|Client ID from the OAuth Application Registry configured on your instance.|
|OAuthClientSecret|Client Secret from the OAuth Application Registry configured on your instance.|
|OAuthRefreshToken|Refresh token used to obtain new access tokens without re-authenticating.|

**Note:** If your OAuth client secret contains a semicolon, it can conflict with the semicolon delimited format of the custom properties string.

## JDBC driver properties

Configure these properties in your JDBC client's driver properties list, and the existing user and password properties.

**Note:** The location of driver properties varies by client application \(for example, DBeaver or Tableau\) but follows the standard JDBC specification. Look for Driver Properties, Advanced Properties, or Connection Properties in your client tool.

|Property|Description|
|--------|-----------|
|useoauth|Set to true to connect using OAuth instead of a username and password.|
|oauthclientid|Client ID from the OAuth Application Registry configured on your instance.|
|oauthclientsecret|Client Secret from the OAuth Application Registry configured on your instance.|
|oauthrefreshtoken|Refresh token used to obtain new access tokens without re-authenticating.|

**Parent Topic:**[Live Connect reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/troubleshooting.md)

