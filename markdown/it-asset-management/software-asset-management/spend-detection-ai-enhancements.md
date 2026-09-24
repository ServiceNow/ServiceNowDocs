---
title: AI-powered software spend detection
description: AI-powered spend detection identifies software purchases in imported spend transactions and normalizes the derived raw publisher and raw product to existing publisher and product records in Software Asset Management Content Library. This automation improves spend reporting accuracy and reduces manual classification effort.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/spend-detection-ai-enhancements.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [software spend detection, software asset workspace, software asset management spend detection, servicenow otto for software asset management, Spend transaction software classification skill, Spend transaction software normalization skill]
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management, Asset Management]
---

# AI-powered software spend detection

AI-powered spend detection identifies software purchases in imported spend transactions and normalizes the derived raw publisher and raw product to existing publisher and product records in Software Asset Management Content Library. This automation improves spend reporting accuracy and reduces manual classification effort.

When the ServiceNow Otto for Software Asset Management \(SAM\) store app \(sn\_now\_assist\_sam\) is installed, imported spend transactions are processed by two AI skills: the Spend transaction software classification skill and the Spend transaction software normalization skill. These AI skills improves classification accuracy for new software products and publishers, then links each software transaction to existing publisher and product records.

## How the AI-powered pipeline works

After a spend transaction import completes, the **SAM - Label Spend Transactions** scheduled job runs the imported transactions through the following AI skills:

-   **Spend transaction software classification skill**

    Analyzes the vendor name, description, and GL account for each transaction to identify whether it represents a software purchase. For transactions identified as software, the skill also extracts the publisher and product.

-   **Spend transaction software normalization skill**

    Matches the extracted publisher and product to the existing records in the Software Asset Management Content Library. This linking supports accurate spend reporting and license position tracking.


For more details, see [Classify and normalize software spend transactions by using ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/classify-normalize-software-spend-transactions.md) and [Skill inputs and triggers for ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/now-assist-sam-skills-inputs.md).

Transactions not identified as software are not processed by the Spend transaction software normalization skill.

**Note:** If the ServiceNow Otto for Software Asset Management \(SAM\) store app isn't installed or either AI skill is inactive, the **SAM - Label Spend Transactions** job uses the existing machine learning pipeline instead.

## How transactions move through the labeling pipeline

The **SAM - Label Spend Transactions** scheduled job updates the **State**, **Is software**, and **Is managed** fields on the Software Spend Transactions \[sam\_spend\_transaction\] table for each transaction based on the outcome of the classification and normalization skills.

The **State** field reflects the pipeline outcome for each transaction:

-   **New**

    Default state when a transaction is imported or manually created. A transaction stays in New if the pipeline exhausts the maximum number of retry attempts without reaching a terminal state.

-   **Labeled**

    The classification skill identified the transaction as a software purchase, and the normalization skill matched both the publisher and product to existing records in the Software Asset Management Content Library.

-   **Partially labeled**

    The classification skill identified the transaction as a software purchase, and the normalization skill matched the publisher, but not the product, to an existing record in the Software Asset Management Content Library. The **Is software** field is set to true.

-   **Unlabeled**

    The pipeline couldn't classify or normalize the transaction after the maximum number of retry attempts.

-   **Manually labeled**

    A user manually set or updated the **Is software**, **Publisher**, or **Product** fields on the transaction.


When the classification skill identifies a transaction as a non-software purchase, the **Is software** field is set to false, and the transaction bypasses the normalization skill.

After a transaction reaches the Labeled or Partially labeled state, the **Is managed** field is evaluated. When a matching software model exists in your Software Asset Management Content Library for the normalized publisher and product, the **Is managed** field is set to true.

The maximum number of retry attempts is controlled by the **samp.spend\_prediction\_service.max\_label\_attempts** system property, which defaults to 3. You can update this property at any time. For more details, see [Software Asset Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/sam-properties.md).

## AI activity log

Track how many software transactions are processed by the AI pipeline using the **AI activity log** card. This card shows a rolling count of transactions from the Software Spend Transactions \[sam\_spend\_transaction\] table where the prediction method is AI, the transaction is a software purchase, and the state is Labeled or Partially labeled.

To access the card, go to **Software Asset Workspace** &gt; **Software asset overview**. The card appears under the **Activity center** section.

**Parent Topic:**[Software Spend Detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/software-spend-detection.md)

**Related topics**  


[Managing software spend in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/spend-detection-sam-workspace.md)

[AI in Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/exploring-now-assist-sam.md)

[Skill inputs and triggers for ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/now-assist-sam-skills-inputs.md)

[Generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/explore-generative-ai-skills-now-assist-sam.md)

