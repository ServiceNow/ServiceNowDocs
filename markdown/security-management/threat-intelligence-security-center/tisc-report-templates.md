---
title: Report Templates
description: Defines the ability to re use the report templates that can be shared within the group of users to generate reports quickly and consistently.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administration, Threat Intelligence Security Center, Security Operations]
---

# Report Templates

Defines the ability to re use the report templates that can be shared within the group of users to generate reports quickly and consistently.

Use this feature to create different types of report templates, which can be applied to case\(s\) that provides the status of ongoing investigation in relevance to any threat to your organization, and helps in generating reports of the same.

This section explains how to implement CTI reporting at a case level and also provides both admin \(template design\) and analyst \(runtime\) experiences.

You can add custom case task form fields or related lists to the report template that are dot-walkable. In addition, you can format and configure the report based on your requirements using various report elements.

Role required: sn\_sec\_tisc.admin

The following table explains a few report templates that are provisioned within the base system.

|Name|Description|
|----|-----------|
|Case Status Report - Threat Actor Profile|The Report is designed to provide a status about ongoing case investigation related to a threat actor trying to understand the context and relevance of the threat to the organization, adversary behaviour and potential goals, IOC enrichment, associated malware and tools, Observed TTPs, difference from existing TTPs – net new capabilities, slight modifications, and so on.|
|Executive Summary|The Report is designed to inform senior decision makers about a particular risk. The focus is on executive audiences and in support of strategic problems explaining why and how, rather than what and when. Any technical details and appendices in support of long-form, narrative writing will not be included in this report.|
|Post Investigation Summary - Threat Actor Profile|The Report is designed to provide context and relevance of the threat to the organization; adversary behaviour and potential goals; IOC enrichment; Associated malware and tools; Observed TTPs; Difference from existing TTPs – net new capabilities, slight modifications, and so on.|

**Note:** By default, these reports are in the published state and will be in read-only mode. As the report templates will be in the read-only mode, the users can't make any edits to the templates and the analysts will not able to generate the reports as the report templates will be disabled.

