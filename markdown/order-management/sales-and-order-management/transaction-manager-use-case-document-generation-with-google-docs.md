---
title: Transaction Manager use case: Document generation with Google Docs
description: Generate documents from Transaction Manager by using Google Docs and Google Apps Script.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Transaction Manager: Use cases, Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager use case: Document generation with Google Docs

Generate documents from Transaction Manager by using Google Docs and Google Apps Script.

To generate a document from Transaction Manager, Google Docs combined with Google Apps Script provides an efficient and straightforward solution. By creating custom APIs using Apps Script, you can easily receive GET and POST requests from a direct URL. This eliminates the need for middleware, streamlining integration with services like CPQ or Transaction Manager.

You can trigger document generation by either of these methods:

-   CPQ Webhook: Automatically send POST requests to initiate document creation.
-   Transaction Manager: Use this for managing and automating processes.

## Setting up a Google doc to pull CPQ data

To access the developer window, open the Google doc where you want to integrate the script. In the menu bar, go to Extensions &gt; Apps Script to open the development environment.

You can write custom JavaScript to process data and interact with Google Docs by using the Apps Script editor.

![BOM](../images/cpq-txn-mgr-use-case-doc-gen-script-loc.jpeg)

![Script](../images/cpq-txn-mgr-use-case-doc-gen-script-interface.png)

## Coding

Google Apps Script includes GET and POST requests.

-   GET requests \(`doGet`\) respond with a simple text output, useful for verifying that the web app is running.
-   POST requests \(`doPost`\) handle incoming data \(usually JSON\), generates the document based on the template, and returns a link to the newly created document.

This [video](https://www.youtube.com/watch?v=N3vnUgjQCGU) explains how the `doGet` and `doPost` work in a Google Doc app script.

When using Transaction Manager, you need to transform the JSON to send over to Google Docs. Below is an example template. If you are using a webhook, see [Webhooks](cpq-webhooks.md) for how the data will be sent over to Google Docs.

The following code block shows an example Transform Template, sent as a POST to the doPost function.

```
{ 
  "transaction": { 
    "uuid": "{{txn.uuid}}", 
    "term": {{txn.term}}, 
    "stage": "{{txn.stage}}", 
    "status": "{{txn.status}}", 
    "account": "{{txn.account}}", 
    "endDate": "{{txn.endDate}}", 
    "netTotal": {{txn.netTotal}}, 
    "termUnit": "{{txn.termUnit}}", 
    "createdBy": "{{txn.createdBy}}", 
    "quoteName": "{{txn.quoteName}}", 
    "startDate": "{{txn.startDate}}", 
    "accountName": "{{txn.accountName}}", 
    "createdDate": "{{txn.createdDate}}", 
    "opportunity": "{{txn.opportunity}}", 
    "paymentTerm": "{{txn.paymentTerm}}", 
    "quoteNumber": "{{txn.quoteNumber}}", 
    "contractTerm": {{txn.contractTerm}}, 
    "contractType": "{{txn.contractType}}", 
    "currencyCode": "{{txn.currencyCode}}", 
    "estTaxAmount": {{txn.estTaxAmount}}, 
    "modifiedDate": "{{txn.modifiedDate}}", 
    "billToAddress": "{{txn.billToAddress}}", 
    "hardwareTotal": {{txn.hardwareTotal}}, 
    "servicesTotal": {{txn.servicesTotal}}, 
    "shipToAddress": "{{txn.shipToAddress}}", 
    "softwareTotal": {{txn.softwareTotal}}, 
    "discountAmount": {{txn.discountAmount}}, 
    "expirationDate": "{{txn.expirationDate}}", 
    "lastModifiedBy": "{{txn.lastModifiedBy}}", 
    "primaryContact": "{{txn.primaryContact}}", 
    "customerSegment": "{{txn.customerSegment}}", 
    "discountPercent": {{txn.discountPercent}}, 
    "transactionType": "{{txn.transactionType}}", 
    "estTaxPercentage": {{txn.estTaxPercentage}}, 
    "agreementDiscount": {{txn.agreementDiscount}}, 
    "taxEntityLocation": "{{txn.taxEntityLocation}}", 
    "transactionNumber": {{txn.transactionNumber}}, 
    "totalPriceEstimate": {{txn.totalPriceEstimate}}, 
    "overallDealDiscount": {{txn.overallDealDiscount}}, 
    "annualTransactionBands": "{{txn.annualTransactionBands}}", 
    "annualTransactionCount": {{txn.annualTransactionCount}}, 
    "accountSpecificDiscount": {{txn.accountSpecificDiscount}} 
  },   
  "lines": [
  {{#each lines}} 
    { 
      "uuid": "{{txn.line.uuid}}", 
      "productInfo": {
        "productId": "{{txn.line.productId}}",
        "productSku": "{{txn.line.productSku}}",
        "productCode": "{{txn.line.productCode}}",
        "productName": "{{txn.line.productName}}",
        "productType": "{{txn.line.productType}}",
        "productDescription": "{{txn.line.productDescription}}"
      },
      "pricing": {
        "netPrice": {{txn.line.netPrice}},
        "listPrice": {{txn.line.listPrice}},
        "discountAmount": {{txn.line.discountAmount}},
        "discountPercent": {{txn.line.discountPercent}},
        "netTotal": {{txn.line.netTotal}},
        "customerLineDiscount": {{txn.line.customerLineDiscount}},
        "agreementLineDiscount": {{txn.line.agreementLineDiscount}}
      },
      "dates": {
        "startDate": "{{txn.line.startDate}}",
        "endDate": "{{txn.line.endDate}}",
        "createdDate": "{{txn.line.createdDate}}",
        "modifiedDate": "{{txn.line.modifiedDate}}"
      },
      "quantity": {{txn.line.quantity}},
      "currencyCode": "{{txn.line.currencyCode}}",
      "configUUID": "{{txn.line.configUUID}}",
      "orderDetails": {
        "globalOrder": {{txn.line.globalOrder}},
        "orderNumber": {{txn.line.orderNumber}},
        "transactionLineNumber": {{txn.line.transactionLineNumber}}
      },
      "termDetails": {
        "term": {{txn.line.term}},
        "termUnit": "{{txn.line.termUnit}}",
        "termMultiplier": {{txn.line.termMultiplier}}
      },
      "approvals": "{{txn.line.approvals3}}",
      "lastModifiedBy": "{{txn.line.lastModifiedBy}}"
    }
    {{#unless @last}},{{/unless}} 
  {{/each}}
  ]
}
```

If you do not set the `doGet` function and try to access the URL you will receive an error. If not using the `doGet` for other purposes, it is best to always set it to the following and just modify the text.

```
function doGet(e) {
  return ContentService.createTextOutput('Logik Transaction Manager Document Generation Web App is running.');
}
```

When you access the live URL, you receive this message:

![Message: Logik Transaction Manager Document Generation Web App is running.](../images/cpq-txn-mgr-use-case-doc-gen-msg.png)

The `doPost` is important, because it will probably handle the Webhook or Integration payloads being sent from CPQ via POST requests.

Next, we create a function to generate a Google Doc using the `doPost` function.

In your Google Apps script, the `doPost` function will receive a POST request containing data \(in JSON format\) that you want to populate into a Google Doc template. The main logic for interacting with the Google Doc \(i.e., replacing placeholders like `{{EXAMPLE}}` with actual values\) will be placed in a separate function that is called from `doPost`.

To set up the `doPost` function, define the `doPost` function to handle incoming POST requests and call your custom document generation function. Below is an example of how to structure it.

```
function doPost(e) {
  // Parse the JSON data from the POST request
  const postData = JSON.parse(e.postData.contents);

  // Call the function to create and populate the Google Doc
  const docLink = createGoogleDocFromTemplate(postData);

  // Return the public link to the generated document in the response
  return ContentService.createTextOutput(docLink);
}
```

In this code:

-   The `postData` object contains the parsed data sent in the POST request.
-   `createGoogleDocFromTemplate(postData)` is the function you will define to handle the Google Docs generation.
-   The `docLink` is the public link to the generated Google Doc, returned to the caller.

Next, create the document generation function. The `createGoogleDocFromTemplate` function will:

1.  make a copy of a Google Doc template.
2.  replace placeholders \(e.g., `{{EXAMPLE}}`\) in the document with the corresponding data.
3.  return a public link to the generated document.

The following code block shows an example `createGoogleDocFromTemplate` function:

```
function createGoogleDocFromTemplate(data) {
  // Specify the ID of the Google Doc template
  var templateId = 'YOUR_TEMPLATE_DOC_ID_HERE';
  // Make a copy of the template
  var templateDoc = DriveApp.getFileById(templateId).makeCopy();
  var doc = DocumentApp.openById(templateDoc.getId());
  var body = doc.getBody();
  // Replace placeholders with actual data from the POST request
  body.replaceText('{{ACCOUNT_NAME}}', data.transaction.accountName);
  body.replaceText('{{QUOTE_NUMBER}}', data.transaction.quoteNumber);
  body.replaceText('{{USER}}', data.transaction.createdBy);
  // Continue to replace all other placeholders...
  // Save and close the document
  doc.saveAndClose();
  // Make the document public (optional, based on your needs)
  templateDoc.setSharing(DriveApp.Access.ANYONE, DriveApp.Permission.VIEW);
  // Return the public link to the newly created document
  return templateDoc.getUrl();
}
```

In this function:

-   The templateId variable stores the Google Doc template’s ID. You should replace `'YOUR_TEMPLATE_DOC_ID_HERE'` with the actual ID of your template.
-   `makeCopy()` creates a copy of the template.
-   `replaceText('{{EXAMPLE}}', data.key)` replaces each placeholder in the document with actual data from the incoming POST request. For example, `{{ACCOUNT_NAME}}` is replaced by `data.transaction.accountName`.
-   The document is made public with `setSharing()`, but you can adjust the sharing settings as needed.

## Logging

Google Apps Script offers built-in logging via Logger.log\(\) for debugging, but better logging is available in Google Cloud Logs. To access logs:

Go to &gt; **View** &gt; **Executions** to check outputs from your script. Then, connect your project to the Google Cloud Platform to view the logs.

In the Google Cloud Logs Explorer, apply the filter `resource.type="app_script_function"` to view logs related to your app.

## Deploying

-   Click the “Deploy” button in the top right corner of the Apps Script editor.
-   Select “Deploy as web app.”
-   Set the project version \(you can create a new one\).
-   Define who can access the app:

    -   Execute as: This should be set to Me, so the script runs with your permissions.
    -   Who has access: Choose “Anyone” \(public\).
    ![New deployment user interface](../images/cpq-txn-mgr-google-apps-script-editor-new-deployment.png)


Once deployed, you’ll get a URL ending in `/exec` for live usage and `/dev` for testing. This is the URL that users will target to trigger the `doGet` function or send POST requests to trigger `doPost`.

In the following examples, the ellipsis \(...\) represents the unique App Script number for your script.

-   Live: `https://script.google.com/macros/s/.../exec`
-   Dev: `https://script.google.com/macros/s/.../dev`

If you want to test your changes before pushing them live, use the Dev URL to test your script with real data.

Every time you redeploy, you need to create a new version of your script. Follow these steps:

1.  In the Google Apps Script editor, click the **Deploy** button in the top right.
2.  Select **Manage deployments** from the menu.
3.  In the Deployments window, click **Edit** on the existing deployment, or create a new deployment.
4.  Click **Select Version**, and then click **New version**.

In the pop-up window, you can give your version a name or description. This is optional, but helpful for tracking changes. Click **Save** to create the new version.

To view or manage your current deployments:

1.  In the Google Apps Script editor, click the **Deploy**.
2.  Select **Manage deployments**. Here you’ll see all active versions of your script.
3.  You can edit, delete, or redeploy any version by clicking the three-dot menu next to the version.

-   Edit: Update an existing deployment to point to a new version.
-   Delete: Remove the deployment entirely \(Note: the live link will stop working if the deployment is deleted\).

If needed, you can roll back to an older version of your web app:

1.  Go to **Deploy &gt; Manage deployments**.
2.  Find the previous version you want to return to and click **Edit**.
3.  Select the earlier version from the Select Version menu.
4.  Click `Deploy` to activate the previous version.

This provides an easy way to revert any issues that may arise with newer versions.

**Parent Topic:**[Transaction Manager: Use cases](transaction-manager-use-cases.md)

