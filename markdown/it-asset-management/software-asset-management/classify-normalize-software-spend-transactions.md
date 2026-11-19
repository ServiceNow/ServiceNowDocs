---
title: Classify and normalize software spend transactions by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Classify imported spend transactions to identify software purchases and normalize the derived raw publisher and raw product by matching them to existing publisher and product records. This automation reduces manual effort and improves spend reporting accuracy.Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to classify spend transactions. A trigger initiates an action, such as when the system classifies spend transactions.Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/classify-normalize-software-spend-transactions.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [Spend transaction software classification, Spend transaction software normalization, Now Assist for SAM, Software spend detection, Software spend transactions, Spend transaction import, Label spend transactions, Publisher normalization, Product normalization, Raw publisher, Raw product, Software asset workspace, License operations, AI search, Software classification]
breadcrumb: [Use generative AI skills, Using AI in Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Classify and normalize software spend transactions by using ServiceNow Otto for Software Asset Management \(SAM\)

Classify imported spend transactions to identify software purchases and normalize the derived raw publisher and raw product by matching them to existing publisher and product records. This automation reduces manual effort and improves spend reporting accuracy.

## Before you begin

Before you use the Spend transaction software classification and Spend transaction software normalization skills, install the following plugins and the store apps that match your platform release version.

<table id="table_spend_txn_norm_plugins_bra"><thead><tr><th>

Platform release

</th><th>

Plugins

</th><th>

Store apps

</th></tr></thead><tbody><tr><td>

Australia Patch 6 or later patches

</td><td>

-   Software Asset Management Professional \[com.snc.samp\]
-   Software Asset Management - Spend Detection \[com.sn\_sam\_spend\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 11.0.0 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 11.0.2 or later

</td></tr><tr><td>

Brazil or later releases

</td><td>

-   Software Asset Management Professional \[com.snc.samp\]
-   Software Asset Management - Software Spend Detection \[com.sn\_sam\_spend\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 11.0.0 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 12.0.4 or later

</td></tr></tbody>
</table>AI Search must be activated on your ServiceNow® instance. For details, see the AI Search activation steps in [Install ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-now-assist-sam.md).

Role required: sam\_user

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The Spend transaction software classification skill first identifies whether each imported spend transaction is a software purchase. If the transaction is classified as software, then the skill extracts the raw publisher and raw product details using the vendor name, transaction description, and GL account columns. Transactions that the skill classifies as non-software skip the extraction step for raw publisher and raw product and are not passed to the Spend transaction software normalization skill.

**Note:** AI-generated classifications may contain inaccuracies. Review AI-classified transactions to verify accuracy before using them for compliance or financial reporting.

The Spend transaction software normalization skill matches software spend transactions to existing publisher and product records to enable accurate spend reporting and license position tracking. The skill uses AI search to normalize the raw publisher and raw product derived by the Spend transaction software classification skill. When the skill finds a reliable match in existing publisher and product records, it populates the publisher and product fields on the spend transaction record. If no reliable match exists, the transaction remains unnormalized.

## Procedure

1.  Import spend transactions or manually create a spend transaction.

    For details, see:

    -   [Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-spend-transactions.md)
    -   [Create a spend transaction manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/manually-update-transactions.md)
2.  After the **SAM - Label Spend Transactions** scheduled job runs, navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software spend detection** &gt; **All transactions** to review the classified transactions.

    The list shows each transaction's state, publisher, product, and prediction method. For details, see [Managing software spend in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-sam-workspace.md) and [AI-powered software spend detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md).


**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/using-now-assist-sam.md)

## Spend transaction software classification skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to classify spend transactions. A trigger initiates an action, such as when the system classifies spend transactions.

### Triggers for the Spend transaction software classification skill

The following table lists the trigger for the Spend transaction software classification skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|The skill classifies spend transactions as part of the spend transaction import pipeline through the SAM - Label Spend Transactions scheduled job. The job processes batches of transactions that haven't yet been classified.|

### Inputs for the Spend transaction software classification skill

The following table lists the input for the Spend transaction software classification skill.

|Input|Description|
|-----|-----------|
|Software Spend Transactions \[sam\_spend\_transaction\]|The skill reads the vendor name, transaction description, and GL account fields from imported spend transaction records.|

## Spend transaction software normalization skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

### Triggers for the Spend transaction software normalization skill

The following table lists the trigger for the Spend transaction software normalization skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|The skill normalizes the raw publisher and raw product after the Spend transaction software classification skill identifies a transaction as software. When a match is found in existing publisher and product records, the skill populates the Publisher and Product fields on the spend transaction record.|

### Inputs for the Spend transaction software normalization skill

The following table lists the input for the Spend transaction software normalization skill.

|Input|Description|
|-----|-----------|
|Extracted publisher and product values|Raw publisher and product produced by the Spend transaction software classification skill for transactions identified as software.|

