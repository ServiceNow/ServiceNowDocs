---
title: Set up Dispute Management
description: Configure Dispute Management to process card payment network and ACH disputes. Installation requirements vary by network provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/setting-up-disputes-management.html
release: brazil
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-09-16"
reading_time_minutes: 5
breadcrumb: [Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up Dispute Management

Configure Dispute Management to process card payment network and ACH disputes. Installation requirements vary by network provider.

First, set up your implementation for Financial Services Card Operations by [installing Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/financial-services-card-operations/install-fso-card-ops.md), importing financial services data, and reviewing and configuring the application's components. This is a prerequisite for all card payment networks and ACH disputes covered in this topic.

**Note:**

Financial Services Operations Core is installed with Financial Services Card Operations.

Next, complete the section for your card payment network \(Visa or Mastercard\) or for Nacha ACH disputes.

|Network|Required|Optional|
|-------|--------|--------|
|Visa|Visa Spoke, Financial Services Operations Integration with Visa, Dispute Rules Content Pack for Visa|Verifi Spoke, Ethoca spoke, Card Data Security|
|Mastercard|Mastercard Spoke, Financial Services Operations Integration with Mastercard, Dispute Rules Content Pack for Mastercard|Verifi Spoke, Ethoca spoke, Card Data Security|
|Nacha|Dispute Rules Content Pack for Nacha| |

## Visa

Complete these steps if Visa is your card payment network provider.

1.  [Install Financial Services Operations Integration with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/install-financial-services-operations-integration-with-visa.md)

    Install the Visa Integration plugin to manage the dispute lifecycle with events like case creation and questionnaire submission, among others. This plugin also captures data model elements used at sub-flows.

    Visa Spoke and Dispute Rules Content Pack for Visa will also be installed as dependent plugins if they aren't already installed.

    -   Visa Spoke actions to perform transaction inquiry, order insight digital, collaborate with merchants, and perform other functions with enhanced security.
    -   Dispute Rules Content Pack for Visa provides the dispute categorization rules according to Visa guidelines. Run chargeback eligibility rules based on Visa Core Rules and Visa Product and Service Rules.
2.  

    Set up Visa Spoke to enable your organization to manage card disputes and card-on-file payments through Visa APIs. The spoke provides secure access to Visa Resolve Online \(VROL\) for dispute management and Visa Stop Payment Service \(VSPS\) for payment controls. This enables you to search transactions, collaborate with merchants, manage dispute cases, and control card-on-file payments.


## Mastercard

Complete these steps if Mastercard is your card payment network provider.

1.  [Install Financial Services Operations Integration with Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/install-financial-services-operations-integration-with-mastercard.md)

    Install the Mastercard Integration plugin to manage the dispute lifecycle with events like case creation and questionnaire submission, among others. This plugin also captures data model elements used at sub-flows.

    Mastercard Spoke and Dispute Rules Content Pack for Mastercard will also be installed as dependent plugins if they aren't already installed.

    -   Mastercard Spoke actions perform transaction inquiry, order insight digital, collaborate with merchants, and perform other functions with enhanced security.
    -   Dispute Rules Content Pack for Mastercard provides dispute categorization rules according to Mastercard guidelines. You can run chargeback eligibility rules based on Mastercard Rules.
2.  

    Set up Mastercard Spoke to enable your organization to manage card disputes and automate dispute lifecycle events through Mastercard APIs. This integration streamlines transaction searches, claim creation, chargeback processing, and merchant collaboration, reducing manual effort and improving dispute resolution accuracy.


## NACHA

[Install the Dispute Rules Content Pack for Nacha](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/dispute-rules-content-pack-nacha-install.md) if you need to support disputes involving automated clearing house \(ACH\) transactions.

The Dispute Rules Content Pack for Nacha gives agents access to Nacha operating guidelines to check the eligibility of disputed ACH transactions. It provides a central reference for ACH return reason codes and the logic used to determine them based on the operating guidelines.

## Card data tokenization

If you require PCI DSS tokenization for Visa or Mastercard cardholder data, install Card data security \(see [Configuring Card Data Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/configuring-card-data-security.md)\) after you install the corresponding network integration plugin. Network-specific artifacts install only when that integration plugin is present. This step is optional and doesn't apply to Nacha ACH disputes.

## Common configuration

The following components apply regardless of which card payment network or ACH provider you use. Install them based on your organization's regulatory scope and desired capabilities; none are required for the base dispute management implementation.

-   

    Use Verifi Spoke to integrate with the Verifi CDRN API suite and perform early dispute resolution.

-   

    Use the Ethoca spoke to integrate with Ethoca Consumer Clarity APIs for early dispute resolution and fraud prevention.

-   [Install the Dispute Content Pack for US Regulations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/install-the-dispute-content-pack-for-us-regulations.md)

    If you're a US-based issuer subject to Regulation E or Regulation Z, install Dispute Content Pack for US Regulations to automatically track federal SLA deadlines instead of monitoring them manually. It supplies SLA definitions and landing page metrics so dispute agents and managers can identify cases that are at risk of, or have breached, a regulatory deadline. Requires Financial Services Card Operations to already be installed and active.

-   [Configure ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/configure-now-assist-for-fso.md)

    Configure ServiceNow Otto for Financial Services Operations \(FSO\) to leverage agentic and generative AI capabilities.


-   **[Configure additional questions for dispute intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/configuring-additional-questions-for-dispute-intake.md)**  
Configure the questionnaire that appears for dispute agents or account holders when they initiate a dispute.
-   **[Configure Disputes intake via Virtual Agent in ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/configuring-disputes-intake-via-virtual-agent.md)**  
If you have the admin role, you can configure Disputes intake via Virtual Agent in ServiceNow Otto for Financial Services Operations \(FSO\). This provides a conversational experience for your customers to submit card disputes.
-   **[Help resolve friendly fraud disputes agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/friendly-fraud-agentic-ai-workflow.md)**  
Use this agentic workflow to assist human agents with analyzing friendly fraud cases, selecting a course of action, and drafting a decision response to customers.

**Parent Topic:**[Dispute Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-management/dispute-management.md)

**Related topics**  


[Card Disputes data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/financial-services-operations/dispute-data-model.md)

