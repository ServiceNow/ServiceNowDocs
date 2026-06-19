---
title: Outsourced Service Provider dashboard
description: The Outsourced Service Provider dashboard enables monitoring of breached service-level agreements \(SLAs\), average resolution time, and case transfer percentages, among other metrics. You can utilize the insights to identify the areas of concern and to plan your case management strategy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/ocs-dashboard.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Outsourced Customer Service, Extend capabilities, Configure, Customer Service Management]
---

# Outsourced Service Provider dashboard

The Outsourced Service Provider dashboard enables monitoring of breached service-level agreements \(SLAs\), average resolution time, and case transfer percentages, among other metrics. You can utilize the insights to identify the areas of concern and to plan your case management strategy.

**Important:** Starting with the Xanadu release, the Outsourced Service Provider dashboard has a new, modernized look and feel.

To access the new Outsourced Service Provider dashboard, navigate to **All** &gt; **Outsourced Customer Service** &gt; **Analytics**, and select the outsourced service provider \(OSP\) name. Existing customers upgrading from earlier releases to the Xanadu release can also access the new Outsourced Service Provider dashboard.

However, existing customers on release versions prior to the Xanadu release can still view the old Outsourced Service Provider dashboard by navigating to **All** &gt; **Outsourced Customer Service** &gt; **Overview**.

\[Omitted image "ocs-dashboard.jpeg"\] Alt text: Outsourced Service Provider dashboard displaying data for all the service providers. For more information about different metrics, refer to the Indicators section.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Internal OSP Manager|sn\_csm\_ocs.manager|

## Indicators

**Outsource cases: Unassigned open cases**

The number of open cases that are unassigned to the OSP agents.

**Outsourced cases: open cases with breached SLAs**

The number of cases that have remained open past the time required by the Service Level Agreement \(SLA\).

**Outsource cases: open cases**

The number of cases that are in the open state.

**Outsourced cases: Average overall CSAT**

Average customer satisfaction \(CSAT\) based on survey results. For more information about CSAT, see [Customer service satisfaction surveys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/c_CustomerServiceSatisfactionSurvey.md).

**Outsourced cases: Number of resolved cases**

The number of cases that the OSP agent has worked on and moved to resolved state.

**Outsourced cases: Summed duration of resolved cases**

The total time taken by the OSP agents to resolve the cases.

**Outsourced cases: Number of transferred cases**

Number of cases that are transferred to an internal ServiceNow agent when an OSP agent couldn’t resolve the case.

## Global filter

The Outsourced Service Provider dashboard utilizes the outsourced service providers as global filters. You can select one or more outsourced service providers to view different metrics and reports. By default, the dashboard displays data from all outsourced service providers.

## Reports

|Title|Type|Description|
|-----|----|-----------|
|Unassigned Open Cases|\[Omitted image "icon-single-score-report.png"\] Alt text: Single score report|The number of cases that are in the open state and isn’t yet assigned to an OSP agent. In this report, for example, there are 42 cases that are yet to be assigned. The OSP manager views the number of such cases at a glance and assigns them.|
|Active SLAs Breached|\[Omitted image "icon-single-score-report.png"\] Alt text: Single score report.|This report shows all breached SLAs that are still active In this report, for example, there are 42 such active SLAs. The OSP manager views the number of breached SLAs at a glance, which helps in taking immediate action.|

