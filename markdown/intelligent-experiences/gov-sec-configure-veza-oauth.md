---
title: Configure OAuth in Veza
description: Create an OAuth 2.0 client and an OAuth 2.0 app in your Veza tenant so that AI Control Tower can authenticate to Veza using OAuth 2.0 instead of an API key.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-veza-oauth.html
release: brazil
topic_type: task
last_updated: "2026-09-08"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure Veza access intelligence in the agent map, Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configure OAuth in Veza

Create an OAuth 2.0 client and an OAuth 2.0 app in your Veza tenant so that AI Control Tower can authenticate to Veza using OAuth 2.0 instead of an API key.

## Before you begin

Role required: Admin access to your Veza tenant

## About this task

AI Control Tower uses two separate Veza OAuth 2.0 credentials: an OAuth 2.0 client for the client credential grant, and an OAuth 2.0 app for the authorization code grant. Create the OAuth 2.0 client for system-level \(client credential\) access, and the OAuth 2.0 app for per-user \(authorization code\) access, or both if you want to switch between them later. For more information, see [Configure OAuth for Veza in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-servicenow.md).

## Procedure

1.  In your Veza tenant, navigate to **Administration** &gt; **API Keys**.

2.  Create a new **OAuth 2.0 client** for the client credential grant.

    Note the client secret when you create it. Veza doesn't show it again. Set the scope to `servicenow:aict:read`. For more information, see [OAuth2 clients](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/developers/api/authentication/oauth2-clients) in Veza documentation.

3.  Create a new **OAuth 2.0 app** for the authorization code grant.

    Set the base URL to your ServiceNow instance URL, allow any redirect URL, and set the scope to `servicenow:aict:read`. For more information, see [OAuth2 apps](https://docs.veza.com/4yItIzMvkpAvMVFAamTf/developers/api/authentication/oauth2-apps) in Veza documentation.


## Result

Note the client ID and client secret for both the OAuth 2.0 client and the OAuth 2.0 app. You need these values to configure OAuth on the ServiceNow platform. See [Configure OAuth for Veza in ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-servicenow.md).

**Parent Topic:**[Configure Veza access intelligence in the agent map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configure-veza-access-intelligence.md)

