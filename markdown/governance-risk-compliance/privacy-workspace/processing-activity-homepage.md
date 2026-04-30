---
title: Processing activity overview page
description: The processing activity overview page provides the privacy risk and compliance posture for a processing activity. This page contains details, such as compliance score, criticality score, risk posture and heatmap, privacy and risk assessment status, issues and policy exceptions, and control assurance status.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reporting, Privacy Management, Governance, Risk, and Compliance]
---

# Processing activity overview page

The processing activity overview page provides the privacy risk and compliance posture for a processing activity. This page contains details, such as compliance score, criticality score, risk posture and heatmap, privacy and risk assessment status, issues and policy exceptions, and control assurance status.

The vertical layout of a processing activity provides a structured, top-down view that presents information in a clear and sequential manner. This design facilitates an intuitive understanding of the data processing lifecycle by visually representing each step of the workflow in a linear progression. You can easily trace the flow of information from initiation through to completion, enabling better insight into how personal data is collected, used, shared, and retained. This layout supports streamlined navigation and improves the ability to identify key elements and dependencies within the processing activity, enhancing both usability and compliance oversight.

![Overview of the reports on a processing activity in Privacy management.](../image/processing-activity-prm-hr-onboarding-sample.png "Processing activity overview page")

## Required roles

To view the home page, you must have sn\_privacy.manager and the sn\_privacy.analyst roles.

## Use cases

For examples of how different people in your organization would use this home page, see the following use cases.

|User|Dashboard use|
|----|-------------|
|Privacy manager and Privacy analyst|The privacy manager and the privacy analyst can view and understand the privacy compliance posture of the given processing activity.|

## Reports in a processing activity overview

The processing activity overview page is organized into six sections.

|Title|Description|
|-----|-----------|
|State|Current state of the processing activity in the workflow: New, Discover, Review, Monitor, and Retired.|

|Title|Description|
|-----|-----------|
|Compliance score|Compliance score percentage of the processing activity and the change since the last period.|
|Criticality score|Regulatory risk level of the processing activity.|
|Compliance status|Number of compliant and non-compliant controls for each applicable authority document or policy. Toggle between **Authority documents** and **Policies** to switch views.|

|Title|Description|
|-----|-----------|
|Risk posture|Residual risk score of the processing activity, along with the inherent risk level and control effectiveness.|
|Risk heatmap|Distribution of processing activities by residual/inherent risk and control effectiveness levels. You can filter by risk classification.|

|Title|Description|
|-----|-----------|
|Risk assessments|Number of risk assessments by state, including counts for open, overdue, and due in 7 days. You can filter by RAM template.|
|Privacy assessments|Number of privacy assessments by state, including counts for open, overdue, and due in 7 days. You can filter by available assessment templates.|

|Title|Description|
|-----|-----------|
|Issues|Number of issues by priority, including counts for open, overdue, and due in 7 days.|
|Policy exceptions|Number of policy exceptions by risk rating, with counts for open, overdue, and due in 7 days.|

|Title|Description|
|-----|-----------|
|Controls|Distribution of controls by state.|
|Attestations|Number of attestations that are open, overdue, and due in 7 days.|
|Indicators|Number of indicators that are open, overdue, and failed in the last 6 months.|

**Parent Topic:**[Reporting for Privacy Management](reporting-prm.md)

