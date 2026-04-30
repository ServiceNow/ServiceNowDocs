---
title: Modify display limit in Hierarchy tab of EAP
description: Configure an initial load limit system property to control how many work items the Hierarchy tab displays at each portfolio level in the Enterprise Agile Planning \(EAP\) workspace.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-02-26"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Modify display limit in Hierarchy tab of EAP

Configure an initial load limit system property to control how many work items the Hierarchy tab displays at each portfolio level in the Enterprise Agile Planning \(EAP\) workspace.

## Before you begin

Ensure that **Application Scope** of your ServiceNow instance is set to **Strategic Planning**.

Role required: admin

## About this task

By default, the Hierarchy tab loads the top 100 work items at each portfolio level, ordered by global rank. This limit applies across all levels such as Portfolio, Solution Train, Agile Release Train, and Agile Team. When a portfolio contains more than 100 top-level items, team members may not see all relevant work without manually applying filters.

Creating the **sn\_apw\_advanced.eap\_hierarchy\_items\_limit** system property overrides this default and lets you set a display limit that better matches your organization's portfolio size and performance requirements.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|sn\_apw\_advanced.eap\_hierarchy\_items\_limit|
    |Application|Strategic Planning. This value is automatically filed based on your instance's application scope.|
    |Description|A clear description on the purpose and functionality of the property.|
    |Type|Integer|
    |Value|Number of work items to be displayed in the Hierarchy tab of Enterprise Agile Planning.|
    |Read roles|User roles who can view this property.|
    |Write roles|User roles who can edit this property.|

4.  Select **Submit**.


