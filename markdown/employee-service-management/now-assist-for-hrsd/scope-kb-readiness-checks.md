---
title: Scope KB readiness checks to HR knowledge
description: Limit the Knowledge Base and Content Readiness checks to HR knowledge articles so the results are faster to generate and more relevant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/now-assist-for-hrsd/scope-kb-readiness-checks.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 1
breadcrumb: [Check data readiness, Configure, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Scope KB readiness checks to HR knowledge

Limit the Knowledge Base and Content Readiness checks to HR knowledge articles so the results are faster to generate and more relevant.

## Before you begin

Role required: admin

You will need the system ID for each knowledge base category that you want to include. To find the system ID, do these steps:

1.  Navigate to **All** &gt; **HR Administration** &gt; **Knowledge Management** &gt; **All Articles**.
2.  Select the category.

    \[Omitted image "KB-category.png"\] Alt text: Knowledge article list showing KB0040002 “Benefits Overview” with its Category column highlighted in green

3.  From the additional actions menu, select **Copy sys\_id**.

    \[Omitted image "knowledge-base-sys-id.png"\] Alt text: Knowledge Category form menu with the “Copy sys\_id” option outlined in green


## About this task

By default, the Knowledge Base and Content Readiness checks run on every knowledge article in the instance. A warning icon next to the Knowledge Base &amp; Content Readiness section shows that no category filter is applied.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Locate the `hrAIA_ReadinessSnapshotUtilsSNC` script.

3.  In the scripting box, locate `KB_CATEGORY_SYS_IDS`, where you can specify the HR knowledge base category.

4.  Select **Update**.


## What to do next

Continue to [Check data readiness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/check-data-readiness.md)

**Parent Topic:**[Check data readiness](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/check-data-readiness.md)

