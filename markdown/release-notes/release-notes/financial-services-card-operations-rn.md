---
title: Financial Services Card Operations release notes
description: The ServiceNow Financial Services Card Operations application enables dispute agents to expedite dispute resolutions by providing the required data and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Financial Services Card Operations release notes

The ServiceNow® Financial Services Card Operations application enables dispute agents to expedite dispute resolutions by providing the required data and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Australia release.

## Financial Services Card Operations highlights for the Australia release

-   Streamline dispute document submission to Mastercard with the document attachment and validation enhancement.
-   Improve dispute resolution accuracy with updated internal policy rules that evaluate the dispute amount rather than the original transaction amount.

See [Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-ops-landing-page.md) for more information.

**Important:** Financial Services Card Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **[Automated document submission in Mastercard transaction dispute process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/chargeback-stage-mastercard.md)**

    Streamline the submission of supporting documents to Mastercard in the Mastercard Dispute Management workflow through document attachment and validation. Attached files are automatically checked against Mastercard requirements for file type and size. This update reduces the need for manual intervention, minimizes rework, and helps avoid rejection risk.

-   **[New subflow and action to support Card data security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-data-security.md)**

    Support attaching documents to a specified table record using the following subflow and action in Card data security:

    -   Attach Document to Table Record
    -   Attach Tokenized Document to Table Record
-   **[Internal policy rule evaluation using dispute amount](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-decision-tables.md)**

    Internal policy rules in the **Card dispute rules for internal policy** decision table now evaluate using the dispute amount instead of the original transaction amount. Previously, if a cardholder or agent modified the disputed amount while answering additional transactional questions during intake, policy rules still evaluated against the original transaction value. Rules now use the dispute amount field \(**sn\_bom\_credit\_card\_disputes\_transaction.dispute\_amount**\), so any amount adjustments made during intake are correctly reflected in rule outcomes.


## Activation information

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Financial Services Operations Integration with Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-mastercard-landing-page.md)**

    The ServiceNow® Financial Services Operations Integration with Mastercard application enables financial institutions to manage the complete Mastercard dispute process from start to closure, including automated document submission.

-   **[Card Data Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-data-security.md)**

    Card data security provides a tokenizer service to tokenize and detokenize data for Dispute Cases and Dispute Transactions to meet Payment Card Industry \(PCI\) requirements.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/financial-services-operations-rn-landing.md)

