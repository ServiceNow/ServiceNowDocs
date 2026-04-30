---
title: Manage observables
description: Observables are artifacts found on a network or operating system that are likely to indicate an intrusion. Typical observables are IP addresses, MD5 hashes of malware files or URLs, or domain names. Threat Intelligence observable table data is available from within a security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manage observables

Observables are artifacts found on a network or operating system that are likely to indicate an intrusion. Typical observables are IP addresses, MD5 hashes of malware files or URLs, or domain names. Threat Intelligence observable table data is available from within a security incident.

Observables information includes value, type, context, and timestamp.

You can create or delete observables manually or automatically through lookup requests.

A new **Finding** column has been added to the **Threat Lookup Results** tab. Possible values are: Malicious and Unknown.

-   If an IoC lookup request does not find a security incident observable, it is labeled Unknown.
-   If an IoC lookup request does find a security incident observable, it is labeled Malicious.

During an upgrade, existing items have the **Finding** column set to Malicious.

**Note:** While Threat Intelligence observables table data is part of a security incident, no other interaction with the Threat Intelligence module is included. For full threat functionality, the Threat Intelligence plugin is available by subscription.

**Related topics**  


[Create a security incident observable](../task/create-si-observable.md)

