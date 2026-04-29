---
title: Edge Encryption components
description: Edge Encryption is composed of the Edge Encryption proxy server that runs on a server in your network, and the Edge Encryption plugin that must be installed on your ServiceNow instance. If using order-preserving encryption types or encryption patterns, a proxy database must also be installed in your network.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption components

Edge Encryption is composed of the Edge Encryption proxy server that runs on a server in your network, and the Edge Encryption plugin that must be installed on your ServiceNow instance. If using order-preserving encryption types or encryption patterns, a proxy database must also be installed in your network.

## Proxy application

When going through the Edge Encryption proxy server, the Edge Encryption plugin enables you to specify which fields, patterns, and attachments should be encrypted. You can also manage encryption rules to encrypt specific requests and can schedule mass encryption jobs.

## Proxy server

The Edge Encryption proxy server uses encryption rules to identify in an HTTP request what, if anything, must be encrypted and encrypts it before forwarding the request to the instance. For decryption, the Edge Encryption proxy server looks at the HTTP responses for any encrypted data and decrypts it before sending the response back to the client. For this decryption to happen, all HTTP requests and responses must go through the Edge Encryption proxy server. These HTTP requests include any requests originating from a browser, as well as any SOAP or REST requests.

## Proxy database

If using order preserving encryption or encryption patterns, your proxy servers rely on a MySQL database located in your network. All proxy servers in your network must use the same database.

The proxy database contains these tables.

|Name|Description|
|----|-----------|
|db\_id|Unique database ID|
|edge\_token\_map|Encryption pattern data|
|token\_map|Order-preserving encryption data|

## Backing up your proxy database

Because encryption patterns rely on tokenization, clear text values are stored in your proxy database. If the database is lost, clear text values can’t be restored. It’s critical that you maintain regular backups. To avoid data loss, back up your proxy database according to ServiceNow recommendations.

-   Back up your database every 24 hours.
-   Retain MySQL database binary log files for at least two days. After a backup has been restored, use the binary log to regenerate any data lost since the most recent backup.

**Parent Topic:**[Exploring Edge Encryption](c_EdgeEncryptionOverview.md)

