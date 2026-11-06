---
title: Financial Services Operations Core release notes
description: The ServiceNow Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Brazil release.Claim Summarization on the Claim Workspace and Claim Summary pages moves to the supported Now Assist context menu \(NACM\) component, replacing the deprecated AI Summary Card component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/financial-services-operations-core-rn.html
release: brazil
topic_type: topic
last_updated: "2026-04-06"
reading_time_minutes: 1
keywords: [claim summarization, NACM, AI Summary Card, claim workspace, claim summary, Now Assist, financial services]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Financial Services Operations Core release notes

The ServiceNow® Financial Services Operations Core application provides a data model that enables financial institutions to create flexible data structures that meet their business needs. Financial Services Operations Core was enhanced and updated in the Brazil release.

## About Financial Services Operations Core

The case type selector in Financial Services Operations now uses the predefined Customer Service Management \(CSM\) implementation, replacing the previous FSO-specific override.

See [Case type selector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-case-type-select-modals.md) for more information.

## Activation and other requirements

**Important:** Financial Services Operations Core is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Financial Services Operations Core by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/financial-services-operations-rn-landing.md)

## Version 13.2.1

Claim Summarization on the Claim Workspace and Claim Summary pages moves to the supported Now Assist context menu \(NACM\) component, replacing the deprecated AI Summary Card component.

### What's changed

-   **Claim Summarization component update**

    Generate AI-powered claim summaries using the Now Assist context menu \(NACM\) component, which replaces the deprecated AI Summary Card component on the Claim Workspace and Claim Summary pages. Claims processors and adjusters can continue to generate an AI-generated summary of a claim: processors see it on the Claim Summary page, and adjusters see it on both the Claim Workspace and Claim Summary pages.

    Share a generated summary to the claim's work notes from the summary component. Selecting **Share** opens an editable work notes dialog, where adjusters can edit the summary text before selecting **Save to work notes**.

    Activate the Claim Summarization skill configuration for the summary component to appear on either page. If the skill configuration isn't active, the component doesn't display on either page.


