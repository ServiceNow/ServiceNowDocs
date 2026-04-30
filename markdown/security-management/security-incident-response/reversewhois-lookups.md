---
title: Reverse Whois integration
description: Reverse Whois is a service that performs searches on domain names registered by individuals or organizations.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Reverse Whois integration

Reverse Whois is a service that performs searches on domain names registered by individuals or organizations.

Perform domain lookups using search terms in observables that you attach to a security incident. The Reverse Whois API searches domain records based on search terms you enter, and it returns all records that correspond with those terms.

Analysts sometimes use this integration along with the Whois integration for security incident research. The Whois integration provides additional enrichment information based on the domain lookups from the Reverse Whois integration.

1.  [Install and configure Reverse Whois](../task/install-and-config-reversewhois.md)  
Before you run the integration on your instance, complete the installation and configuration steps so the Reverse Whois application properly integrates with the Security Operations product.
2.  [\(Optional\) Install and configure Whois](../task/whois-install-and-config.md)  
Install the Whois plugin to provide additional enrichment information on your domain lookups from the Reverse Whois API. This lookup provides additional enrichment data on the domain, such as the registration date, name of registrar, and country of origin.
3.  [Initiate lookup for Reverse Whois](../task/manually-attch-an-obsvrble-reversewhois.md)  
Initiate domain lookups using search terms in observables that you manually attach to a security incident record.
4.  [Verify expected results for Reverse Whois](../task/verify-expected-rslts-rvrsewhois.md)  
Enrichment results are displayed on the **ReverseWhois Domains** tab at the bottom of the security incident record. Locate the lookup results to verify that the lookup ran successfully.
5.  [\(Optional\) Run enrichment lookup and verify expected results for Whois](../task/verify-expected-results-for-whois.md)  
Run the Whois integration to perform enrichment lookups on the domains returned from the Reverse Whois integration.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

