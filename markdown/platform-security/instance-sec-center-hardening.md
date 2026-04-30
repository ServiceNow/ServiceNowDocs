---
title: Check the daily compliance score and configure security property settings
description: Review the Daily Compliance Score metric and security configuration properties to see if your instance complies with the suggested security requirements. You can affect the daily compliance score by updating non-compliant security properties in the Hardening Compliance Configurations page.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Instance Security Center, Platform Security]
---

# Check the daily compliance score and configure security property settings

Review the Daily Compliance Score metric and security configuration properties to see if your instance complies with the suggested security requirements. You can affect the daily compliance score by updating non-compliant security properties in the Hardening Compliance Configurations page.

**Important:**

Instance Security Center \(ISC\) has reached the end of sales as of September 2024, and is no longer supported or available for new activation.

ServiceNow Security Center \(SSC\) is the recommended solution going forward. For more information, see [Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md).

The Daily Compliance Score is a percentage score. It is based on how compliant the current settings of your instance security properties are with the compliance values published in the [Hardening settings](../../security-center/reference/security-hardening-settings.md).

Review the daily compliance score of your instance regularly. Follow these guidelines when you are evaluating your daily compliance score:

-   Greater than or equal to 90% indicates that the instance is compliant with critical security controls.
-   Greater than or equal to 50% and less than 90% indicates a moderate level of security compliance.
-   Less than 50% indicates a low level of security compliance.

-   **[Adjust instance security settings to increase compliance](../task/update-security-hardening-params.md)**  
Using the Hardening Compliance Configuration page, harden and optimize non-compliant security properties that affect the daily compliance score of your instance. Its use ensures that your instance complies with the published security hardening standards, while fulfilling your company's security requirements.
-   **[How Daily Compliance score, trend, and graph data is refreshed](how-daily-compl-score-trend-date-refreshed.md)**  
Trend and graph data in the Instance Security Center is updated after the performance analytics job executes at 02:00 local time. It appears in the Daily Compliance Score tile, in the Event ribbon tiles, and in the Analytics Hub page detail when you click one of the event tiles.
-   **[PCI compliance score dashboard](../../../use/dashboards/application-content-packs/pci-comp-score-dashboard.md)**  
The PCI compliance score dashboard shows how your instance conforms to payment card industry \(PCI\) security standards. Use the dashboard to view your compliance score and modify your configuration to improve security.
-   **[PCI configuration controls score dashboard](../../../use/dashboards/application-content-packs/pci-config-controls-dashboard.md)**  
Use the PCI configuration controls score dashboard to review your PCI configuration and determine which security checks are non-compliant. You can change the configuration of the non-compliant security checks from the instance security center.

**Parent Topic:**[Instance Security Center](instance-security-center.md)

**Related topics**  


[Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md)

[Monitor security events](instance-sec-center-event-ribbon.md)

[Scan for incorrect security definitions](scan-for-incorrect-security-definitions.md)

[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)

[Activate the ISC Virtual Agent interface](../task/activating-virtual-agent-interface.md)

