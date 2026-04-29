---
title: About Report Templates in TISC
description: Defines the ability to re use the report templates that can be shared within the group of users to generate reports quickly and consistently.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# About Report Templates in TISC

Defines the ability to re use the report templates that can be shared within the group of users to generate reports quickly and consistently.

Use this feature to create different types of report templates, which can be applied to case\(s\) and threat intelligence that provides the status of ongoing investigation in relevance to any threat to your organization, and helps in generating reports of the same.

This section explains how to implement CTI reporting for both case and threat intelligence reports, and also provides both admin \(template design\) and analyst \(runtime\) experiences.

For case reports, you can add custom case task form fields or related lists to the report template.

You can format and configure both the reports based on your requirements using various report elements.

Role required: sn\_sec\_tisc.admin

The following table explains a few case and threat intelligence report templates that are provisioned within the base system.

|Name|Description|
|----|-----------|
|Case Status Report - Threat Actor Profile|The Report is designed to provide a status about ongoing case investigation related to a threat actor trying to understand the context and relevance of the threat to the organization, adversary behavior and potential goals, IOC enrichment, associated malware and tools, Observed TTPs, difference from existing TTPs – net new capabilities, slight modifications, and so on.|
|Executive Summary|The Report is designed to inform senior decision makers about a particular risk. The focus is on executive audiences and in support of strategic problems explaining why and how, rather than what and when. Any technical details and appendices in support of long-form, narrative writing will not be included in this report.|
|Post Investigation Summary - Threat Actor Profile|The Report is designed to provide context and relevance of the threat to the organization; adversary behavior and potential goals; IOC enrichment; Associated malware and tools; Observed TTPs; Difference from existing TTPs – net new capabilities, slight modifications, and so on.|
|Threat Intelligence - Alert|An Alert Report is a more generic and user-configurable report listing specific security alerts that meet user-defined criteria, often used to manage non-critical notifications.|
|Threat Intelligence - Tipper|A Tipper Report is a threat intelligence report that provides actionable, timely information on threat actors, techniques, and trends directly relevant to a specific business.|
|Threat Intelligence Report - Periodic Intelligence Report|A Periodic Report is a regular update, such as a monthly or quarterly document, that provides a general overview of business operations, projects, or a company's overall status, rather than focusing on specific threats or alerts.|

**Note:** By default, these reports are in the published state and will be in read-only mode. As the report templates will be in the read-only mode, the users can't make any edits to the templates and the analysts will not able to generate the reports as the report templates will be disabled.

