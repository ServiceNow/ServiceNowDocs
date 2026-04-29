---
title: Certificates page
description: The Certificates page lets you access data regarding your certificates, Sensor credentials, and Collector credentials.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Certificates page

The Certificates page lets you access data regarding your certificates, Sensor credentials, and Collector credentials.

The following image shows the Certificates page.

![Certificates page](../images/sensor-certificate-collector.png)

## Certificate Authority

In the Certificate Authority section, you can generate a new certificate by choosing the expiration date and selecting **Generate**.

![Generate a new CA](../images/generate-authority-certificate.png)

On the Certificate page, you can do the following.

-   Generate a Certificate Authority.
-   Generate a Sensor Credential bundle password or submit one.
-   Generate a Collector Bundle password or submit one and set up the bundle format.

## Sensor Credentials

In the Sensor Credentials section, you can generate or submit a password for sensor credentials and then select **Generate Bundle**.

**Note:** The Sensor certificate automatically renews when the Console certificate is renewed.

## Collector Credentials

In the Collector Credentials section, you can generate Collector credentials, generate a password bundle, and submit a bundle with either a ZIP file or a tar.gz \(tgz\) formatted file. Select the zip format for Window collectors and the tar.gz format for Linux collectors.

**Note:** The credentials are formatted in JSON.

When ready, select **Generate Bundle**.

**Note:** The certificate for the Discovery Console for OT and the Discovery Sensor for OT automatically renews when it is within 30 days of its expiration date.

