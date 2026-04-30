---
title: Create an Identity Provider on your ServiceNow instance for Healthcare Operations Core
description: Set up an Identity Provider in your ServiceNow instance to enable OIDC for Healthcare Operations Core.
locale: en-US
release: yokohama
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Embedding Care Team Portal in Epic Hyperspace via Hyperdrive, Configuring Healthcare Operations Core, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Create an Identity Provider on your ServiceNow instance for Healthcare Operations Core

Set up an Identity Provider in your ServiceNow instance to enable OIDC for Healthcare Operations Core.

## Before you begin

Ensure that the com.snc.integration.sso.multi.installer plugin is installed on your instance.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Select **New**.

3.  Under What kind of SSO are you trying to create, select **OpenID Connect**.

4.  In the Import OpenID Connect Well-Known Configuration window, enter the following fields:

    -   Name – Enter a name for your Identity Provider \(for example, Epic OIDC\)
    -   Client ID – Input the Client ID created from your FHIR app on fhir.epic.com.
    -   Well-Known Configuration IRL – Enter `[https://fhir.epic.com/interconnect-fhir-oauth/api/FHIR/R4/.well-known/openid-configuration](https://fhir.epic.com/interconnect-fhir-oauth/api/FHIR/R4/.well-known/openid-configuration)`.

        **Note:** Verify this value with Epic as it may be different for your environment.

5.  Select **Import.**


## Result

An Identity Provider has been created based on the information provided by the well-known configuration.

