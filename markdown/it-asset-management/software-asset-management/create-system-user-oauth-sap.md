---
title: Create a system user for OAuth authentication in SAP
description: Create a dedicated system user in SAP to serve as the OAuth 2.0 client ID for the Software Asset Management integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/create-system-user-oauth-sap.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
keywords: [SAP system user, OAuth authentication, SU01, SAP OAuth user]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a system user for OAuth authentication in SAP

Create a dedicated system user in SAP to serve as the OAuth 2.0 client ID for the Software Asset Management integration.

## Before you begin

The OData services must be activated and the system alias assigned before creating the OAuth system user. See [Activate OData services and assign a system alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/activate-odata-services-sap.md).

Role required: SAP Basis administrator

## About this task

Use transaction code **SU01** to create the system user. The system user is referenced as the OAuth client ID when configuring the OAuth client in the **SOAUTH2** transaction.

## Procedure

1.  Open transaction code **SU01** in your SAP system and create a user.

    For example, `OAUTH_USER`.

2.  Set the **User Type** value to **System**.

3.  Generate a password for the user and save it in a secure location.

    This password is required when configuring the OAuth client.

4.  Select **Save**.


## What to do next

Configure the OAuth client in SAP. For details, see [Configure an OAuth client in SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/configure-oauth-client-sap.md).

