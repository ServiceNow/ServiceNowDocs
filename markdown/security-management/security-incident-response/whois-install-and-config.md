---
title: \(Optional\) Install and configure Whois
description: Install the Whois plugin to provide additional enrichment information on your domain lookups from the Reverse Whois API. This lookup provides additional enrichment data on the domain, such as the registration date, name of registrar, and country of origin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/whois-install-and-config.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reverse Whois integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Install and configure Whois

Install the Whois plugin to provide additional enrichment information on your domain lookups from the Reverse Whois API. This lookup provides additional enrichment data on the domain, such as the registration date, name of registrar, and country of origin.

## Before you begin

1.  If you have not requested entitlement for the application, see [Get entitlement for a Security Operations product or application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/entitle-secops-product.md) for the Whois application from the ServiceNow Store.
2.  Obtain credentials for the Whois API key from the product website: [WHOIS API website](https://whoisapi.whoisxmlapi.com/).

Role required: admin

## Procedure

1.  If you have not installed the application, see [Install a Security Operations integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-operations/install-non-core-apps.md) and follow the steps to install it.

2.  After the installation completes, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Whois API tile.

3.  Select **Configure**.

    \[Omitted image "reverse-whois-config-tile.png"\] Alt text: A description of the app and the button used to initiate the configuration.

4.  In the **Whois API Configuration** dialog box, enter the API key you obtained from the product website.

    \[Omitted image "reverse-config-9-4.png"\] Alt text: Reverse Whois API Configuration completed configuration

5.  Select **Submit**.

    Configuration is successfully completed unless an error message is displayed. You can now run enrichment lookups on the domains returned from the Reverse Whois integration.


If an error message is displayed, the API key may be invalid.

\[Omitted image "reverse-whois-config-error.png"\] Alt text: Example configuration error message

**Parent Topic:**[Reverse Whois integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/reversewhois-lookups.md)

**Previous topic:**[Install and configure Reverse Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/install-and-config-reversewhois.md)

**Next topic:**[Initiate the lookup for Reverse Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/manually-attch-an-obsvrble-reversewhois.md)

