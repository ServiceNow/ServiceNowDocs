---
title: SCIM Troubleshooting
description: Common error scenarios integrating with SCIM.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial: Configure SCIM for user provisioning with a Provider, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# SCIM Troubleshooting

Common error scenarios integrating with SCIM.

## Invalid Rest API URL

Action: Enter valid API URL. Would be able to cross check the REST API URL in the **REST API Explorer**.

## No Redirect URL is set in ServiceNow instance

Action: Enter valid Redirect URL for SCIM OAuth entity in ServiceNow. Enter redirect URL while configure OAuth entity in ServiceNow.

## When Redirect URL is different than the request

Action: ‘**redirect\_url**’ provided in ‘**Authorization Endpoint’** should be same as the OAuth entity configured in ServiceNow.

**Note:**

This error occurs when there is a mismatch between Azure ‘Authorization Endpoint’ and ServiceNow ‘Redirect URL’

## When an invalid client secret is passed

Action: Value entered in ‘Client Secret’ should be same as the OAuth entity configured in ServiceNow.

## When an invalid ‘ClientId’ passed in Azure ‘Authorization EndPoint’

Action: Value entered for ‘client\_id’ parameter in ‘Authorization Endpoint’ has to be same as OAuth entity configured in ServiceNow.

