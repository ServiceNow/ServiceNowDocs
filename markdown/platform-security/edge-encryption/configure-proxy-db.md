---
title: Configure the Edge Encryption proxy database
description: If using order-preserving encryption types or encryption patterns, you can optionally configure the Edge Encryption proxy database properties.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure the Edge Encryption proxy database

If using order-preserving encryption types or encryption patterns, you can optionally configure the Edge Encryption proxy database properties.

## Before you begin

Role required: admin

## About this task

To use order-preserving encryption types or encryption patterns, a MySQL database running in your network is mandatory. This task connects the proxy to the database, but it does not install or configure the database.

**Note:** If using multiple proxy servers, all proxy servers must use the same proxy database. The values entered in the installer must be the same for all proxy servers.

## Procedure

1.  Confirm or change the database URL, which is the location of the proxy database.

2.  In the **Name** field, enter the name of the proxy database.

    The default value is **edgeencryption**.

3.  Enter the username and password for accessing the proxy database.

4.  Click **Next**.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Previous topic:**[Update SSL certificate](update-ssl-certificate.md)

**Next topic:**[Launch the Edge Encryption proxy server](launch-proxy.md)

