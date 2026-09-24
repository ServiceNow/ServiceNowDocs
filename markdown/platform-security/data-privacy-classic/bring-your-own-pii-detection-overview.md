---
title: Bring Your Own PII Detection Service
description: Integrate your organization's PII detection service to discover and mask sensitive data during AI inference calls. Routing your sensitive data inline guardrails to an external service allows you to comply with legal requirements around AI &amp; Data Governance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/bring-your-own-pii-detection-overview.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Data anonymization, Data privacy, Data Privacy, Platform Privacy]
---

# Bring Your Own PII Detection Service

Integrate your organization's PII detection service to discover and mask sensitive data during AI inference calls. Routing your sensitive data inline guardrails to an external service allows you to comply with legal requirements around AI &amp; Data Governance.

ServiceNow's Bring Your Own PII Detection Service feature enables organizations to connect their custom PII \(Personally Identifiable Information\) detection services to the ServiceNow Data Privacy module. Instead of relying solely on built-in detection patterns, you can configure external detection services to analyze data according to your organization's specific compliance requirements and detection rules.

**Important:** This capability does not apply to sensitive data sitting on the platform. Instead, it applies to ServiceNow Otto inline guardrails for detecting and masking sensitive data, which are part of Now Assist Guardian capabilities. To leverage this capability, you need a Data Privacy or ServiceNow Vault license.

The Bring Your Own PII Detection feature allows you to:

-   Configure one or more external PII detection services
-   Set a default external service configuration per channel
-   Test external service connections to verify functionality
-   Activate and deactivate external services without removing configurations
-   Manage multiple external detection services from a centralized home page

## Key concepts

The following concepts are fundamental to understanding and using the Bring Your Own PII Detection Service feature:

-   **External service configuration:** A connection definition that specifies the endpoint, credentials, and settings for your custom PII detection service.
-   **Channel:** A communication pathway through which PII detection requests are routed.
-   **Default configuration:** The external service configuration that is automatically used for a specific channel when no other configuration is explicitly selected.
-   **Service state:** Whether an external service configuration is active \(enabled for requests\) or inactive \(disabled from receiving requests\).
-   **Test functionality:** A mechanism to verify that your external service is responding correctly and can process PII detection requests as expected.

## Managing external services

The Bring Your Own PII Detection home page provides a centralized location for managing all configured external services. From this page, you can:

-   View a list of all external service configurations with their current status \(active or inactive\).
-   Create new external service configurations.
-   Edit existing configurations to update connection details or settings.
-   Test configurations to verify functionality.
-   Activate or deactivate services without permanently removing configurations
-   View detailed information about each service configuration in a side pane.

    The side pane provides additional details about a selected service, including its current state, channel associations, and configuration parameters.


## Best practices

-   **Test before production:** Always test external service configurations in a non-production environment before deploying to production.
-   **Monitor service health:** Regularly verify that your external detection service is responding correctly and processing requests within expected timeframes.
-   **Document configurations:** Maintain clear documentation of your external service configurations, including endpoint details and any custom detection rules.
-   **Set clear defaults:** Establish default configurations for each channel to ensure consistent PII detection behavior.
-   **Plan for failover:** Consider configuring backup external services if your PII detection requirements are critical to your operations.

## Requirements

To use the Bring Your Own PII Detection Service feature, you need:

-   A valid Data Privacy standalone license \(or ServiceNow Vault license\)
-   An external PII detection service endpoint \(URL and authentication credentials\)
-   Sufficient permissions to create and manage external service configurations
-   Knowledge of your external service's API contract \(request/response format\)

