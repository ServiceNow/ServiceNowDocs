---
title: PhishTank integration
description: PhishTank is a community-based phishing verification system into which users submit suspected threats, and other users in the system vote to determine whether the phishing threats are legitimate. When integrated with the ServiceNow AI Platform Security Operations product, the threat intelligence results provide analysts with additional insight into phishing-related security incidents or investigations.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# PhishTank integration

PhishTank is a community-based phishing verification system into which users submit suspected threats, and other users in the system vote to determine whether the phishing threats are legitimate. When integrated with the ServiceNow AI Platform Security Operations product, the threat intelligence results provide analysts with additional insight into phishing-related security incidents or investigations.

The PhishTank integration performs lookups on potential phishing site URLs.

The workflow checks for new observables as they arrive in security incidents. If the observables are of a type recognized by the API integration, the observables are evaluated. Observables determined to be malicious are tagged.

1.  [Install and configure PhishTank](../task/install-and-configure-phishtank.md)  
Before you run the integration on your instance, complete the installation and configuration steps so the PhishTank application properly integrates with ServiceNow AI Platform Security Operations.
2.  [Verify expected results for PhishTank](../task/verify-expected-results-phishtank.md)  
Observables are generated automatically by a security incident and scanned by the application. Lookup results are displayed on the Threat Lookup Results tab at the bottom of the security incident record.
3.  [\(Optional\) Manually attach an observable for PhishTank](../task/attach-an-observable-manually-phishtank.md)  
You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

