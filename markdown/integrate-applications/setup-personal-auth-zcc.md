---
title: Set up personal authentication for a connection
description: Configure a connection so that each user authenticates with their own credentials.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/setup-personal-auth-zcc.html
release: australia
topic_type: task
last_updated: "2026-11-11"
reading_time_minutes: 1
keywords: [personal authentication setup, per-user access, OAuth integration type Personal]
breadcrumb: [Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# Set up personal authentication for a connection

Configure a connection so that each user authenticates with their own credentials.

## Before you begin

Prerequisites:

-   The connector supports personal authentication. See [Supported connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/personal-auth-zcc.md).
-   A record exists in the Application Registries \[oauth\_entity\] table for your data source or identity provider service principal.

Role required: df\_connection\_admin

## About this task

Set the OAuth integration type of a connection to Personal so that each user authenticates with their own credentials. Users then see only the data they can access at the source.

## Procedure

1.  Start creating a connection for a connector that supports personal authentication.

2.  For the authentication method, select **OAuth**.

3.  Select **Access Token** as the OAuth credential type.

4.  Select the OAuth entity profile for your data source or identity provider service principal.

5.  Select **Personal** as the OAuth integration type.

6.  Select **Get OAuth Token** to open the authentication flow in a new browser tab and sign in.

7.  Select **Connect**.


## Result

Each user must authenticate with their own credentials before they can access data through the connection. For more information, see [Manage your personal access tokens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/personal-auth-zcc.md).

**Parent Topic:**[Managing zero copy connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/managing-connections-zcc.md)

