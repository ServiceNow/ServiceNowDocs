---
title: Configure roles and authorizations for the OAuth user
description: Create a role in SAP and assign the required authorization objects to the OAuth system user to support OData service access and background job execution for integration with the Software Asset Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/configure-roles-auth-oauth-user.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
keywords: [OAuth user role, SAP authorizations, PFCG, OAuth SAP role]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Configure roles and authorizations for the OAuth user

Create a role in SAP and assign the required authorization objects to the OAuth system user to support OData service access and background job execution for integration with the Software Asset Management application.

## Before you begin

The OAuth client must be configured in SAP before assigning roles to the OAuth user. See [Configure an OAuth client in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/configure-oauth-client-sap.md).

SAP Role required: SAP Basis administrator

## About this task

Use transaction code **PFCG** to create a role and assign the authorization objects that grant the OAuth user access to OData services, background job scheduling, and OAuth scope management.

## Procedure

1.  Open transaction code **PFCG** in your SAP system.

2.  Enter a role name in the **Role** field and select **Create Single Role**.

    For example, `OAUTH_ROLE`.

3.  Add authorization object `S_SERVICE` and select the external service name `TADIR Service` in the **Type** field.

    \[Omitted image "sap-oauth-service.png"\] Alt text: Adding authorization object for external service and the type of service in SAP

4.  Add authorization object `S_BTCH_ADM` and select the **N \(No Administrator Authorization\)** option in the **Activities** field.

    \[Omitted image "sap-role-auth-admin.png"\] Alt text: Adding authorization object for administration and activities in the SAP

5.  Add authorization object `S_BTCH_JOB`, select **RELE \(Release Jobs\)** in the **Activities** field, and leave the **JOBGROUP** field empty.

    \[Omitted image "sap-role-auth-batch.png"\] Alt text: Adding authorization object for background jobs and activities in SAP

6.  Add authorization object `S_SCOPE` and enter **\*** in the **Activities** field.

    \[Omitted image "sap-config-oauth-scope.png"\] Alt text: Adding authorization object for OAuth scope

7.  Add authorization object `S_PROGNAM` and the following values in the corresponding fields.

    -   **P\_ACTION** — `BTCSUBMIT`
    -   **P\_PROGNAM** — `/NOW/SAMP_USER_PROG_BCKJOB_RUN`
    \[Omitted image "sap-config-oauth-prognam.png"\] Alt text: Adding authorization object for background jobs in SAP

8.  Save the role and assign it to the OAuth system user.

    For example, `OAUTH_USER`.


## Result

The OAuth user has the required authorizations to access OData services, run background jobs, and manage OAuth scopes for the integration.

## What to do next

Create an OAuth 2.0 SAP connection on your ServiceNow instance. For more information, see [Establish an SAP connection using OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/add-sap-connection-oauth.md).

