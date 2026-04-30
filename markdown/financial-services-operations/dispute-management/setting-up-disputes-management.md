---
title: Set up Dispute Management
description: Set up your Dispute Management implementation by installing the required plugins.
locale: en-US
release: zurich
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up Dispute Management

Set up your Dispute Management implementation by installing the required plugins.

## Configuration overview

-   [Install Financial Services Card Operations](../../fso-card-operations/task/install-fso-card-ops.md)

    Set up your implementation for Financial Services Card Operations by installing the application, importing financial services data, and reviewing and configuring the application's components.

-   [Set up Visa Spoke](https://www.servicenow.com/docs/access?context=set-up-visa-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

    Install Visa Spoke if Visa is your card payment network provider. Use the spoke to manage card disputes with Visa Resolve Online \(VROL\). Leverage Visa Spoke actions to perform transaction inquiry, order insight digital, collaborate with merchants, and perform other functions with enhanced security.

-   [Install Financial Services Operations Integration with Visa](../../fso-visa-spoke/task/install-financial-services-operations-integration-with-visa.md)

    Install the Visa Integration plugin if Visa is your card payment network provider. This plugin installs Visa Spoke which is a dependent plugin if it is not already installed. Manage dispute lifecycle with events like case creation and submit questionnaires amongst others. Data model elements to capture the information used at sub-flows.

-   [Install the Dispute Rules Content Pack for Visa](../../dispute-content-pack-for-visa/task/install-dispute-rules-content-pack-for-visa.md)

    Dispute Rules Content Pack for Visa provides the questionnaire for intake of a dispute and dispute categorization rules as per Visa guidelines. Run chargeback eligibility rules based on Visa Core Rules and Visa Product and Service Rules.

-   [Set up Verifi Spoke](https://www.servicenow.com/docs/access?context=set-up-verifi-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

    Use Verifi Spoke to integrate with the Verifi CDRN API suite and perform API calls to perform early dispute resolution.

-   [Set up Mastercard spoke](https://www.servicenow.com/docs/access?context=set-up-mastercard-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

    Install Mastercard Spoke if Mastercard is your card payment network provider. Use the spoke to manage card disputes with Mastercard. Leverage Mastercard spoke actions, to perform transaction inquiry, order insight digital, collaborate with merchants, and perform other functions with enhanced security.

-   [Set up Ethoca spoke](https://www.servicenow.com/docs/access?context=set-up-ethoca-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

    Use the Ethoca spoke to integrate with Ethoca Consumer Clarity APIs.

-   [Install the Dispute Rules Content Pack for Mastercard](../../dispute-content-pack-for-mastercard/task/install-the-dispute-rules-content-pack-for-mastercard.md)

    Dispute Rules Content Pack for Mastercard provides the questionnaire for intake of a dispute and dispute categorization rules as per Mastercard guidelines. Run chargeback eligibility rules based on Mastercard Rules.

-   [Install the Dispute Content Pack for US Regulations](../../dispute-content-pack-US-regulation/task/install-the-dispute-content-pack-for-us-regulations.md)

    Dispute Content Pack for US Regulations is designed to support monitoring dispute cases effectively and take necessary actions. This application provides SLA definitions pertaining to Regulation E \(Reg E\) and Regulation Z \(Reg Z\) and tracks the dispute cases during the life cycle. Provides SLA definitions for dispute management applications and landing page metrics to track dispute cases that are under risk or breached.

-   [Install Now Assist for Financial Services Operations \(FSO\)](../../fso-common/task/configure-now-assist-for-fso.md)

    Install Now Assist for Financial Services Operations \(FSO\) to leverage generative AI capabilities.

    -   [Configure case summarization in Now Assist for Financial Services Operations \(FSO\)](../../fso-common/task/configure-now-assist-for-fso.md)
    -   [Configure Disputes intake via Virtual Agent in Now Assist for Financial Services Operations \(FSO\)](../../fso-now-assist/task/configuring-disputes-intake-via-virtual-agent.md)

-   **[Configure additional questions for dispute intake](../../fso-card-operations/task/configuring-additional-questions-for-dispute-intake.md)**  
Configure the questionnaire that appears for dispute agents or account holders when they initiate a dispute.

**Parent Topic:**[Dispute Management](../../fso-card-operations/concept/dispute-management.md)

**Related topics**  


[Card Disputes data model](../../fso-card-operations/reference/dispute-data-model.md)

