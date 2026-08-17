---
title: Certificate tab
description: The Certificate tab is for generating or uploading the Discovery Console for OT certificate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/certificate-tab.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Settings page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Certificate tab

The Certificate tab is for generating or uploading the Discovery Console for OT certificate.

## Console Certificate

The Console generates its own self-signed certificate bundle when initially deployed. The Certificate tab is for updating, generating, uploading, or downloading a Console Certificate.

On the Certificate tab you can select from the following actions to update a Console Certificate:

-   Generate New Bundle.
-   Upload Bundle \(p12\).
-   Download the Certificate Bundle \(.zip\).
-   Renew Certificates.

\[Omitted image "cert-tab-renew1a.png"\] Alt text: Certificate tab on the Settings page

After you generate a New Bundle, you can select the link **Download Console Certificate Bundle \(.zip\)**. The bundle contains the Console's Collector Certificate Authority and the RabbitMQ certificate. These certificates establish trust between the Console and Collector and confirms their communications are secure and encrypted.

**Note:** For more information, see [Renew a certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/renew-a-certificate.md). The steps are similar but the Certificate tab only pertains to the Console Certificate.

**Parent Topic:**[Settings page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/settings-page-console.md)

