---
title: Authentication Algorithms
description: Verify the identity of the sender using Authentication Algorithms
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Connections and Credentials, Access Management]
---

# Authentication Algorithms

Verify the identity of the sender using Authentication Algorithms

Allow integration steps to authenticate with web services that require complex or non-standard connection or credential mechanisms. Associate authentication algorithms to credential and connection aliases to reduce or eliminate the need to manually configure integration steps.

You can use an authentication algorithm to generate custom authentication data for your integration steps. Integration steps can use this dynamic data to create any custom artifacts necessary to authenticate with the target web service. For example, a REST step could create an authentication header, query parameters, or a token.

Authentication algorithms support the following steps:

-   Get Connection Info Step
-   REST Step
-   SOAP Step

For more information, see [Integration steps](https://www.servicenow.com/docs/access?context=integration-steps&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

## Authentication algorithm types

-   **Amazon Signature Version 4**: This is a pre-built authentication algorithm to connect to Amazon Web Services.
-   **Custom Authentication**: This is a template that developers can use to create their own authentication algorithms.

To know more, on how to configure the authentication algorithm, see [Configure an authentication algorithm](../task/configure-authentication-algorithm.md).

## Scripts

Instance Authentication Scripts are on instance scripts part of **sys\_script\_include** table.

| | |
|---|---|
|RequestAuthInternal|Read only script on instance, which supports generating AWS V4 signature or custom authentication that is sent with outbound request.|
|RequestAuthAWSV4Signer|Script extending RequestAuthInternal to implement signer to generate AWS V4 signature.|
|RequestAuthTwitterSigner|Script extending RequestAuthInternal to implement signer to generate Twitter signature using OAuth 1.0a.|
|RequestAuthSampleCustomSigner|Sample script extending RequestAuthInternal to understand how to write custom signer on instance.|

MID Authentication Scripts are on MID scripts part of **ecc\_agent\_script\_include** table.

| | |
|---|---|
|RequestAuthInternal|Read only script on MID, which supports generating AWS V4 signature or custom authentication that is sent with outbound request.|
|RequestAuthAWSV4MIDSigner|Script extending RequestAuthInternal to implement signer to generate AWS V4 signature.|
|RequestAuthTwitterSigner|Script extending RequestAuthInternal to implement signer to generate Twitter signature using OAuth 1.0a.|
|RequestAuthSampleMidCustomSigner|Sample script extending RequestAuthInternal to understand how to write custom signer on MID.|

## JavaScript API's

Following are the JavaScript API's for authentication algorithm.

-   [AuthCredential](https://developer.servicenow.com/dev.do#!/reference/api/utah/server/sn_auth-namespace/AuthCredentialAPI)
-   [HttpRequestAuthedData](https://developer.servicenow.com/dev.do#!/reference/api/utah/server/sn_auth-namespace/HttpRequestAuthedDataAPI)
-   [HttpRequestData](https://developer.servicenow.com/dev.do#!/reference/api/utah/server/sn_auth-namespace/HttpRequestDataAPI)
-   [RequestAuthAPI](https://developer.servicenow.com/dev.do#!/reference/api/utah/server/sn_auth-namespace/RequestAuthAPI)

