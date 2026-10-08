---
title: Components installed
description: Information about the scheduled jobs and tables that are installed with the HRBP productivity assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/hrbp-sa-components-installed.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 1
breadcrumb: [Reference, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Components installed

Information about the scheduled jobs and tables that are installed with the HRBP productivity assistant.

## HRBP productivity assistant scheduled jobs

The following table consists of scheduled jobs for the HRBP productivity assistant.

|Scheduled job|Description|
|-------------|-----------|
|HRBP Weekly Email Scheduled Job|This scheduled job sends weekly digest emails to HR business partners, collecting their open cases and items for the week.|
|HRBP assignment weekly reconciliation|This weekly job re-syncs HR business partner assignments for all active cases to catch organization changes missed by the real-time business rule, such as bulk imports.|

## Data access and case assignment tables

|Table|Description|
|-----|-----------|
|`sn_hrbp_hub_hr_data_access`|HR data access definitions.|
|`sn_hrbp_hub_hr_data_access_rule`|Rules that determine HR data access.|
|`sn_hrbp_hub_hr_data_access_assignment`|Assignments of HR data access to HRBPs.|
|`sn_hrbp_hub_hrbp_case_assignment`|Assignments of HR cases to HRBPs.|

