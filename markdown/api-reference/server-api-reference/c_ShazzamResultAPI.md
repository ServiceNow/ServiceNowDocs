---
title: ShazzamResult - Global
description: The ShazzamResult script include provides methods to encapsulate a Shazzam result.Property that shows if the IP address is activeProperty is true if this IP address is alive, which means no ports are open, but at least one responded.The Windows domain name for the IP.Host name for the IP.IP address of the results.A JavaScript array of ShazzamScanner instances.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ShazzamResult- Global

The ShazzamResult script include provides methods to encapsulate a Shazzam result.

Use this script include during the discovery scanning phase.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ShazzamResult - active

Property that shows if the IP address is active

|Name|Type|Description|
|----|----|-----------|
|active|Boolean|True if this IP address is active, which means at least one port is open.|

## ShazzamResult - alive

Property is true if this IP address is alive, which means no ports are open, but at least one responded.

|Name|Type|Description|
|----|----|-----------|
|alive|Boolean|True if the IP address is alive, meaning no ports are open, but at least one port responded.|

## ShazzamResult - domainName

The Windows domain name for the IP.

|Name|Type|Description|
|----|----|-----------|
|domainName|String|The Windows domain name for the IP if one was resolved by the scanner.|

## ShazzamResult - hostName

Host name for the IP.

|Name|Type|Description|
|----|----|-----------|
|hostName|String|Host name of the IP if one was resolved by the scanner.|

## ShazzamResult - ip

IP address of the results.

|Name|Type|Description|
|----|----|-----------|
|ip|String|IP address of the results|

## ShazzamResult - scanners

A JavaScript array of ShazzamScanner instances.

|Name|Type|Description|
|----|----|-----------|
|scanners|Array|Array of ShazzamScanner instances|

