---
title: Modify purge policies to clean up data
description: Modify the default data purge policies to clean up data according to your organizational requirement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/hr-service-delivery/set-up-purge-pollicies-ta.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [purge policies, data cleanup, table cleanup, purge data]
breadcrumb: [Configure, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Modify purge policies to clean up data

Modify the default data purge policies to clean up data according to your organizational requirement.

## Before you begin

Role required: sn\_ta\_hiring\_core.admin/ sn\_ta\_tp.talent\_profile\_admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Administration** &gt; **Table Cleanup**.

2.  Select one or more of the following tables to modify the default auto flush settings one at a time.

    |Table|Matchfield type|Data retention|
    |-----|---------------|--------------|
    |sn\_ta\_hiring\_core\_job\_application \[sn\_ta\_hiring\_core\_job\_application\]|sys\_updated\_on|3 years|
    |sn\_ta\_tp\_talent\_profile \[sn\_ta\_tp\_talent\_profile\]|sys\_updated\_on|3 years|
    |sn\_ta\_hiring\_core\_job\_applicant \[sn\_ta\_hiring\_core\_job\_applicant\]|sys\_updated\_on|3 years|
    |sn\_ta\_tp\_talent\_pool \[sn\_ta\_tp\_talent\_pool\]|sys\_updated\_on|3 years|
    |sn\_ta\_hiring\_core\_job\_description \[sn\_ta\_hiring\_core\_job\_requisition\]|sys\_updated\_on|3 years|
    |sn\_ta\_tp\_talent\_profile \[sn\_ta\_tp\_talent\_profile\]|job\_applicant.consent\_updated|1 year|

    For a description of the auto flush form field values, see [Autoflush form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/atf-auto-flush.md).


-   **[Rules to archive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/hr-service-delivery/archive-data-ta.md)**  
Create rules to archive and delete data according to your organizational policy.
-   **[Cascade rules for cleaning data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/hr-service-delivery/cascade-rule-ta.md)**  
Cascade rules determine a thorough cleanup of the outdated data and its related counterparts at source from the system.

**Parent Topic:**[Configuring Hiring Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/hr-service-delivery/config-frmwrk-ta.md)

