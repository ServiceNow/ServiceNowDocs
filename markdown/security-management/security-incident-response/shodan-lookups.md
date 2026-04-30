---
title: Shodan integration
description: Shodan is a search engine that analyzes service banner information from connected devices all around the globe. Service banners include information about a computer system, such as host name, device type, operating system, geographic location, and connected ISP. When integrated with the ServiceNow AI Platform Security Operations product, this service banner information provides analysts with additional enrichment data and insight for security incidents or investigations.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Shodan integration

Shodan is a search engine that analyzes service banner information from connected devices all around the globe. Service banners include information about a computer system, such as host name, device type, operating system, geographic location, and connected ISP. When integrated with the ServiceNow AI Platform Security Operations product, this service banner information provides analysts with additional enrichment data and insight for security incidents or investigations.

The integration requires the Security Incident Response and Threat Intelligence plugins.

The Shodan integration performs enrichment on the following observables:

-   IP addresses
-   URLs

The application checks for new observables every five minutes. If the observables are of a type recognized by the Shodan integration, the observables are enriched.

1.  [Install and configure](../task/install-and-configure-shodan.md)  
Before you run the integration on your instance, complete the installation and configuration steps so the Shodan application properly integrates with ServiceNow AI Platform Security Operations.
2.  [Verify expected results](../task/shodan-verify-expected-results.md)  
Observables are generated automatically by a security incident and scanned by the application. Enrichment results are displayed on the **Observable Enrichment Results** and **Network Banners** tabs.
3.  [\(Optional\) Manually attach an observable for Shodan](../task/manually-attach-an-observable-shodan.md)  
You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

