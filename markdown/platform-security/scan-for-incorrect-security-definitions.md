---
title: Scan for incorrect security definitions
description: Run the Auditor to scan your instance and find incorrect security definitions. It provides findings you can correct to help improve the security posture of your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/scan-for-incorrect-security-definitions.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Instance Security Center, Platform Security]
---

# Scan for incorrect security definitions

Run the Auditor to scan your instance and find incorrect security definitions. It provides findings you can correct to help improve the security posture of your instance.

**Important:**

Instance Security Center \(ISC\) has reached the end of sales as of September 2024, and is no longer supported or available for new activation.

ServiceNow Security Center \(SSC\) is the recommended solution going forward. For more information, see [Instance Security Center to ServiceNow Security Center migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-center-to-security-center-migration.md).

The Auditor performs a “full-body” assessment of your instance health that analyzes your system configuration. For security scans, it compares your current security configuration to best practice definitions, and to security property compliance values.

From an instance security standpoint, it provides insights and recommendations into what you should continue doing, and where you might be able to improve. These insights and recommendations help you answer the following questions:

-   Are the appropriate security-related properties set?
-   Is the High Security plugin enabled?
-   Do the right access control rules exist?

## Run the Auditor and analyze scan results

1.  To run the Auditor, click **Audit** on the Instance Security Center home page.
2.  When it completes, open Scan Results to review and analyze the security findings.
3.  To review the detail for a specific scan result, double-click the result number. This information includes its status, scan type, execution time, and error messages.
4.  Each of the Auditor findings contains resolution details, and a URL to product content about how to address them. Follow the documented guidelines to resolve the issues in each of the findings.

**Parent Topic:**[Instance Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-center.md)

**Related topics**  


[Instance Security Center to ServiceNow Security Center migration]()

[Monitor security events]()

[Check the daily compliance score and configure security property settings]()

[Monitor instance metrics]()

[Activate the ISC Virtual Agent interface]()

[Hardening settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/security-hardening-settings.md)

[Enable High Security Plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-high-security-plugin.md)

[Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md)

