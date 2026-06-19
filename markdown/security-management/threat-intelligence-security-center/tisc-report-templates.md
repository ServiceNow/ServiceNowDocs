---
title: About Report Templates in TISC
description: Report templates in TISC help you generate standardized reports for cases and threat intelligence investigations. Use these templates to track ongoing security investigations and communicate threat information to different audiences.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-report-templates.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# About Report Templates in TISC

Report templates in TISC help you generate standardized reports for cases and threat intelligence investigations. Use these templates to track ongoing security investigations and communicate threat information to different audiences.

Use this feature to create different types of report templates. You can apply templates to cases and threat intelligence to track ongoing investigations. The templates help generate reports about threats to your organization.

This section explains how to implement CTI reporting for case and threat intelligence reports. It covers both admin \(template design\) and analyst \(runtime\) experiences.

For case reports, you can add custom case task form fields or related lists to the report template.

You can format and configure both the reports based on your requirements using various report elements.

Role required: sn\_sec\_tisc.admin

The following table explains case and threat intelligence report templates that are provisioned within the base system.

|Name|Description|
|----|-----------|
|Case Status Report - Threat Actor Profile|This report provides status about ongoing case investigations related to threat actors. It helps understand the context and relevance of threats to the organization, adversary behavior, potential goals, IOC enrichment, associated malware and tools, observed TTPs, and differences from existing TTPs.|
|Executive Summary|This report informs senior decision makers about a particular risk. The focus is on executive audiences and strategic problems, explaining why and how rather than what and when. Technical details and appendices are not included.|
|Post Investigation Summary - Threat Actor Profile|This report provides context and relevance of threats to the organization. It covers adversary behavior, potential goals, IOC enrichment, associated malware and tools, observed TTPs, and differences from existing TTPs.|
|Threat Intelligence - Alert|An Alert Report is a generic and user-configurable report that lists specific security alerts meeting user-defined criteria. It is often used to manage non-critical notifications.|
|Threat Intelligence - Tipper|A Tipper Report provides actionable, timely information on threat actors, techniques, and trends. The information is directly relevant to a specific business.|
|Threat Intelligence Report - Periodic Intelligence Report|A Periodic Report is a regular update, such as a monthly or quarterly document. It provides a general overview of business operations, projects, or company status rather than focusing on specific threats or alerts.|

**Note:** By default, these reports are in the published state and are read-only. Users cannot edit the templates, and analysts cannot generate reports because the templates are turned off.

