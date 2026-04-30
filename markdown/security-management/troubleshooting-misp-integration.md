---
title: Troubleshooting MISP integration
description: This section covers important troubleshooting tips that can help you resolve common issues you can encounter when setting up or running MISP integration.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [MISP administration, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Troubleshooting MISP integration

This section covers important troubleshooting tips that can help you resolve common issues you can encounter when setting up or running MISP integration.

## SSL issues

When connecting through the MISP integration, ensure that you’ve installed a valid CA certificate on the MISP server, which hasn’t expired. You can import RSA or your own certificates into the platform and ensure that the common name of the certificate matches the host name. For more information, see [Install and configure the MISP integration for Security Operations](../task/install-and-configure-misp.md) and [MISP user roles and permissions](misp-user-roles-and-permissions.md).

**Parent Topic:**[MISP administration](../concept/misp-administration.md)

**Related topics**  


[Getting started with MISP integration for Security Operations](get-started-with-misp-integration-for-security-operations.md)

[Install and configure the MISP integration for Security Operations](../task/install-and-configure-misp.md)

[Review the MISP integration settings](../task/review-the-misp-integration-settings.md)

[Configure MISP sighting searches](../task/configure-sightings-search.md)

[Configure how an automatic event is created](../task/configure-automatic-event-creation-profile.md#)

[MISP event data](../concept/misp-event-data.md)

[Associated MISP events](associated-misp-events.md)

[MISP user information](misp-user-information.md)

[Domain separation and MISP](domain-separation-and-misp.md)

