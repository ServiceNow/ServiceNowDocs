---
title: Automating vaccine response reviews with the Azure Form Recognizer service
description: Your organization can automatically review and validate vaccine responses with Vaccination Status by integrating with the Azure Form Recognizer service.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Automating vaccine response reviews, Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Automating vaccine response reviews with the Azure Form Recognizer service

Your organization can automatically review and validate vaccine responses with Vaccination Status by integrating with the Azure Form Recognizer service.

## Validating vaccine responses with confidence scores

Vaccination Status can work with the Azure Form Recognizer Service to approve vaccine responses or flag them for further review. Use your own trained machine-learning \(ML\) service from Azure to read Centers for Disease Control and Prevention \(CDC\) Vaccine Cards or use the trained model provided by the ServiceNow® platform. If you use your own model, the fields compared must exactly match the names expected in the validation code. Currently, those fields are the **First Name** and **Last Name** fields.

-   For more information on Azure Form Recognizer service, see [Azure Form Recognizer documentation](https://docs.microsoft.com/en-us/azure/applied-ai-services/form-recognizer/).
-   For more information on the Azure Form Recognizer API used by default, see [Form Recognizer 2021-09-30-preview](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v3-0-preview-1/operations/CopyDocumentModelTo).

When the Azure Form Recognizer service reads the uploaded CDC Vaccination Card, it generates a confidence score for each field. The confidence score is compared to the confidence threshold set by a Vaccination Status administrator in Vaccination Status. With a validation engine, the confidence threshold is used to approve or flag the user's response and update their vaccine profile.

-   If the uploaded vaccination card passes the confidence threshold and matches the name on the user's vaccine profile, the vaccine response is approved.

-   If the uploaded vaccination card has a name that does not match, the outcome of the review in the vaccine profile is updated to require a review \(**Not yet reviewed**\).


For more information on the validation engine used with the validator services, see the following topics:

-   [Automate reviews of vaccine responses](../task/enable-automated-vaccine-response-reviews.md)
-   [Set up Vaccination Status properties](../task/config-vaccination-properties.md)

## Integration details

The following items are provided and supported by Vaccination Status to streamline the integration process:

-   An existing sub-flow, Azure Form Recognizer: Validate vaccination card
-   CDC Vaccination Card is available as an attachment type and linked to the Azure Form Recognizer validator service

    **Note:** You must still obtain credentials for your organization to provide in the Azure Form Recognizer connection alias.

-   A trained model that you can use when setting up your integration

For more information on integrating with the service and enabling automatic reviews, see [Configure Azure Form Recognizer integration for automatic vaccine response reviews](../task/config-azure-form-recognizer-integration.md).

