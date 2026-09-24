---
title: Configure OAuth for Veza in ServiceNow
description: Set up two application registries, their OAuth entity scopes and credentials, then link them to the pre-provided connection alias, so that AI Control Tower can authenticate to Veza using OAuth 2.0.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-veza-servicenow.html
release: brazil
topic_type: task
last_updated: "2026-09-08"
reading_time_minutes: 3
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure Veza access intelligence in the agent map, Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configure OAuth for Veza in ServiceNow

Set up two application registries, their OAuth entity scopes and credentials, then link them to the pre-provided connection alias, so that AI Control Tower can authenticate to Veza using OAuth 2.0.

## Before you begin

Confirm the following are in place:

-   The OAuth 2.0 client and OAuth 2.0 app you created in your Veza tenant, along with their client IDs and client secrets. See [Configure OAuth in Veza](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-oauth.md).

Role required: admin

## About this task

AI Control Tower uses two application registries on the ServiceNow platform: one configured with the client credential grant type for system-level access, and one configured with the authorization code grant type so that each AI steward can get their own per-user token. Each can link to the same pre-provided `SN AI Security Veza Connector` connection alias, but not at the same time.

**Important:** Set the refresh token lifespan to 2,592,000 seconds \(30 days\) on both application registries. This must match the refresh token expiration configured on the Veza side. If the ServiceNow value is longer than the Veza value, token refresh fails after the Veza-side token expires.

|Field|Client credential application registry|Authorization code application registry|
|-----|--------------------------------------|---------------------------------------|
|Client ID and client secret|From the Veza OAuth 2.0 client|From the Veza OAuth 2.0 app|
|Grant type|Client Credentials|Authorization Code|
|Authorization URL|Your Veza tenant's `/oauth/authorize` endpoint|Your Veza tenant's `/oauth/authorize` endpoint|
|Token URL|Your Veza tenant's `/oauth/token` endpoint|Your Veza tenant's `/oauth/token` endpoint|
|Redirect URL|Not applicable|Your instance URL followed by `/oauth_redirect.do`|
|Use PKCE|Clear the check box|Select the check box|
|Refresh token lifespan|2,592,000 seconds \(30 days\)|2,592,000 seconds \(30 days\)|

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registries** and create two new application registries using the values in the preceding table.

    ServiceNow automatically generates an OAuth entity profile for each application registry.

2.  On each generated OAuth entity profile, create an OAuth entity scope with the scope value `servicenow:aict:read`.

3.  Create an OAuth credential for each application registry.

    On the authorization code-based credential, set **Integration type** to **Personal** so that each AI steward authenticates with their own identity. The client credential-based credential doesn't expose this field; it's always System.

4.  On each OAuth credential record, select **Get OAuth Token** to verify that the credential can reach Veza.

    For the client credential-based credential, you don't need to do anything further — the token refreshes automatically. For the authorization code-based credential, you're redirected to log in to Veza and authorize access.

5.  Navigate to the pre-provided `SN AI Security Veza Connector` connection alias and link either or both credentials to the SN AI Security Veza Connector alias, one per connection. Only one connection can be **Active** at a time.

    Choose based on how you want AI stewards to authenticate:

    -   Set the connection linked to the client credential-based OAuth credential to **Active** so that all AI stewards share one system-level token. No AI steward needs to individually authenticate with Veza.
    -   Set the connection linked to the authorization code-based OAuth credential to **Active** so that each AI steward gets their own personal token. Each AI steward must select **Re-Authenticate** and log in to Veza before they can view access intelligence data. See [Discover your agent network with the map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-use-map.md).

## Result

OAuth is configured on the ServiceNow platform. Create the AI connection for Veza next. See [Create an AI connection for Veza access intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-create-ai-connection-veza.md).

**Parent Topic:**[Configure Veza access intelligence in the agent map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-access-intelligence.md)

