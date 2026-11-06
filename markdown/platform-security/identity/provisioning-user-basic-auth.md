---
title: Provision users using basic authentication
description: Configure SCIM to automatically provision and de-provision users and groups to ServiceNow by using the providers' provisioning service with basic authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/provisioning-user-basic-auth.html
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure SCIM for user provisioning with a provider, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Provision users using basic authentication

Configure SCIM to automatically provision and de-provision users and groups to ServiceNow by using the providers' provisioning service with basic authentication.

## Before you begin

Role required: scim\_admin

**Warning:** Grant this role carefully. The scim\_admin role is equivalent to giving the user the admin role, where the scim\_admin can add or update Personally Identifiable Information \(PII\).

The SCIM plugin must be activated.

## About this task

**Important:** Basic authentication is being prepared for future deprecation. Starting with the Brazil release, migrate your SCIM provisioning to OAuth 2.0, mutual TLS \(mTLS\), or federated token-based authentication. Basic authentication remains supported until a future release, subject to the restrictions described in the Basic authentication restriction topic. For guidance on identifying and migrating these integrations, see the [KB3220405](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220405) article.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST API Access Policies** to check the details on the REST API Access Policies.

2.  In the API Access Policy page, select the **SCIM API Policy** record.

3.  Verify the **SCIM API Basic Auth** record is available in the Authentication Profiles sections.

4.  Select **Basic Auth** as the Type.

5.  Create the required configurations at the provider's end.

6.  Test the connection to ensure that the provider can connect to ServiceNow.

    **Note:** If the connection fails, ensure that your ServiceNow account has admin permissions and try again.


