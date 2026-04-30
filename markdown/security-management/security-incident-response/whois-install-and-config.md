---
title: \(Optional\) Install and configure Whois
description: Install the Whois plugin to provide additional enrichment information on your domain lookups from the Reverse Whois API. This lookup provides additional enrichment data on the domain, such as the registration date, name of registrar, and country of origin.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reverse Whois integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Install and configure Whois

Install the Whois plugin to provide additional enrichment information on your domain lookups from the Reverse Whois API. This lookup provides additional enrichment data on the domain, such as the registration date, name of registrar, and country of origin.

## Before you begin

1.  If you have not requested entitlement for the application, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) for the Whois application from the ServiceNow Store.
2.  Obtain credentials for the Whois API key from the product website: [WHOIS API website](https://whoisapi.whoisxmlapi.com/).

Role required: admin

## Procedure

1.  If you have not installed the application, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  After the installation completes, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Whois API tile.

3.  Click **Configure**.

    ![A description of the app and the button used to initiate the configuration.](../images/whois-configure.png)

4.  In the **Whois API Configuration** dialog box, enter the API key you obtained from the product website.

    ![Reverse Whois API Configuration completed configuration](../images/reverse-config-9-4.png)

5.  Click **Submit**.

    Configuration is successfully completed unless an error message is displayed. You can now run enrichment lookups on the domains returned from the Reverse Whois integration.


If an error message is displayed, the API key may be invalid.

![Example configuration error message](../images/reverse-whois-config-error.png "Troubleshooting")

**Parent Topic:**[Reverse Whois integration](../concept/reversewhois-lookups.md)

**Previous topic:**[Install and configure Reverse Whois](install-and-config-reversewhois.md)

**Next topic:**[Initiate lookup for Reverse Whois](manually-attch-an-obsvrble-reversewhois.md)

