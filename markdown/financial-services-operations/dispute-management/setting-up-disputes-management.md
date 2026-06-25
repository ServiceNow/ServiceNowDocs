---
title: Set up Dispute Management
description: Set up your Dispute Management implementation by installing the required plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/setting-up-disputes-management.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up Dispute Management

Set up your Dispute Management implementation by installing the required plugins.

## Configuration overview

-   [Install Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-card-operations/install-fso-card-ops.md)

    Set up your implementation for Financial Services Card Operations by installing the application, importing financial services data, and reviewing and configuring the application's components.

-   [Set up Visa Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-visa-spoke.md)

    Install Visa Spoke if Visa is your card payment network provider. Use the spoke to manage card disputes with Visa Resolve Online \(VROL\). Leverage Visa Spoke actions to perform transaction inquiry, order insight digital, collaborate with merchants, and perform other functions with enhanced security.

-   [Install Financial Services Operations Integration with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/install-financial-services-operations-integration-with-visa.md)

    Install the Visa Integration plugin if Visa is your card payment network provider. This plugin installs Visa Spoke which is a dependent plugin if it is not already installed. Manage dispute lifecycle with events like case creation and submit questionnaires amongst others. Data model elements to capture the information used at sub-flows.

-   [Install the Dispute Rules Content Pack for Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/install-dispute-rules-content-pack-for-visa.md)

    Dispute Rules Content Pack for Visa provides the questionnaire for intake of a dispute and dispute categorization rules as per Visa guidelines. Run chargeback eligibility rules based on Visa Core Rules and Visa Product and Service Rules.

-   [Set up Verifi Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-verifi-spoke.md)

    Use Verifi Spoke to integrate with the Verifi CDRN API suite and perform API calls to perform early dispute resolution.

-   [Set up Mastercard spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-mastercard-spoke.md)

    Install Mastercard Spoke if Mastercard is your card payment network provider. Use the spoke to manage card disputes with Mastercard. Leverage Mastercard spoke actions, to perform transaction inquiry, order insight digital, collaborate with merchants, and perform other functions with enhanced security.

-   [Set up Ethoca spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-ethoca-spoke.md)

    Use the Ethoca spoke to integrate with Ethoca Consumer Clarity APIs.

-   [Install the Dispute Rules Content Pack for Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/install-the-dispute-rules-content-pack-for-mastercard.md)

    Dispute Rules Content Pack for Mastercard provides the questionnaire for intake of a dispute and dispute categorization rules as per Mastercard guidelines. Run chargeback eligibility rules based on Mastercard Rules.

-   [Install the Dispute Content Pack for US Regulations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/install-the-dispute-content-pack-for-us-regulations.md)

    Dispute Content Pack for US Regulations supports monitoring dispute cases effectively and take necessary actions. This application provides SLA definitions pertaining to Regulation E \(Reg E\) and Regulation Z \(Reg Z\) and tracks the dispute cases during the life cycle. Provides SLA definitions for dispute management applications and landing page metrics to track dispute cases that are under risk or breached.

-   [Install the Dispute Rules Content Pack for Nacha](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/dispute-rules-content-pack-nacha-install.md)

    The Dispute Rules Content Pack for Nacha gives agents access to Nacha operating guidelines to check the eligibility of disputed automated clearing house \(ACH\) transactions. It provides a central reference for ACH return reason codes and the logic used to determine them based on the operating guidelines.

-   [Install and configure Card data security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/configuring-card-data-security.md)

    Card data security helps organizations adhere to Payment Card Industry Data Security Standard \(PCI DSS\) requirements by protecting cardholder data. It provides a tokenizer service that substitutes sensitive data in dispute workflows—such as Primary Account Numbers \(PANs\) and documents—with non-sensitive equivalent values called tokens.

-   [Install Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/configure-now-assist-for-fso.md)

    Install Now Assist for Financial Services Operations \(FSO\) to leverage agentic and generative AI capabilities.


-   **[Configure additional questions for dispute intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/configuring-additional-questions-for-dispute-intake.md)**  
Configure the questionnaire that appears for dispute agents or account holders when they initiate a dispute.

**Parent Topic:**[Dispute Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/dispute-management.md)

**Related topics**  


[Card Disputes data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-data-model.md)

