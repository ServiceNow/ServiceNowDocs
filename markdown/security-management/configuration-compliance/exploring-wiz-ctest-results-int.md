---
title: Exploring the Wiz Test Results and Issues Integrations with Configuration Compliance
description: Import cloud configuration data with the Wiz Test Results and Issues Integrations with Configuration Compliance that are included with the Wiz Vulnerability Response Integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/configuration-compliance/exploring-wiz-ctest-results-int.html
release: brazil
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Exploring the Wiz Test Results and Issues Integrations with Configuration Compliance

Import cloud configuration data with the Wiz Test Results and Issues Integrations with Configuration Compliance that are included with the Wiz Vulnerability Response Integration.

## Wiz Test Results Integration

Import configuration test results from Wiz to detect non-compliant cloud configurations and help you enforce security policies and standards across your cloud environment.

Findings are mapped to cloud test results \(CTRs\) in the Configuration Compliance application.

**Note:** Prior to v1.1, host configurations from Wiz are not imported.

## Send AI security findings to AI security exposure management

If you have installed [AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/exploring-ai-security-exposure.md), you can import cloud configuration findings as Test Results into Configuration Compliance. See [Set filtering for the Wiz Test Results Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-response/wiz-test-result-tab-filters.md) for more information about configuring this feature. See [Exploring AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/exploring-ai-security-exposure.md) for more information about AI Security Exposure Management.

## Wiz Issues Integration

Import issues data from Wiz to help vulnerability managers, analysts, and cloud security and risk teams identify combinations of vulnerabilities that might reveal a potential attack path in your cloud infrastructure.

These findings are also mapped to CTRs with `Wiz Issues` labeled as the source in the Configuration Compliance application to help you track and remediate assets that may pose complex multi-vector risks.

For more information about the other integrations that are included with the Wiz Vulnerability Response Integration and installation and configuration steps, see [Understanding the Wiz Vulnerability Response Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/vulnerability-response/vr-wiz-exploring-host-cf.md).

