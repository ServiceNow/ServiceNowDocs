---
title: Automating vaccine response reviews
description: Your organization can automatically validate and review vaccine responses with Vaccination Status by integrating third-party validator services and enabling workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Automating vaccine response reviews

Your organization can automatically validate and review vaccine responses with Vaccination Status by integrating third-party validator services and enabling workflows.

Organizations may want methods to reduce the effort required to validate or approve vaccine responses in bulk. You can choose to automatically validate attachments used in vaccine reviews or automate the entire review process.

## Validating vaccine responses

Validation systems work with Vaccination Status to review attachments in a user's vaccine response. First, the user attaches a supported attachment type, such as a SMART health card, and submits their vaccine response. The validator service API and the Vaccination Status flows analyze information from the attachment to see whether there is a match on the following items:

-   First and last name
-   Date received
-   Vaccine code, such as CVX, to verify the vaccine manufacturer

For more information on submitting a vaccine response, see [Report vaccination status to your organization](../task/report-vaccination-status.md).

The validation process creates work notes on the vaccine response record about the validation process to inform you whether the review was completed, and if not, why. You can also see a user's vaccine response record that details each attachment reviewed.

**Note:** Work notes might not be comprehensive. If validation failed, you might want to investigate further to ensure that other information isn't also mismatched.

Once the validation is completed, you can review the vaccine response record to approve or deny the response. For more information on manually reviewing a vaccine response or confirming whether the validator service is working, see [Confirm the reported vaccination status for a user](../task/confirm-vaccine-response.md).

To automate the validation process, you must do the following:

-   Obtain credentials to integrate with the validator service of your choice.
-   Create a connection and credentials alias for the validator service. For more information, see Create a Connection and Credential alias.
-   Create a record for the validator service.
-   Create a record for the attachment type the vaccine codes can be read from, such as a SMART health card.
-   Create a subflow for the validator service. \(A sample Validate vaccine response attachment template is available\).
-   Configure a vaccine code system used to read vaccine codes and validate submitted data. Some systems are included with Vaccination Status. Refer to your validator service for more information on the system they support.
-   Configure a list of vaccine codes used by the vaccine code system. Some commonly supported codes are included with Vaccination Status.

    **Note:** Other commonly supported codes are provided by the Centers for Disease Control and Prevention \(CDC\). For more information, see [COVID-19 Vaccine Related Codes](https://www.cdc.gov/vaccines/programs/iis/COVID-19-related-codes.html).

-   Activate the Auto-validate vaccine response flow to update the status of vaccine response reviews.

## Automating Vaccine response reviews

Vaccination Status can automatically approve vaccine responses based on valid documentation and supported vaccine codes. Unapproved responses are left in the **Not yet reviewed** state so that Vaccination Status administrators or managers \(if enabled\) can perform a manual review.

To enable the automation of reviews, you must do the following:

-   Configure Vaccination Status to automatically validate vaccine responses.
-   Activate the **Allow validation engine approvals to update Vaccine Review Outcome records** property.

For more information on automating vaccine response reviews, see [Automate reviews of vaccine responses](../task/enable-automated-vaccine-response-reviews.md).

## Provided services and integrations

<table id="table_uj1_hk3_wrb"><thead><tr><th>

Validator services

</th><th>

Integration details

</th></tr></thead><tbody><tr><td>

The CommonTrust Network

</td><td>

The CommonTrust Network is a supported integration and validator service in Vaccination Status. The following items are provided and supported by Vaccination Status to streamline the integration process for the CommonTrust Network:

-   An existing subflow, CommonTrust Network: Validate SMART Health Card
-   Records for CVX vaccine codes and the SMART health card vaccine system
-   SMART health card is available as an attachment type and linked to the CommonTrust Network validator service

 You must still obtain credentials for your organization to provide in the CommonTrust Network record. For more information on SMART health cards, see [SMART Health Cards: Vaccination &amp; Testing Implementation Guide](https://build.fhir.org/ig/HL7/fhir-shc-vaccination-ig/vaccination.html#identifying-vaccines).

 If you want to automate vaccine response reviews, see [Automate reviews of vaccine responses](../task/enable-automated-vaccine-response-reviews.md).

</td></tr><tr><td>

Azure Form Recognizer service

</td><td>

Vaccination Status can integrate with Azure Form Recognizer. This integration enables the Azure Form Recognizer service to act as an alternate vaccine validation service. The Azure Form Recognizer service reads CDC Vaccination Cards and utilizes a trained machine-learning \(ML\) service, or model, to determine if there is a match for the user submitting the vaccine response.

 Validity is by the first and last name as each of these fields generates a confidence score provided by the Azure Form Recognizer service. This score is compared to the confidence threshold set in Vaccination Status.

 For more information, see [Automating vaccine response reviews with the Azure Form Recognizer service](automate-vaccine-validation-with-azure-form-recognizer.md).

 To configure Vaccination Status to use the Azure Form Recognizer service, see [Configure Azure Form Recognizer integration for automatic vaccine response reviews](../task/config-azure-form-recognizer-integration.md).

</td></tr></tbody>
</table>