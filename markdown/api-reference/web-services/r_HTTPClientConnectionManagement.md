---
title: Manage connection pooling
description: Outbound HTTP\(S\) connections from a base system instance or inbound connections from MID Servers, the ODBC driver, and other clients are maintained and reused where possible.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Manage connection pooling

Outbound HTTP\(S\) connections from a base system instance or inbound connections from MID Servers, the ODBC driver, and other clients are maintained and reused where possible.

Connection pooling is used to keep track of HTTP\(S\) client connections to determine if they are alive and available for reuse.

ServiceNow HTTP client code means:

-   Any application or script which makes outbound HTTP\(S\) requests from a base system instance.
-   ServiceNow code in the MID Server or the ODBC driver which makes HTTP\(S\) requests to one or more base system instances.

**Note:** This discussion does not apply to browser-to-instance communication. No changes have been made with respect to the management of HTTP\(S\) connections for browser-based communication with ServiceNow. This discussion also does not apply to customer-developed Web Services clients making requests to ServiceNow.

## What Should the Customer Do?

Users should monitor performance, such as the decreased time for loading Discovery data and improved ODBC driver performance. For systems with an unusually large amount of simultaneous outbound HTTP\(S\) activity, such as numerous third-party integrations or high-volume automated activities which generate HTTP\(S\) requests from the base system instance to other places, review the `max_connections` and `max_connections_per_host` properties to ensure that the settings are sufficient. This enhancement has no impact on end-user connections from browsers and no impact on connections from customer-developed Web Services client applications.

-   **[HTTP Connection Management Properties](r_HTTPConnectionManagementProps.md)**  
Connection pooling is controlled by three properties.

**Parent Topic:**[Additional integration resources](../../outbound-web-services/concept/additional-integration-resources.md)

