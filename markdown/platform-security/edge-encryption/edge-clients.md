---
title: Edge Encryption clients
description: Edge Encryption uses three clients to inform the instance that the proxy is running, to synchronize requests between the proxy and the instance, and to forward all end user requests to the instance after any potential encryption.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption clients

Edge Encryption uses three clients to inform the instance that the proxy is running, to synchronize requests between the proxy and the instance, and to forward all end user requests to the instance after any potential encryption.

<table id="table_knz_253_cgb"><thead><tr><th>

Client

</th><th>

Description

</th></tr></thead><tbody><tr><td>

heartbeat/keepalive client

</td><td>

In charge of sending a request to the ServiceNow instance every 5 seconds to let the instance know that this proxy is up and running. The requests drive the last\_response\_on field on the Edge proxy table, and as a consequence drive the state of the proxy. If your system has issues sending the requests, or if the request or request processing is delayed, the instance may mark the proxy as unresponsive, even if the other clients \(including the one for user traffic\) are up and running.This client also controls the online status of the proxy on the instance.

 The **edgeencryption.proxy.keepalive.interval** property controls the polling rate for this client. The default is 5 \(seconds\).

</td></tr><tr><td>

polling/sync client

</td><td>

In charge of various requests the proxy sends to the instance to synchronize on the Edge Encryption configuration \(for example, which table, column, or attachment to encrypt, keys, jobs, rules, and tokenization patterns\).The **edgeencryption.config.poll.interval** property controls the polling rate for this client.

 **Warning:** Do not change this setting. Changing the default setting of the proxy poll interval may result in synchronization delays when updating Edge Encryption settings on the instance.

</td></tr><tr><td>

default/user traffic client

</td><td>

For everything else, this client handles all end user requests and forwards them to the ServiceNow instance after any potential encryption. This client also handles responses from the instance, forwarding them to the end user after any potential decryption.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Edge Encryption](../concept/c_EdgeEncryptionOverview.md)

