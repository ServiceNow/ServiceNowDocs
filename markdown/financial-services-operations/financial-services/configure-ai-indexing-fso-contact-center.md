---
title: Configure AI indexing for Agentic Contact Center for Banking
description: Configure AI indexing to enable intelligent search capabilities across financial accounts, cases, and customer interactions in Agentic Contact Center for Banking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services/configure-ai-indexing-fso-contact-center.html
release: australia
product: Financial Services
classification: financial-services
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 1
keywords: [configure ai indexing agentic contact center, ai search index agentic contact center, indexed sources agentic contact center, activate indexed sources agentic contact center, financial accounts indexed source, fso contact center search]
breadcrumb: [Configure, Agentic Contact Center for Banking, Banking applications, Financial Services Operations \(FSO\)]
---

# Configure AI indexing for Agentic Contact Center for Banking

Configure AI indexing to enable intelligent search capabilities across financial accounts, cases, and customer interactions in Agentic Contact Center for Banking.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Activate the following indexed sources if they aren't already active:

    -   Financial Accounts
    -   Financial Services Base
    -   Interaction
    1.  Select the record for the indexed source.

    2.  Select the **Active** check box if it isn't already selected.

3.  For each indexed source, select **Index All Tables**, then select **OK**.

4.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

5.  For each of the following search profiles, open the record and select **Publish**:

    -   Financial Accounts Search Profile
    -   Financial Services Base Search Profile
    -   FSO Interaction Search Profile

## Result

AI indexing is configured for Agentic Contact Center for Banking.

**Parent Topic:**[Configuring Agentic Contact Center for Banking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/configuring-agentic-contact-center-for-banking.md)

**Related topics**  


[Indexed Source form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/indexed-source-form-ais.md)

[Perform a full table index or reindex for a single AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/index-single-source-ais.md)

[Publish an AI Search search profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/publish-search-profile-ais.md)

