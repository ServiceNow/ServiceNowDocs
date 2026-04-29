---
title: Compliance filter
description: The compliance filter for license bases uses the following fields to define entitled users or CIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certification filters, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Compliance filter

The compliance filter for license bases uses the following fields to define entitled users or CIs.

These field values can be used independently or together to calculate compliance.

|Value|Description|
|-----|-----------|
|Entitled company|All users or configuration items \(CI\) at all locations of this company, in all departments are entitled to use this software package. Compliance at this level calculates how many licenses are purchased for the company at large and how many entitled users or CIs consume them.|
|Entitled location|CIs and users who are assigned to this company location in any department are entitled to use this software package. Compliance at this level calculates how many licenses are purchased for this company location and how many users and CIs consume them.|
|Entitled department|Only the users or CIs in this department at this company location are entitled to use this software package. Compliance is calculated for a single department only.|

The license form can display information about all CIs or named users who are using this software package. The form indicates when license reconciliation is necessary and displays all compliant users or CIs.

Possible compliance levels are:

|Level|Description|
|-----|-----------|
|Non applicable|Compliance levels for all infrastructure licenses that are related to cluster licenses are set to **Non applicable** automatically. Compliance levels are calculated in the cluster license only, and not in the related infrastructure licenses.|
|Out of compliance|More licenses are being consumed than were purchased. There are more users or CIs using this license than the license allows, and some users or CIs are not be entitled to use this software package.|
|Unused|The licenses for this software package are currently unused.|
|Reconciliation required|CIs or users who are not entitled to use this software are consuming licenses. Licenses that require reconciliation are considered out of compliance. Reconciliation requires action to ensure that unentitled users are not using the software. Reconciliation involves uninstalling software or increasing license counts to match actual user counts.|
|Nearly out of compliance|For a software package to be at this compliance level, more than 95% of the licenses are in use by entitled users or CIs. License bases at this level are considered to be **In compliance**.|
|In compliance|This software package has unused licenses. All users or CIs using a license are entitled to use this software package.|

