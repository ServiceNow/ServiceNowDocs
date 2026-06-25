---
title: Troubleshooting MISP integration
description: This section covers important troubleshooting tips that can help you resolve common issues you can encounter when setting up or running MISP integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/troubleshooting-misp-integration.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MISP administration, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Troubleshooting MISP integration

This section covers important troubleshooting tips that can help you resolve common issues you can encounter when setting up or running MISP integration.

## SSL issues

When connecting through the MISP integration, ensure that you’ve installed a valid CA certificate on the MISP server, which hasn’t expired. You can import RSA or your own certificates into the platform and ensure that the common name of the certificate matches the host name. For more information, see [Install and configure the MISP integration for Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/install-and-configure-misp.md) and [MISP user roles and permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/misp-user-roles-and-permissions.md).

**Parent Topic:**[MISP administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/misp-administration.md)

**Related topics**  


[Getting started with MISP integration for Security Operations]()

[Install and configure the MISP integration for Security Operations]()

[Review the MISP integration settings]()

[Configure MISP sighting searches]()

[Configure how an automatic event is created]()

[MISP event data]()

[Associated MISP events]()

[MISP user information]()

[Domain separation and MISP]()

