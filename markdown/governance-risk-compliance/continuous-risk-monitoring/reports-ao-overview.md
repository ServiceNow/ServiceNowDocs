---
title: AO Overview dashboard
description: Users with the Authorization Official \[sn\_irm\_cont\_auth.authorization\_official\] role can view the reports in the AO Overview module.
locale: en-US
release: xanadu
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: reference
last_updated: "2024-08-07"
reading_time_minutes: 2
breadcrumb: [Analytics and Reporting Solutions for CAM, CAM reference, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# AO Overview dashboard

Users with the Authorization Official \[sn\_irm\_cont\_auth.authorization\_official\] role can view the reports in the AO Overview module.

**Important:** Starting with version 18.1.2 of CAM users on Vancouver or Washington DC can view the AO Overview dashboard in the Next Experience UI Framework.

For more information on navigation steps and dashboard appearance, see [Analytics and Reporting Solutions for CAM](../../../use/dashboards/application-content-packs/cam-pa-next-exp-dashboards.md).

## Accessing the dashboard

Users with the following roles can access the dashboard:

-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)
-   Executive Reader \(sn\_irm\_cont\_auth.executive\_read\)
-   Authorizing Official \(sn\_irm\_cont\_auth.authorization\_official\)

To open the dashboard, navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **Analytics Dashboards** &gt; **AO Overview**.

![Short video displaying the different tabs of the AO Overview dashboard.](../image/cam-ao-ovrvw-washingtondc.gif)

## AO Overview - Authorization Packages tab

The Authorization Packages tab on the AO Overview dashboard provides central visibility into the state of all packages. The reports on the Baseline Controls tab provide a general overview of the baseline controls in your system.

|Report|Description|
|------|-----------|
|Packages Pending Approval|The number of authorization packages for which approval has been requested, but that haven’t yet received approval.|
|Packages with Overridden Impact|The number of authorization packages with an impact that have been overridden. For more information, see [RMF step 1 - Categorize the authorization package](../task/categorize.md).|
|Packages by Step|The number of authorization packages categorized by steps \(for example, Monitor, Access, Select, and so forth\).|
|Packages by Impact|The number of authorization packages categorized by impact levels.|
|Pending Approvals|A list of all packages pending approval.|

## AO Overview - Baseline Controls tab

The reports on the Baseline Controls tab on the AO Overview dashboard provide a general overview of the baseline controls in your system.

|Report|Description|
|------|-----------|
|Packages with Unimplemented Controls|The number of authorization packages for which common controls were created, but haven’t yet been implemented.|
|Packages with Inherited Controls|The number of authorization packages that contain baseline controls inherited from a common control.|
|Packages with Common Controls|The number of authorization packages for which common controls were created and implemented.|
|Compliance Score Percentage|Compliance score percentages for policies grouped by name or number.|

**Parent Topic:**[Analytics and Reporting Solutions for CAM](../../../use/dashboards/application-content-packs/cam-pa-next-exp-dashboards.md)

