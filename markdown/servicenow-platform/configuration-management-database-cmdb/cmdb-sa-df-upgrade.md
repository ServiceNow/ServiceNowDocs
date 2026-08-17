---
title: Managing principal class marking during upgrade
description: Make sure that existing Hardware Asset Management \(HAM\) CI classes are included as principal classes in Data Foundations during upgrade, without requiring manual configuration.Review and adjust the CI classes that CMDB success advisor automatically marked as principal classes during upgrade.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-upgrade.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [principal class marking during upgrade, HAM model category migration, automatic principal class assignment, upgrade impact on CI picker filtering, review principal classes after upgrade, adjust automatically marked classes, CI picker filtering system properties]
breadcrumb: [Configure, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Managing principal class marking during upgrade

Make sure that existing Hardware Asset Management \(HAM\) CI classes are included as principal classes in Data Foundations during upgrade, without requiring manual configuration.

Upgrading to a version of CMDB success advisor that introduces the Data Foundations principal class concept can result in CI classes being automatically marked as principal classes when existing HAM model category selections are present.

In CMDB success advisor, each HAM model category maps to one or more CI classes.

For example, if you selected the Computers model category, the cmdb\_ci\_computer class was included. Before the upgrade, these classes were used only for HAM data quality tracking.

After you upgrade to a version that includes Data Foundations, CMDB success advisor automatically marks those same CI classes as principal classes. This gives you a starting point for Data Foundations without requiring manual configuration.

## Upgrade impact

The following table shows how principal classes from HAM model categories are applied across key features in Data Foundations after upgrade.

|Feature|Impact after upgrade|
|-------|--------------------|
|Principal classes list|Your Data Foundations principal classes list is already populated with CI classes from your HAM model category selections.|
|CI picker on task records|On incidents, problems, and changes, the CI picker shows only CIs from your principal classes.|
|Data Foundations dashboard|Your Data Foundations advisor dashboard may already display data using the HAM derived principal classes as the initial scope.|

## Recommended actions

Review and confirm the CI classes that were automatically marked as principal classes during upgrade, and adjust CI picker filtering behavior if needed. For instructions, see [Review principal classes marked automatically during upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-upgrade.md).

## Review principal classes marked automatically during upgrade

Review and adjust the CI classes that CMDB success advisor automatically marked as principal classes during upgrade.

### Before you begin

Role required: sn\_cmdb\_admin

### About this task

Automatic principal class marking happens only once during upgrade. Later changes to HAM model categories do not update the principal classes list automatically. Similarly, principal class changes made without using CMDB success advisor, for example through CI Class Manager, are not reflected in the Data Foundations advisor scope automatically.

### Procedure

1.  On the CMDB success advisor landing page, on the Data Foundations card, select **Edit principal classes**.

    Use this to review the classes that were automatically marked as principal classes during upgrade. See [Managing Data Foundations advisor scope in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-optimize-dashboard.md).

2.  Confirm that the marked classes align with your Data Foundations advisor scope, then remove any unwanted classes and add others as needed.

    You can select up to 200 principal classes.

3.  If CI picker filtering affects users, adjust behavior using the system properties for CMDB success advisor.

    See [Principal class tracking in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-principal-class.md).


