---
title: Post-upgrade steps for ServiceNow Otto for Contract Management Pro
description: If you are upgrading to ServiceNow Otto for Contract Management Pro from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the AI Admin Hub console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cmpro-na-upgrade-steps.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [script to migrate data for Now Assist in Contract Management, post-upgrade steps for Now Assist in Contract Management, post upgrade steps for Now Assist in Contract Management, script to migrate data for ServiceNow Otto for Contract Management, post-upgrade steps for ServiceNow Otto for Contract Management, post upgrade steps for ServiceNow Otto for Contract Management]
breadcrumb: [Configure, ServiceNow Otto for Contract Management Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Post-upgrade steps for ServiceNow Otto for Contract Management Pro

If you are upgrading to ServiceNow Otto for Contract Management Pro from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the AI Admin Hub console.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  In the **Name** field, search for `Upsert DI skill config`.

3.  In the script, add the use case ids that you want to migrate to the AI Admin Hub console.

    \[Omitted image "cmpro-na-upgrade-script.png"\] Alt text: Use case ids added tn the script box of the fix script.

4.  Select **Run Fix Script**.


## Result

Your customized use cases are migrated to the AI Admin Hub console.

**Parent Topic:**[Configure ServiceNow Otto for Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md)

**Related topics**  


[Configure data permissions for AI skills]()

[Select large language models for use cases in ServiceNow Otto for Contract Management Pro]()

[Configuring contract metadata extraction]()

[Configuring contract analysis]()

[Configuring contract obligation extraction]()

[Configuring agentic workflows in ServiceNow Otto for Contract Management Pro]()

[Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-conf-metadata-extraction.md)

[Configuring contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-conf-contract-analysis.md)

