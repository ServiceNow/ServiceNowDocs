---
title: Use Invoice inquiry solution generator skill
description: Turn on the Invoice inquiry solution generator skill, which automates the resolution generation for inquiry cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/use-invoice-inquiry-solution-generator-skill.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, generator skill, Finance and Supply Chain, AI Admin, invoice inquiry case]
breadcrumb: [Use ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Use Invoice inquiry solution generator skill

Turn on the Invoice inquiry solution generator skill, which automates the resolution generation for inquiry cases.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills** and select the **AI Skills** tab in the AI Admin Hub console.

2.  Expand the **Finance and Supply Chain** workflow group and select **Accounts Payable Operations**.\[Omitted image "invoice-inquiry-solution-generate.png"\] Alt text: Invoice inquiry solution generator skill

3.  Select **Invoice inquiry solution generator skill**&gt; **Turn on**to activate the skill.

    Activate the skill in the **Turn on skill** pop-up. The skill works in relation with the Inquiry resolution provider agent. For more information on the Inquiry resolution provider AI agent, see [Inquiry resolution provider AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/apo-help-resolve-supplier-questions-agentic.md).


## Result

AI skills and the AI agent analyze the invoice and related inquiry data, then recommend a resolution. The AP agent reviews the recommendation and the case closure notes are updated automatically.

