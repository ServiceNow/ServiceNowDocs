---
title: RISKIQ and WHOISIQ integration
description: With the integration of RISKIQ and WHOISIQ APIs with the ServiceNow AI Platform Security Operations product, security analysts are provided with additional enrichment data and insight into the validity of websites.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# RISKIQ and WHOISIQ integration

With the integration of RISKIQ and WHOISIQ APIs with the ServiceNow AI Platform® Security Operations product, security analysts are provided with additional enrichment data and insight into the validity of websites.

The RISKIQ SSL Certificates API performs lookups on SSL Certificates, which include details on the issuing certificate authority, organizations who request certificates, the entity certificates are issued to, and the domain. SSL certificate lookups are performed automatically when security incidents are created.

The RISKIQ WHOISIQ API performs lookups on other observable types, such as domain, email, nameserver, organization, address, and phone number. URL and domain observables are enriched automatically when security incidents are created.

The integration requires the Security Incident Response and Threat Intelligence products.

1.  [Supported observables for RISKIQ and RISKIQ WHOISIQ](../reference/riskiq_supported_obsv.md)  
The RISKIQ API supports automatic SSL certificate lookups on IP address, file hash, Certificate Serial Number, domain, and URL observables. URL and domain observables are enriched automatically with the WHOISIQ API. For observable enrichment on other types of observables with the WHOISIQ API, create observables and run lookups manually from the Observables table.
2.  [Install and configure RISKIQ and WHOISIQ](../task/install-and-config-riskiq.md)  
Before you run the integration on your instance, complete the installation and configuration steps so the RISKIQ and WHOISIQ applications properly integrate with ServiceNow AI Platform Security Operations.
3.  [Verify expected results for RISKIQ SSL certificate lookups](../task/verify-expected-rslts-for-riskiq.md)  
When a security incident generates observables for URLs, domains, IP addresses, certificate file hashes \(SHA-1 fingerprint\), and certificate serial numbers, security incident analysts use the SSL certificate lookup results to verify sites have certificates that have been issued by a trusted public Certificate Authority \(CA\).
4.  [Verify expected results for WHOISIQ URL lookups](../task/verify-expctd-rslts-url-lookups-riskiq.md)  
When a security incident generates observables for URLs or domains, the WHOISIQ API performs the observable enrichment automatically upon security incident creation. The lookup results are displayed on the **Observable Enrichment Results** and **SSL Certificates** tabs on the security incident record.
5.  [Create an observable for manual WHOISIQ lookups](../task/manually-attch-obsv-whoisiq.md)  
Security incident analysts use information from observable enrichment with the WHOISIQ API to learn more about the email addresses, names, and phone numbers of organizations.
6.  [Verify expected results for manual WHOISIQ lookups](../task/verify-expected-rslts-whoisiq.md)  
Run a manual lookup on an observable when it does not automatically generate a security incident. For observable enrichment lookups using the WHOISIQ API for email addresses, organization names, phone numbers, or mailing addresses, initiate the lookup manually from the Observables table.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

