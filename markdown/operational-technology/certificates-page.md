---
title: Certificates page
description: The Certificates page lets you access data regarding your certificates, Sensor credentials, and Collector credentials.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/certificates-page.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Certificates page

The Certificates page lets you access data regarding your certificates, Sensor credentials, and Collector credentials.

On the Certificate page, you can do the following.

-   Generate a Certificate Authority.
-   Download the Certificate Bundle \(.zip\).
-   Generate a Sensor Bundle using a generated or user-submitted password.
-   Generate a Collector Bundle using a generated or user-submitted password. This bundle is generated using the specified bundle format.

The following image shows the Certificates page.

\[Omitted image "new-certificate-page.png"\] Alt text: Certificate page

## Certificate Authority

In the Certificate Authority section, you can generate a new certificate by choosing the expiration date and selecting **Generate CA**.

Select the **Download Certificate Bundle \(.zip\)** link to download the file containing the Console's Certificate Authority and the server certificate. The certificates establish trust between these applications and confirms their communications are secure and encrypted.

## Sensor Credentials

In the Sensor Credentials section, you can generate or submit a password for sensor credentials and then select **Generate Bundle**. The Sensor credentials are formatted in JSON.

**Note:** The Sensor certificate automatically renews when the Console certificate is renewed.

## Collector Credentials

In the Collector Credentials section, you can generate Collector credentials, generate a password bundle, and submit a bundle with either a ZIP file or a tar.gz \(tgz\) formatted file. Select the ZIP format for Window collectors and the tar.gz format for Linux collectors.

**Note:** The Collector credentials are formatted in JSON.

When ready, select **Generate Bundle**.

**Note:** The certificate for the Discovery Console for OT and the Discovery Sensor for OT automatically renews when it is within 30 days of its expiration date.

