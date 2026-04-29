---
title: Configure Azure Form Recognizer integration for automatic vaccine response reviews
description: As a Vaccination Status admin, configure Vaccination Status to work with Azure Form Recognizer service and automate vaccine response approvals.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Automating vaccine response reviews with the Azure Form Recognizer service, Automating vaccine response reviews, Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure Azure Form Recognizer integration for automatic vaccine response reviews

As a Vaccination Status admin, configure Vaccination Status to work with Azure Form Recognizer service and automate vaccine response approvals.

## Before you begin

To integrate with the Azure Form Recognizer service, you should do the following:

-   Use Azure Form Recognizer and obtain connection credentials
-   Train a machine-learning model if you are using your organization's own model for validation purposes

Role required: sn\_imt\_vaccine.admin

## About this task

When you add your credentials to connect to the Azure Form Recognizer service, you may choose to use a ServiceNow -trained model or a model created by your organization.

-   For more information on Azure Form Recognizer service, see [Azure Form Recognizer documentation](https://docs.microsoft.com/en-us/azure/applied-ai-services/form-recognizer/).
-   For more information on the Azure Form Recognizer API used by default, see [Form Recognizer 2021-09-30-preview](https://westus.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v3-0-preview-1/operations/CopyDocumentModelTo).

## Procedure

1.  Enable the **Allow validation engine approvals to update Vaccine Review Outcome records** property to automate the approvals of vaccine responses.

    1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Properties**.

    2.  Locate the **Allow validation engine approvals to update Vaccine Review Outcome records** property and select **Yes**.

2.  Configure the Azure Recognizer service confidence threshold property used to validate Centers for Disease Control and Prevention \(CDC\) Vaccination Cards.

    The value in this step is the confidence level required by the service to determine that a submitted CDC Vaccination Card matches the user.

    1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Properties**.

    2.  Navigate to the **Azure Form Recognizer confidence threshold, a decimal value between 0 and 1** \[sn\_imt\_vaccine.azure\_form\_recognizer\_confidence\_threshold\] property.

    3.  Enter a decimal value to represent the confidence threshold required for a vaccine response to match.

    4.  Select **Save**.

3.  Add your connection credentials and trained model to the Azure Form Recognizer validator service.

<table id="choicetable_gy1_qhr_4sb"><thead><tr><th align="left" id="d668261e219">

Trained model

</th><th align="left" id="d668261e222">

Steps

</th></tr></thead><tbody><tr><td id="d668261e228">

**ServiceNow model**

</td><td>

-   Add your connection credentials.
    1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Validator services**.
    2.  Select **Azure Form Recognizer**.
    3.  Open the sn\_imt\_vaccine.Azure\_Form\_Recognizer connection and credential alias.
    4.  Select **Create New Connection and Credential**.
    5.  Replace the Connection URL with the URL from your Azure Form Recognizer resource. For more information, see [Create a Form Recognizer resource](https://docs.microsoft.com/en-us/azure/applied-ai-services/form-recognizer/create-a-form-recognizer-resource).
    6.  Enter a Model ID to use for your copy of the trained model in Azure Form Recognizer.
    7.  Enter your API subscription key from your Azure Form Recognizer resource.
    8.  Select **Create**.
-   Generate a model copy authorization with customer support or your account management team.

**Note:** Contact ServiceNow Customer Service and Support or your account management team for "Vaccination Status – Azure Integration setup support". ServiceNow Customer Service and Support and your account management team can complete the steps required to add the trained model with you. Model copy authorizations only last for an hour.

</td></tr><tr><td id="d668261e324">

**Customer-trained model**

</td><td>

1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Validator services**.
2.  Select **Azure Form Recognizer**.
3.  Open the sn\_imt\_vaccine.Azure\_Form\_Recognizer connection and credential alias.
4.  Select **Create New Connection and Credential**.
5.  Replace the Connection URL with the URL your Azure Form Recognizer resource. For more information, see [Create a Form Recognizer resource](https://docs.microsoft.com/en-us/azure/applied-ai-services/form-recognizer/create-a-form-recognizer-resource).
6.  Enter your Model ID from the trained model in Azure Form Recognizer.
7.  Enter your API subscription key from your Azure Form Recognizer resource.
8.  Select **Create**.


</td></tr></tbody>
</table>4.  Activate the Auto-validate vaccine response flow.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Search for the Auto-validate vaccine response flow.

    3.  Select the flow.

    4.  Select **Activate**.


## Result

When users add CDC Vaccination Card attachments to their vaccine responses and set the attachment type to CDC Vaccination Card, the following occurs:

-   The card is read by the Azure Form Recognizer service and trained machine-learning \(ML\) model
-   A confidence score is generated
-   The confidence score is compared to the configured threshold
-   The validation engine sets the Vaccine Review Outcomes based on whether the first and last names matched

**Parent Topic:**[Automating vaccine response reviews with the Azure Form Recognizer service](../concept/automate-vaccine-validation-with-azure-form-recognizer.md)

