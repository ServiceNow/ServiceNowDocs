---
title: Configure Azure portal
description: Configuring the Azure portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/configure-azure-portal.html
release: brazil
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Hyperscaler connection with Azure, Using AI Control Tower to create hyperscaler connections, Using AI Control Tower \(legacy\), AI Control Tower \(legacy\), Establishing AI governance, Enable AI Experiences]
---

# Configure Azure portal

Configuring the Azure portal.

## Before you begin

Role required: Azure admin

## Procedure

1.  Log in to the Azure portal as Azure admin.

2.  Navigate to **Azure AI Foundry**.

3.  Open the **AI HUB resource** containing your agents.

4.  Select **Access Control \(IAM\)**.

5.  Select + Add icon to **Add role assignment**.

6.  Add roles **Cognitive Services Open AI Contributor** and **Contributor** to Service principal \(Integration user\).

    The credentials used on ServiceNow to connect to Azure are the credentials of the Service principal \(Integration user\).


## What to do next

[Connect to Azure from ServiceNow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-control-tower/connect-to-azure-from-servicenow.md)

