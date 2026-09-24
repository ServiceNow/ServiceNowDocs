---
title: Financial Services Operations Integration with Visa release notes
description: The ServiceNow Financial Services Operations Integration with Visa application enables integration with workflow applications, such as the card operations dispute management playbook with Visa Resolve Online \(VROL\) subflows. See the following sections for release notes by version.Align the Visa dispute questionnaire subflows with Visa IES release 26.2, revisions 1 and 2. Dispute agents see accurate field labels, validation, and Spoke action wiring.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/financial-services-operations-integration-with-visa-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Financial Services Operations Integration with Visa, Visa Resolve Online, dispute resolution, card operations, dispute management, fraud reporting, dispute questionnaire, financial services, workflow integration, release notes, Visa, dispute questionnaire, IES, Interface Elements Specification, subflows, field labels, validation, Spoke actions, financial services]
audience: [administrator, developer]
breadcrumb: [Financial Services Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Financial Services Operations Integration with Visa release notes

The ServiceNow® Financial Services Operations Integration with Visa application enables integration with workflow applications, such as the card operations dispute management playbook with Visa Resolve Online \(VROL\) subflows. See the following sections for release notes by version.

## About Financial Services Operations Integration with Visa

-   Provides the framework for supporting dispute resolution use cases on ServiceNow which requires integration with VROL.
-   Use predefined subflows to address primary integrations such as creating a dispute case, reporting fraud, and submitting a dispute questionnaire.

See [Financial Services Operations Integration with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/financial-services-operations-integration-with-visa-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Financial Services Operations Integration with Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/financial-services-operations-rn-landing.md)

## Version 5.1.1

Align the Visa dispute questionnaire subflows with Visa IES release 26.2, revisions 1 and 2. Dispute agents see accurate field labels, validation, and Spoke action wiring.

### What's changed

-   **Updated questionnaire field labels and validation**

    Renamed the question "Explain why credit presented does not apply" to "Provide the Transaction Identifier\(s\) or Acquirer Reference Number\(s\) and the Transaction Date that the credit\(s\) was applied to and why the credit\(s\) does not resolve the Dispute," and renamed "Certification that the merchant facilities were withdrawn" to "Certification that the facilities were withdrawn." The Name field is no longer required, and Key Factors now accepts up to 200 characters.

-   **Updated Spoke action wiring for new questionnaire fields**

    Added the Date facilities were withdrawn and Date cardholder checked out from hotel fields to the `Submit Dispute Questionnaire` and `Look up Dispute Details Response Parser` spoke actions, and added CE Transaction Details as a read-back field on `Look up Dispute Details Response Parser`. See [Financial Services Card Operations 2026 September Monthly release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/financial-services-card-operations-rn.md) for the corresponding questionnaire questions.


