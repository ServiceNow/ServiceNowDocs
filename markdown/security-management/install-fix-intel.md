---
title: Install Fix Intelligence for Security Exposure Management
description: Activate the Fix Intelligence for Security Exposure Management plugin \(sn\_vul\_fix\) to add the Fix tables, role, and integration to your USEM environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/install-fix-intel.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [install Fix Intel, activate plugin, sn\_vul\_fix]
breadcrumb: [Fix Intelligence for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Install Fix Intelligence for Security Exposure Management

Activate the Fix Intelligence for Security Exposure Management plugin \(`sn_vul_fix`\) to add the Fix tables, role, and integration to your USEM environment.

## Before you begin

Role required: admin

Prerequisites:

-   Unified Security Exposure Management, Vulnerability Response, and the Unified Exposure Pipeline applications are active on your instance. Scanner integrations are configured using the Unified exposure pipeline. For information about the unified exposure pipeline, see [Unified Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/integrating-usem.md).

## About this task

Activate the Fix Intelligence for Security Exposure Management plugin to install the Fix tables \(`sn_vul_fix_intel` and its supporting tables\), the `sn_vul_fix.read` role, the ingestion scripts, and the registered integration.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  In the search field, enter the Fix Intelligence for Security Exposure Management plugin name.

    The plugin scope is `sn_vul_fix`.

3.  Select the plugin, and then select **Install**.

4.  When activation completes, confirm that the Fix tables and the `sn_vul_fix.read` role are present.

    For the full list of what the plugin installs, see [Components installed with Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/fix-intel-components-installed.md).


## Result

Fix Intelligence for Security Exposure Management is active. The Fix tables, role, and integration are installed on your instance.

