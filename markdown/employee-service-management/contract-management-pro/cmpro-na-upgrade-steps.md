---
title: Post-upgrade steps for Now Assist in Contract Management
description: If you are upgrading to Now Assist in Contract Management starting with Yokohama \(Patch 3\) from a previous version and you have customized use cases, run a fix script to migrate the existing data to the AI Admin Hub console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cmpro-na-upgrade-steps.html
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-04-02"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Post-upgrade steps for Now Assist in Contract Management

If you are upgrading to Now Assist in Contract Management starting with Yokohama \(Patch 3\) from a previous version and you have customized use cases, run a fix script to migrate the existing data to the AI Admin Hub console.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  In the **Name** field, search for `Upsert DI skill config`.

3.  In the script, add the use case ids that you want to migrate to the AI Admin Hub console.

    \[Omitted image "cmpro-na-upgrade-script.png"\] Alt text: Use case ids added tn the script box of the fix script.

4.  Select **Run Fix Script**.


**Parent Topic:**[Configure Now Assist in Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/confg-na-in-cmpro.md)

**Related topics**  


[Select large language models for use cases in Now Assist in Contract Management]()

[Configure data permissions for Now Assist skills]()

[Configuring contract metadata extraction]()

[Configuring contract analysis]()

[Configuring contract obligation extraction]()

[Configuring agentic workflows in Now Assist in Contract Management]()

