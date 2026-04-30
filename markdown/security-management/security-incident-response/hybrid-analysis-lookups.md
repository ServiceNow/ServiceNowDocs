---
title: Hybrid Analysis integration
description: The Hybrid Analysis application is part of an open online community in which users analyze files and URLs for threats. You share results and utilize research from the community for more effective incident responses. When integrated with the ServiceNow AI Platform Security Operations product, the shared threat intelligence provides you with additional insight into the severity of specific observables.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Hybrid Analysis integration

The Hybrid Analysis application is part of an open online community in which users analyze files and URLs for threats. You share results and utilize research from the community for more effective incident responses. When integrated with the ServiceNow AI Platform Security Operations product, the shared threat intelligence provides you with additional insight into the severity of specific observables.

The Hybrid Analysis integration performs threat lookups on the following observables:

-   File hashes
-   IP addresses
-   URLs

The flow checks for new observables as they arrive in security incidents. If the observables are of a type recognized by the API integration, the observables are evaluated. Observables determined to be malicious are tagged.

1.  [Install and configure](../task/install-and-configure-hybrid-analysis.md)  
Before you run the integration on your instance, complete the installation and configuration steps so the Hybrid Analysis application properly integrates with ServiceNow AI Platform Security Operations.
2.  [Verify expected results](../task/verify-expected-results-hybrid-analysis-.md)  
Observables are generated automatically by a security incident and scanned by the application. Locate the lookup results on the security incident to verify the threat lookup has run successfully. Also view raw data and run threat lookups on child observables.
3.  [\(Optional\) Manually attach an observable for Hybrid Analysis](../task/attach-an-observable-manually-hybrid-analysis.md)  
You can manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

