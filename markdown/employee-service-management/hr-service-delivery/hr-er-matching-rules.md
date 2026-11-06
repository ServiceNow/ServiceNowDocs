---
title: Employee Relations matching rules
description: ER cases do not use a subject person. Matching rules look for an agent with the required skills in the same country where the case was opened. That agent is assigned the case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/hr-service-delivery/hr-er-matching-rules.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Employee Relations matching rules

ER cases do not use a subject person. Matching rules look for an agent with the required skills in the same country where the case was opened. That agent is assigned the case.

Matching rules look for:

-   Country the ER case was opened in.
-   If no country is available, find any involved parties with a type of complainant and use their country.
-   If there are no involved parties with type of complainant, look for involved parties with type of subject of allegation and use their country.
-   If there are no involved parties with a country that can be used, then only skills are used.

**Note:** For more information, see [Add or modify a matching rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/hr-service-delivery/CreateModMatchingRule.md).

You can restrict an ER case to be assigned to only members of a specific group. See [Configure an employee relations case restriction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/hr-service-delivery/hr-er-create-case-restriction.md).

