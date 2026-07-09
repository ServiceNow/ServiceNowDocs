---
title: Configure quote document generation
description: The Generate PDF Document feature generates a PDF document of the current quote based on the selected template. After the document is generated, it is available in the Attachments section of the Contextual Side Panel \(CSP\). To enable this feature, an administrator configures a custom integration and a custom event that initiate the document generation process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-generate-document.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure quote document generation

The Generate PDF Document feature generates a PDF document of the current quote based on the selected template. After the document is generated, it is available in the **Attachments** section of the Contextual Side Panel \(CSP\). To enable this feature, an administrator configures a custom integration and a custom event that initiate the document generation process.

## Before you begin

Role required: admin

Before you configure the document generation feature, complete the following instance setup:

1.  Activate the Quote Experience plugin \(App ID: sn\_quote\_mgmt\_adv\).
2.  Submit a support ticket requesting to enable the **Document Generation** tenant setting.
3.  When the tenant setting is enabled, export and import the transaction blueprint.

You must also create a document template before you configure this feature. Document templates are created and managed outside ServiceNow CPQ Administration. For instructions, see [Configure quote PDF documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management-configure-pdf-documents.md).

## About this task

The document generation feature uses the following system fields to determine the template and signers for the generated document.

|Type|Display name|Variable name|
|----|------------|-------------|
|Field|Document Template|`txn.docGen.template`|
|Field|Document External Signer|`txn.docGen.externalSigner`|
|Field|Document Internal Signer|`txn.docGen.internalSigner`|

To configure the feature, update the system fields, create a custom integration and a custom event in the blueprint, and then deploy the blueprint. Complete the following phases in order.

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction**.

2.  On the blueprint, select **Fields**.

3.  For each system field listed in the preceding table, set the **Default Access** to **Editable**.

4.  Add each system field to the transaction layout.

5.  Create a custom integration.

    For more information, see [Quote transaction integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-integrations.md)

6.  Configure the following integration settings.

    |Setting|Value|
    |-------|-----|
    |HTTP Method|`POST`|
    |Additional Path|`/api/sn_quote_mgmt_adv/v1/quotes/{{txn.id}}/documents`|
    |Timeout|`5000`|
    |Line Item Details to Include|None|
    |Async|Disabled|
    |Headers|Not applicable|

7.  Leave the **Request Transformation** unconfigured.

    No request transformation is required for this integration.

8.  For **Connection to Endpoint**, select **serviceNowJwtConnection**.

9.  Leave the **Response Transformation** unconfigured.

    No response transformation is required for this integration.

10. Create a custom event.

11. In the event properties, set **Event Access** to **Active**.

12. Associate the integration you created with the event.

13. Add a button to the layout to trigger the event.

    1.  Enable the event button.

    2.  From the **Event** picklist, select the event you created in Phase 3.

14. In **Views**, adjust the access to the event for each stage.

15. Select **Save**.

16. Select **Deploy** to deploy the blueprint.


## Result

When a user selects the generate-document button on a quote, the integration generates a PDF document from the selected template and attaches it to the quote. The document is available in the **Attachments** section of the Contextual Side Panel \(CSP\).

