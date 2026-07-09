---
title: Certificate tab
description: The Certificate tab is for generating or uploading the Discovery Console for OT certificate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/certificate-tab.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Settings page, Using the Discovery Console, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Certificate tab

The Certificate tab is for generating or uploading the Discovery Console for OT certificate.

## Console Certificate

The Console generates its own self-signed certificate bundle when initially deployed. The Certificate tab is for updating, generating, uploading, or downloading a Console Certificate.

On the Certificate tab you can select from the following actions.

-   Update the Certificate
-   Generate a New Bundle
-   Upload the Bundle \(.p12\)
-   Download the Certificate Bundle \(.zip\)

\[Omitted image "image.settings-certificate-download"\] Alt text: Console certificate

After you generate a New Bundle, you can select the link **Download Console Certificate Bundle \(.zip\)**. The bundle contains the Console's Collector Certificate Authority and the RabbitMQ certificate. These certificates establish trust between the Console and Collector and confirms their communications are secure and encrypted.

