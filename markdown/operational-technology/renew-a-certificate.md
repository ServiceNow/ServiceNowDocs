---
title: Renew a certificate
description: This section describes how to renew a certificate on the Certificates page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/renew-a-certificate.html
release: australia
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [Certificates page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Renew a certificate

This section describes how to renew a certificate on the Certificates page.

## Before you begin

Role required: admin

## Procedure

1.  From the Certificates page, select the Renew Certificates button.

2.  The prompt window opens.

    The prompt reads: **The purpose of this renewal is to extend expiring certificates. It is NOT intended as a long-term solution. When renewing the certificate authority, verify all devices are turned on and connected.**

    \[Omitted image "renew-prompt-window.png"\] Alt text: Renew Certificates prompt

3.  Check the box next to either the Certificate Authority or the Server Certificate.

    For this example, the Certificate Authority is chosen.

4.  The **Certificate Authority Expires** appears with a pop-up calendar at the end of the line.

    \[Omitted image "renew-prompt-expiration-date.png"\] Alt text: Calendar pop-up

5.  The calendar opens for you to choose an expiration date.

6.  Once you have chosen a date, it appears in the window after the Certificate Authority.

    \[Omitted image "renew-prompt-expiration-date1.png"\] Alt text: Certificate Authority Expires

    **Note:** This renewal does not generate a new private key pair. The Console keeps track of old and the new certificates. To avoid issues, renew the Sensors and Collectors certificates at the same time. Renew all certificates at least 48 hours before the expiration date and verify that all devices are online to verify the automated retrieval occurs. After they are retrieved, there is a small interruption as the Sensor and Collectors restart to load the new certificates.


**Parent Topic:**[Certificates page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/certificates-page.md)

