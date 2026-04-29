---
title: Authenticate an Edge Encryption proxy server
description: Specify that a proxy server is a trusted source so that Edge Encryption can process requests coming from that proxy server.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Authenticate an Edge Encryption proxy server

Specify that a proxy server is a trusted source so that Edge Encryption can process requests coming from that proxy server.

## Before you begin

If a proxy server is not authenticated, the console log includes the following message:

```
WARN This Edge Encryption proxy has not yet been authenticated by the instance.
Please navigate to the matching Proxy record on your ServiceNow instance and authenticate it.
```

If you attempt to access the proxy, you receive the following message: `This site can't be reached`.

To maintain the proxy in an operational state during the upgrade process, authentication is not required until after the proxy update is successful.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Proxies**.

2.  Select the proxy and click **Authenticate**.


## Result

The proxy moves from **Unauthenticated** to **Pending** to **Authenticated**. The status changes from **Unauthenticated** to **Pending** when you start the authentication. When authentication is complete, the status changes from **Pending** to **Authenticated**, and you can access the proxy and Edge Encryption can accept requests from the proxy.

**Note:** If you stop and restart the proxy, the proxy remains **Authenticated** and restarts successfully.

**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)

