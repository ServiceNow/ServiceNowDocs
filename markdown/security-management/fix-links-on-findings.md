---
title: Fix links on findings and vulnerabilities
description: Fix Intelligence for SEM adds a read-only Fix reference to vulnerable items and vulnerabilities, so you can see which fix resolves a given finding directly from the finding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/fix-links-on-findings.html
release: yokohama
topic_type: concept
last_updated: "2026-07-29"
reading_time_minutes: 1
keywords: [Fix reference, fix\_intel, vulnerable item, vulnerability]
breadcrumb: [Use, Fix Intelligence for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Fix links on findings and vulnerabilities

Fix Intelligence for SEM adds a read-only Fix reference to vulnerable items and vulnerabilities, so you can see which fix resolves a given finding directly from the finding.

When Fix Intelligence for SEM processes a sync, it links each fix to the findings it resolves. That link is surfaced as a read-only **Fix** reference field \(`fix_intel`\) on two existing Vulnerability Response tables:

-   **Vulnerable Item** \(`sn_vul_vulnerable_item`\): The finding record. Its **Fix** field points to the fix that resolves that finding.
-   **Remediation Task** \(`sn_vul_remediation_task`\): The remediation task record. When a remediation task rule groups findings by fix, the task shows the fix it addresses.

## Using the link

From a finding, open its **Fix** reference to see the remediation action, the other findings the fix resolves, and the assets it affects. You can also filter or group findings by whether they have a fix identified. To read a fix in Unified Security Exposure Management Workspace, see [View fixes in USEM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/view-fixes-in-workspace.md).

**Parent Topic:**[Using Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/using-fix-intel-security-exposure-management.md)

