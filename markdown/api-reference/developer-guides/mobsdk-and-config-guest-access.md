---
title: Configure guest user access
description: To enable SDK services to be accessible by unauthenticated users, you must configure the Mobile SDK on your ServiceNow instance to allow guest user access. A guest user can view public web pages hosted in an instance using NowWeb, have a conversation as a guest using NowChat, access public data on the instance using NowTableService and NowGraphQLService, and access custom API services configured for unauthenticated users using NowAPIService.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Get started with Mobile SDK - Android, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Configure guest user access

To enable SDK services to be accessible by unauthenticated users, you must configure the Mobile SDK on your ServiceNow instance to allow guest user access. A guest user can view public web pages hosted in an instance using NowWeb, have a conversation as a guest using NowChat, access public data on the instance using NowTableService and NowGraphQLService, and access custom API services configured for unauthenticated users using NowAPIService.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Mobile SDK** &gt; **All** and select the application to which you want to allow guest access.

2.  For each service that you want to enable guest access, add `"allowGuestAccess":true` to its configuration array.

    **Note:** The NowAttachment service does not currently support guest access.

    ![Enable guest access](../../image/mobsdk-guest-access-config.png)

3.  Select **Update** to save your changes.


