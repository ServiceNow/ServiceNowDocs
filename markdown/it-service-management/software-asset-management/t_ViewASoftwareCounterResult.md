---
title: View software counter results for the legacy Software Asset Management plugin
description: Software counter results provide detailed information about each grouping that is formed through the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# View software counter results for the legacy Software Asset Management plugin

Software counter results provide detailed information about each grouping that is formed through the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## Procedure

1.  On the Software Counter form, click a name in the **Software Counter Results** related list.

    ![SAM software counter results 2](../image/SAMSoftwareCounterResults2.png "SAM software counter results 2")

2.  View the Software Counter Result form \(see table\).

    All fields on the form are read-only.

    ![SAM software counter results 3](../image/SAMSoftwareCounterResults3.png "SAM software counter results 3")

    |Field|Description|
    |-----|-----------|
    |Software counter|Name of the software counter whose results are displayed.|
    |Grouping|Grouping this software belongs to.|
    |Parent|Name of the parent software, if one exists, assigned to this software.|
    |Rights|Number of rights available in the group.|
    |Installs|Number of rights used by installations of the software in the group.|
    |Immediate compliance|Number of additional rights needed for the group to achieve compliance based on installations.|
    |Planned compliance|Number of additional rights needed for the group to achieve compliance based on installations and number of unused entitlements available.|
    |Usage Section|
    |Foreground|Total duration of foreground usage of the software, based on all the installations for the group.|
    |Background|Total duration of background usage of the software, based on all the installations for the group.|
    |Times used|Total number of times the software was used, based on software usage records for the group.|
    |Duration|Total duration of software usage, based on software usage records for the group. \(Not the sum of Foreground and Background.\)|
    |Related List|
    |Summary|Breakdown of software counter results by[type](../concept/c_UseTheSoftwareCounter.md). Click a type to view a detailed [summary](t_ViewASoftwareCounterSummary.md).|


**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](../concept/c_UseCountersSWLicenseReconcil.md)

