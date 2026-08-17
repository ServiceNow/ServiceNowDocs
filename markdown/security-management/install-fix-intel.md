---
title: Install Fix Intelligence for Security Exposure Management
description: Activate the Fix Intelligence for Security Exposure Management plugin \(sn\_vul\_fix\) to add the Fix tables, role, and integration to your USEM environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/install-fix-intel.html
release: zurich
topic_type: task
last_updated: "2026-08-03"
reading_time_minutes: 2
keywords: [install Fix Intel, activate plugin, sn\_vul\_fix]
breadcrumb: [Fix Intelligence for Security Exposure Management, Integrations, Unified Security Exposure Management, Security Operations]
---

# Install Fix Intelligence for Security Exposure Management

Activate the Fix Intelligence for Security Exposure Management plugin \(`sn_vul_fix`\) to add the Fix tables, role, and integration to your USEM environment.

## Before you begin

Role required: admin

Prerequisites:

-   Unified Security Exposure Management and Vulnerability Response, including the Vulnerability Integration Framework, are active on your instance.
-   Your organization is entitled to Armis Centrix™ for Vulnerability Prioritization and Remediation \(ViPR\).

## About this task

Activate the Fix Intelligence for Security Exposure Management plugin to install the Fix tables \(`sn_vul_fix_intel` and its supporting tables\), the `sn_vul_fix.read` role, the ingestion scripts, and the registered integration.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  In the search field, enter the Fix Intelligence for Security Exposure Management plugin name.

    The plugin scope is `sn_vul_fix`.

3.  Select the plugin, and then select **Install**.

4.  When activation completes, confirm that the Fix tables and the `sn_vul_fix.read` role are present.

    For the full list of what the plugin installs, see [Components installed with Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/fix-intel-components-installed.md).


## Result

Fix Intelligence for Security Exposure Management is active. The Fix tables, role, and integration are installed on your instance.

## What to do next

Now Support configures the Armis Centrix™ for ViPR integration for your instance. Allow one to two business days after you install the plugin. If the integration is not configured after that time, raise a support case.

You must also configure inbound authentication. For more information, see [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3139883).

When the integration is configured and the first sync completes, you can review the ingested fixes. See [View fixes in USEM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/view-fixes-in-workspace.md).

**Parent Topic:**[Fix Intelligence for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/fix-intel-for-usem-landing.md)

