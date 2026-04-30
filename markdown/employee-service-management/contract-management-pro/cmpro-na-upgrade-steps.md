---
title: Post-upgrade steps for Now Assist in Contract Management
description: If you are upgrading to Now Assist in Contract Management starting with Yokohama \(Patch 3\) from a previous version and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-04-02"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Post-upgrade steps for Now Assist in Contract Management

If you are upgrading to Now Assist in Contract Management starting with Yokohama \(Patch 3\) from a previous version and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  In the **Name** field, search for `Upsert DI skill config`.

3.  In the script, add the use case ids that you want to migrate to the Now Assist Admin console.

    ![Use case ids added tn the script box of the fix script.](../image/cmpro-na-upgrade-script.png "Post-upgrade fix script for Now Assist in Contract Management")

4.  Select **Run Fix Script**.


**Parent Topic:**[Configure Now Assist in Contract Management](confg-na-in-cmpro.md)

**Related topics**  


[Select large language models for use cases in Now Assist in Contract Management](cmpro-na-manage-llm.md)

[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)

[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)

[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

