---
title: Classify and normalize software spend transactions by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Classify imported spend transactions to identify software purchases and normalize the derived raw publisher and raw product by matching them to existing publisher and product records. This automation reduces manual effort and improves spend reporting accuracy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/classify-normalize-software-spend-transactions.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ServiceNow Otto for Software Asset Management, software asset management, generative AI skills, Spend transaction software classification skill, Spend transaction software normalization skill]
breadcrumb: [Use generative AI skills, Using AI in Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Classify and normalize software spend transactions by using ServiceNow Otto for Software Asset Management \(SAM\)

Classify imported spend transactions to identify software purchases and normalize the derived raw publisher and raw product by matching them to existing publisher and product records. This automation reduces manual effort and improves spend reporting accuracy.

## Before you begin

Role required: sam\_user

The following plugins and store applications must be installed on your ServiceNow instance to use the AI skills:

-   [ServiceNow Otto for Software Asset Management \(SAM\)](https://store.servicenow.com/store/app/869d23661b646a50a85b16db234bcbab) \(sn-now-assist-sam\) app
-   Software Asset Management Professional \(com.snc.samp\) plugin
-   [Software Asset Workspace](https://store.servicenow.com/store/app/f3a752821b4f221084105282604bcb32) \(sn\_sam\_workspace\) app
-   Software Asset Management - Spend Detection \(com.sn\_sam\_spend\) plugin

AI Search must be activated on your ServiceNow® instance. For details, see the AI Search activation steps in [Install ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-now-assist-sam.md).

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

ServiceNow Otto for SAM classifies and normalizes spend transactions through the Spend transaction software classification skill and the Spend transaction software normalization skill. The skills run automatically as part of the Software Spend Detection workflow whenever spend transactions are imported or manually created.

**Note:** AI-generated classifications may contain inaccuracies. Review AI-classified transactions to verify accuracy before using them for compliance or financial reporting.

## Procedure

1.  Import spend transactions or manually create a spend transaction.

    For details, see:

    -   [Import financial transactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-spend-transactions.md)
    -   [Create a spend transaction manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/manually-update-transactions.md)
2.  After the **SAM - Label Spend Transactions** scheduled job runs, navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software spend detection** &gt; **All transactions** to review the classified transactions.

    The list shows each transaction's state, publisher, product, and prediction method. For details, see [Managing software spend in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-sam-workspace.md) and [AI-powered software spend detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-ai-enhancements.md).


**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/using-now-assist-sam.md)

