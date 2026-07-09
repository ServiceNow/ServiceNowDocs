---
title: Configure the HL7 FHIR connection and credentials
description: Bind the FHIR server URL and OAuth credentials to the shared HL7 FHIR Connection &amp; Credential Alias so that all eight spoke actions can authenticate to and read from your FHIR R4 server.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 2
keywords: [connection, credential alias, OAuth, FHIR server]
---

# Configure the HL7 FHIR connection and credentials

Bind the FHIR server URL and OAuth credentials to the shared `HL7 FHIR` Connection &amp; Credential Alias so that all eight spoke actions can authenticate to and read from your FHIR R4 server.

## Before you begin

Role required: admin

You need the following from your FHIR server administrator: the FHIR R4 server base URL, the OAuth authorization, token, and revoke-token endpoint URLs, and the OAuth client ID and client secret registered for your instance.

## About this task

The spoke ships a Connection &amp; Credential Alias named `HL7 FHIR` with an attached configuration template named `FHIR Connection Configuration`. The template adds a guided **Add Connection** action to the alias that creates the HTTP connection and an OAuth 2.0 credential in one step. The OAuth client credentials and the FHIR server URL ship empty — you supply them through the guided setup. All eight actions share this single alias.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** and open the **HL7 FHIR** alias.

2.  On the alias record, click **Add Connection** to open the guided `FHIR Connection Configuration` setup form.

3.  Enter the connection details: a **Connection Name**, the **Connection URL** \(your FHIR R4 server base URL — host and protocol only, over HTTPS\), and the **API version**.

    Leave **API version** at the default `baseR4` unless your FHIR server uses a different R4 URL fragment. This value populates the `api_version` connection attribute that every action appends to the base URL.

4.  Enter the OAuth credential details supplied by your FHIR server administrator: **OAuth Name**, **OAuth Client ID**, **OAuth Client Secret**, and **OAuth Token URL**.

    The guided setup creates an OAuth 2.0 credential \(`FHIR Spoke Credential`\) and application registry \(`FHIR Spoke OAuth`\) that use the authorization code grant with PKCE \(`S256`\).

5.  Save the connection, then complete the OAuth authorization to obtain an access token.

6.  Use the alias **Test Connection** action to verify that the instance can authenticate to and reach the FHIR server.


## Result

All eight HL7 FHIR Spoke actions can now authenticate to your FHIR server through the shared alias. To add a stream action to a flow, see [Add a FHIR stream action to a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

