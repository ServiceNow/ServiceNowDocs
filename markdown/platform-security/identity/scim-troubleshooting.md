---
title: SCIM Troubleshooting
description: Common errors that occur when you integrate with SCIM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/scim-troubleshooting.html
release: australia
product: Identity
classification: identity
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure SCIM for user provisioning with a provider, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# SCIM Troubleshooting

Common errors that occur when you integrate with SCIM.

## Invalid REST API URL

Action: Enter valid API URL. You can check the REST API URL in the **REST API Explorer**.

## No redirect URL is set in ServiceNow instance

Action: Enter valid Redirect URL for SCIM OAuth entity in ServiceNow. Enter redirect URL while you configure the OAuth entity in ServiceNow.

## When the redirect URL is different from the request

Action: ‘**redirect\_url**’ provided in ‘**Authorization Endpoint’** should be the same as the OAuth entity configured in ServiceNow.

**Note:**

This error occurs when there is a mismatch between Azure ‘Authorization Endpoint’ and ServiceNow ‘Redirect URL’

## When an invalid client secret is passed

Action: Value entered in ‘Client Secret’ should be the same as the OAuth entity configured in ServiceNow.

## When an invalid client ID is passed in Azure Authorization Endpoint

Action: Value entered for ‘client\_id’ parameter in ‘Authorization Endpoint’ must be the same as the OAuth entity configured in ServiceNow.

