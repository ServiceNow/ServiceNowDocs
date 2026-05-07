---
title: Configure reports HR Service Delivery Advanced Integration with Workday
description: Configure the necessary reports to pull data, such as time offs plans, time off reasons, holiday calendar WID, and work schedule calendar WID, from Workday into the ServiceNow tables.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery Advanced Integration with Workday, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure reports HR Service Delivery Advanced Integration with Workday

Configure the necessary reports to pull data, such as time offs plans, time off reasons, holiday calendar WID, and work schedule calendar WID, from Workday into the ServiceNow tables.

**Important:** Only a Workday administrator can create reports in Workday. A ServiceNow administrator must collect the report details from a Workday administrator.

## Time off use case

To use the Time off request functionality, create the following reports:

-   Absence table reasons
-   Absence table tiers
-   Absence tables
-   Get holiday calendar WID
-   Get work schedule calendar WID
-   Time off plans
-   Time off reasons
-   Time off types
-   Time offs

**Note:** For information about the Time off request functionality, see [Time off request to Workday](w-timeoff.md).

## Payroll use case

To use the Payslip discrepancy functionality, create the Look up payslip report.

**Note:**

-   For information about the Payslip discrepancy functionality, see [Report an issue with your payslip](../task/payslips-awd.md).
-   For information about the Look up payslip report creation, see this [KB article](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3D157dd77ddbc63c58f21f5583ca9619a9%26sysparm_view%3D%26sysparm_domain%3Dnull%26sysparm_domain_scope%3Dnull).

## Total rewards use case

To use the Total rewards functionality, create the Total Rewards report.

**Note:**

-   For more information about the Total rewards functionality, see [Set up Total Rewards using Workday](../task/total-rewards-awd.md).
-   For information about the Total Rewards report creation, see this [KB article](https://support.servicenow.com/kb_knowledge.do?sys_id=b91467f9db4a3c58f21f5583ca9619a8&sysparm_view=&sysparm_domain=null&sysparm_domain_scope=null).

## Holiday calendar use case

To use the Holiday calendar functionality, create the Get holiday calendar WID report.

**Note:**

-   If you have already created Get holiday calendar WID report for the Time off request functionality, creating another report of Get holiday calendar WID is not required.
-   For more information about the Holiday Calendars functionality, see [Holiday calendars](../task/holiday-calendar-awd.md).
-   For information about the Holiday Calendar report creation, see this [KB article](https://support.servicenow.com/kb_knowledge.do?sys_id=39fa1ff1dbc63c58f21f5583ca961941&sysparm_view=&sysparm_domain=null&sysparm_domain_scope=null).

