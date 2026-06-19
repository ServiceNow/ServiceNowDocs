---
title: Get started with Data Foundations advisor dashboard setup
description: The Data Foundations advisor dashboard can be configured automatically on installation or upgrade, or manually through the CMDB success advisor landing page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-get-started.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Get started with Data Foundations advisor dashboard setup

The Data Foundations advisor dashboard can be configured automatically on installation or upgrade, or manually through the CMDB success advisor landing page.

The Data Foundations scope defines which principal classes CMDB success advisor monitors. When a CI class is included in the Data Foundations advisor dashboard scope, the class is automatically marked as a principal class, which means it appears in CI selection filters on incident, change, and problem forms.

For guidance on choosing the right classes, see the [Guidance on designating principal classes in the CMDB \[KB2707240\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2707240) article in the Now Support Knowledge Base.

## Roles required

Role required: sn\_cmdb\_admin

## Automatic setup

When you install or upgrade CMDB success advisor, the **CMDB Advisor - Auto Setup** on-demand scheduled job can automatically configure the Data Foundations advisor dashboard if all eligibility conditions are met. Open the CMDB success advisor landing page to confirm the dashboard setup state before proceeding manually.

For more information on eligibility conditions and the auto-setup process, see [Automatic dashboard setup in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-auto-setup.md).

## Manual setup

If auto-setup did not run or the eligibility conditions were not met, configure the dashboard manually by selecting principal classes on the CMDB success advisor landing page.

For instructions, see [Set up the Data Foundations advisor dashboard manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-manual-setup.md).

