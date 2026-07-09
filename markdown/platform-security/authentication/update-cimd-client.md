---
title: Update a CIMD client
description: Update a registered Client ID Metadata Document \(CIMD\) client, including switching the metadata sync mode between Live and Static.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/update-cimd-client.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 2
keywords: [update CIMD client, edit CIMD client, metadata sync mode, switch Live Static, Live to Static, Static to Live]
breadcrumb: [CIMD client integration, Inbound Integrations, OAuth Inbound, OAuth authentication, Authentication, Access Management]
---

# Update a CIMD client

Update a registered Client ID Metadata Document \(CIMD\) client, including switching the metadata sync mode between Live and Static.

## Before you begin

Role required: `oauth_admin`

## About this task

After a CIMD client is registered, you can update its details or change how the instance keeps the client's configuration current by switching the metadata sync mode:

-   **Live \(Dynamic\)**

    The ServiceNow AI Platform refreshes the client configuration dynamically from the Client ID metadata. The metadata is cached and re-fetched when the cache expires \(default 1 hour, set by **Cache lifespan**\).

-   **Static \(Manual\)**

    The ServiceNow AI Platform pins the manually entered values and makes no automatic updates.


The sync mode you select determines which fields you maintain:

-   Switching to **Static** requires the **Client URI**, **Redirect URL**, and **Response Types** values, because the ServiceNow AI Platform no longer fetches them from the metadata.
-   Switching to **Live** lets the ServiceNow AI Platform fetch the **Client URI**, **Redirect URL**, and **Response Types** values from the Client ID metadata, so you don't maintain them manually.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **CIMD Clients**.

2.  Open the CIMD client you want to update from the **CIMD Registered Clients** list.

3.  Update the client fields as needed.

    For field descriptions, see the CIMD client fields reference in [Configure a CIMD client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/configure-cimd-client.md).

4.  To switch the sync mode, set **Metadata Sync Mode** to the value you want:

    -   **Live to Static** — set **Metadata Sync Mode** to **Static**, and then enter the **Client URI**, **Redirect URL**, and **Response Types** values. The instance stops fetching these values from the metadata and uses the values you enter.

    -   **Static to Live** — set **Metadata Sync Mode** to **Live**. The instance begins fetching the **Client URI**, **Redirect URL**, and **Response Types** values from the Client ID metadata and refreshes them as the cache expires.

5.  Select **Update**.


## Result

The CIMD client is updated. If you changed the sync mode, the instance applies the new mode the next time the client initiates an authorization flow.

