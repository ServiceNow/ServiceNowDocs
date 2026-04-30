---
title: Managing payment inquiries
description: Using the payment inquiry capability of the Financial Services Payment Operations application, you can submit and manage payment inquiry requests that you receive from your customers and third-party banks for your financial institution. The application supports both personal and business claims and debits.
locale: en-US
release: yokohama
product: Financial Services Payment Operations
classification: financial-services-payment-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Payment Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Managing payment inquiries

Using the payment inquiry capability of the Financial Services Payment Operations application, you can submit and manage payment inquiry requests that you receive from your customers and third-party banks for your financial institution. The application supports both personal and business claims and debits.

Inquiry agents in the middle and back office receive inquiries from customers as well as external banks.

-   Internal inquiries: These inquiries come from a bank's customers. The payment recipient could be either internal or external to the bank, which determines how an inquiry is resolved.
-   External inquiries: These inquiries come from third-party banks, which means that the payment recipient is always internal.

## Types of payment inquiries

The application enables creating the following types of payment inquiries:

-   Beneficiary Claim Non-Receipt \(BCNR\): The customer has sent a payment but the recipient claims that they didn't receive the money. These inquiries can be internal or external.
-   Payment in Error \(PiE\): The customer made a mistake when sending a payment and is trying to retrieve the money.

## How to initiate payment inquiries

-   **Internal inquiries**

    For internal inquiries such as Beneficiary Claim Non-Receipt - Internal and Payment made In Error:

    -   Branch workers and call center agents can create these requests on behalf of their customers from interaction records and the service catalog.
    -   Business customers and consumers can create these requests from the Customer Service Portal and Consumer Service Portal respectively by selecting catalog items and filling out and submitting forms.
-   **External inquiries**

    Inquiry agents can create inquiry cases for external inquiries such as Beneficiary Claim Non-Receipt - External.


## Assignment and resolution for payment inquiries

After an inquiry case is created from a submitted request, it is assigned to an assignment group or inquiry agent using assignment rules. Inquiry agents handle the next steps such as investigating the case, sending emails for requesting information from the recipient bank, and proposing a solution for the case.

Some internal inquiries can also result in the creation of a claim.

-   **[Create a payment inquiry case for an external inquiry](../task/create-payment-inquiry-case-external-inquiry.md)**  
As an inquiry agent, you can create an inquiry case for an external inquiry that you receive from a third-party bank.
-   **[Submit a payment inquiry request for an internal inquiry](../task/submit-payment-inquiry-request.md)**  
As a front-office worker \(branch employee or call center agent\), you can submit a payment inquiry request on behalf of a customer.
-   **[Assign a payment inquiry case](../task/assign-payment-inquiry-case.md)**  
Assign a payment inquiry case to yourself or to another inquiry agent so that you or another agent can start investigating the case.
-   **[Investigate a payment inquiry case](../task/investigate-payment-inquiry-case.md)**  
Investigate the payment inquiry case so that you can get enough information about the case to resolve it.
-   **[Propose a solution for an inquiry case](../task/propose-solution-inquiry-case.md)**  
Propose a solution that is based on your findings from the investigation of the inquiry case that you've just finished, so that you can resolve the case.
-   **[Close a payment inquiry case](../task/close-payment-inquiry-case.md)**  
Close the case after you've created a claim case for the inquiry case or the customer has accepted your proposed solution.

**Parent Topic:**[Financial Services Payment Operations](payment-ops-landing-page.md)

