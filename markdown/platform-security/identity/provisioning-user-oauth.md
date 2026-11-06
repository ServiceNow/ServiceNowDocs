---
title: Provision users using OAuth
description: Configure the provider for SCIM automatically provision and de-provision users and groups to ServiceNow by using the provider's provisioning service with OAuth.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/provisioning-user-oauth.html
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure SCIM for user provisioning with a provider, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Provision users using OAuth

Configure the provider for SCIM automatically provision and de-provision users and groups to ServiceNow by using the provider's provisioning service with OAuth.

## Before you begin

Role required: scim\_admin

**Warning:** Grant this role carefully. The scim\_admin role is equivalent to giving the user the admin role, where the scim\_admin can add or update Personally Identifiable Information \(PII\).

The SCIM plugin must be activated.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  In the Application Registries page, select the **SCIM API** record.

3.  Verify the **SCIM API** record details.

    These details should be provided while configuring the ServiceNow application on Microsoft Entra ID.

4.  Navigate to **All** &gt; **System Web Services** &gt; **REST API Access Policies** to check the details on the REST API Access Policies.

5.  In the API Access Policy page, click the **SCIM API Policy** record.

6.  Verify the **SCIMAPIOAuthOnly** record is available in the Authentication Profiles sections.

7.  Check if the **OAuth Entity** field is set to the **SCIM API** record that was earlier configured or verified as application registry.

8.  Create the required configurations at the provider's end.

9.  Test the connection to ensure that the provider can connect to ServiceNow.

    **Note:** If the connection fails, ensure that your ServiceNow account has admin permissions and try again.


