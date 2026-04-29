---
title: Quick start tests for Integration Commons for CMDB
description: Validate that integrations for CMDB pass validation and still work after you make any configuration changes such as applying an upgrade or developing an application.
locale: en-US
release: australia
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Quick start tests for Integration Commons for CMDB

Validate that integrations for CMDB pass validation and still work after you make any configuration changes such as applying an upgrade or developing an application.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](https://www.servicenow.com/docs/access?context=atf-enable-tests&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Integration Commons for CMDB

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB INT: Set Test Session Application|Modify the run server-side script to set an application name so that you can test only one integration. Otherwise, all integrations installed will be tested.|Paris|
|CMDB INT: Test Against Source Analysis|Test an integration against the values in the CMDB Integration Source Analysis \[sn\_cmdb\_int\_util\_cmdb\_integration\_source\_analysis\] table.|Paris|
|CMDB INT: Validate Application Feed|Validate all application feeds in an integration.|Paris|
|CMDB INT: Validate Discovery Source|Validate that the discovery source exists.|Paris|
|CMDB INT: Validate Entity Mappings|Validate all entity mappings of an integration.|Paris|
|CMDB INT: Validate Fields|Validate fields for CMDB Integrations.|Paris|
|CMDB INT: Validate Lookups|Validate CMDB integration lookups.|Paris|
|CMDB INT: Validate Mandatory Operations|Validate that all integrations for mandatory operations exist for mapped fields.|Paris|
|CMDB INT: Validate Operations|Validate all operations for an integration.|Paris|
|CMDB INT: Validate References|Validate CMDB integration references.|Paris|
|CMDB INT: Validate Related Entries|Validate all related classes against the data dictionary for related entries.|Paris|
|CMDB INT: Validate Relationships|Validate CMDB integration relationships.|Paris|

To learn more about Integration Commons for CMDB, see [Integration Commons for CMDB](../../../product/configuration-management/concept/integration-commons-for-cmdb.md).

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

