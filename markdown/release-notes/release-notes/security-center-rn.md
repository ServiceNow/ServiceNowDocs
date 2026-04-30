---
title: Security Center release notes
description: The ServiceNow Security Center application is composed of multiple distinct tools designed to help you improve your security posture and strengthen your compliance with ServiceNow curated security recommendations. Security Center was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
---

# Security Center release notes

The ServiceNow® Security Center application is composed of multiple distinct tools designed to help you improve your security posture and strengthen your compliance with ServiceNow curated security recommendations. Security Center was enhanced and updated in the Xanadu release.

## Security Center highlights for the Xanadu release

-   Receive prompt notifications for user behaviors that you specify with the Security Event Notifications tool.
-   Monitor the security health of all your instances and take rapid action using the new Security posture dashboards.
-   Be prepared for potential future security announcements from ServiceNow with Security Banner Announcement capabilities.
-   ﻿﻿Schedule security scans with the updated Auditor Suite to monitor access control configurations in the Security Scanner tool.
-   Use the improved Security Center version 2.0 hardening tool to minimize data exposure within your instance.

See [Security Best Practices](https://www.servicenow.com/docs/access?context=security-best-practices-manager&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), [Customer Actions](https://www.servicenow.com/docs/access?context=critical-updates&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), and [Hardening settings baseline versions](https://www.servicenow.com/docs/access?context=hardening-settings-baseline&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), [Security Event Notifications](https://www.servicenow.com/docs/access?context=security-policies&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), and [Data Classification](https://www.servicenow.com/docs/access?context=data-classification-security-metrics&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Security Event Notifications](https://www.servicenow.com/docs/access?context=security-policies&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Receive prompt notifications on user behaviors that you specify with the Security Event Notifications tool. Users that you choose receive email notifications when a policy is triggered, enabling you to promptly remediate issues.

-   **[Security Posture Dashboards](https://www.servicenow.com/docs/access?context=scc-sec-posture-dashboard&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Monitor the security health of all your instances with the Security posture dashboards. The single instance dashboard provides graphical widgets for key security key process indicators \(KPIs\). The multi-instance dashboard, only available on production instances, shows the same KPIs for all instances in a table format. The dashboards can be cloned and then fully customized.

-   **[Security banner announcements](https://www.servicenow.com/docs/access?context=scc-banner&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Prepare for potential future security announcements from ServiceNow using the Security Banner Announcements. This feature enables ServiceNow to trigger new banners in customer instances that are visible to system administrators. These messages inform them of new and urgent potential security issues and include a link to more details.

-   **[Data Classification](https://www.servicenow.com/docs/access?context=data-classification-security-metrics&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Monitor your sensitive data with the Data Classification metrics in the Security Metrics tool. Updates to the tool include two new metrics. Classifiable Data metrics displays the amount of data that is available for classification and what portion has been already classified. The Classified Data metrics displays the breakdown of the classified data across your classification labels.

-   **[Security Center version 2.0 introduces a new set of hardening settings](https://www.servicenow.com/docs/access?context=hardening-settings-baseline&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Security Center version 2.0, introduced in the November store release, includes several new hardening settings, updates to existing ones, and the removal of some unnecessary settings. The new hardening settings come with recommended configurations to restrict access control lists \(ACLs\) for human resources apps, minimizing data exposure and enforcing the principle of least privilege. Additional settings help configure service portal widgets to reduce sensitive data exposure in tables, enforce strict code signing, and set role-based restrictions on apps. Several technical configuration names and descriptions have been updated for clarity, and outdated hardening settings have been removed.

-   **[Improved Security Center architecture](https://www.servicenow.com/docs/access?context=sec-center-v2&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    The Security Center has been redesigned to help admins understand what tasks they can accomplish with Security Center and to pick the right tools for their tasks.


## Changed in this release

-   **[Scan checks](https://www.servicenow.com/docs/access?context=scan-checks&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Schedule security scans with the updated Auditor Suite to monitor access control configurations in the Security Scanner tool. The Auditor Scan suite has been streamlined to contain only access control checks and renamed to Access Control Auditor Suite. The updated access control checks generate a smaller, more focused number of findings that reflect potential security vulnerabilities according to ServiceNow security experts.

-   **[Legacy workflows have been converted to Flow Designer workflows](https://www.servicenow.com/docs/access?context=sec-center-v2&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Legacy base system Workflows have been converted to modern Flow Designer workflows to standardize ServiceNow flows onto the modern technology. The updated low-code flows are designed to be more scalable and make updating and troubleshooting easier.


## Deprecations

Beginning with the ServiceNow AI Platform Xanadu release, ServiceNow will end support for Instance Security Center.

For details, see the [Deprecation Process](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article \(KB 0867184\) in the Now Support Knowledge Base.

## Activation information

Security Center v1.5 is installed by default with the Xanadu family release. Version 1.6 provides significant enhancements. To get Security Center v1,6, visit the [ServiceNow store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

