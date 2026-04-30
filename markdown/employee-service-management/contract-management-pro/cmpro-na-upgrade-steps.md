---
title: Post-upgrade steps for Now Assist in Contract Management
description: If you are upgrading to Now Assist in Contract Management from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [script to migrate data for Now Assist in Contract Management, post-upgrade steps for Now Assist in Contract Management, post upgrade steps for Now Assist in Contract Management]
breadcrumb: [Configure, Now Assist in CM Pro, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Post-upgrade steps for Now Assist in Contract Management

If you are upgrading to Now Assist in Contract Management from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  In the **Name** field, search for `Upsert DI skill config`.

3.  In the script, add the use case ids that you want to migrate to the Now Assist Admin console.

    ![Use case ids added tn the script box of the fix script.](../image/cmpro-na-upgrade-script.png "Post-upgrade fix script for Now Assist in Contract Management")

4.  Select **Run Fix Script**.


## Result

Your customized use cases are migrated to the Now Assist Admin console.

**Parent Topic:**[Configure Now Assist in Contract Management](confg-na-in-cmpro.md)

**Related topics**  


[Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)

[Select large language models for use cases in Now Assist in Contract Management](cmpro-na-manage-llm.md)

[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

[Configuring contract obligation extraction](cncore-conf-obligation-extraction.md)

[Configuring agentic workflows in Now Assist in Contract Management](../concept/cmpro-conf-agentic-workflow.md)

[Configuring contract metadata extraction](cncore-conf-metadata-extraction.md)

[Configuring contract analysis](../concept/cmpro-conf-contract-analysis.md)

