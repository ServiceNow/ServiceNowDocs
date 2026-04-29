---
title: Add external signatories widget in third-party paper record producer
description: Add the external signatories widget to a record producer enabling you to add external signers.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [external signatories widget, external signatories widget for TPC]
breadcrumb: [Configure, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add external signatories widget in third-party paper record producer

Add the external signatories widget to a record producer enabling you to add external signers.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Legal Catalog** &gt; **Record Producers**.

2.  Select the third-party paper record producer \(Example: Third-party Contract Review\) for which you want to add the supporting document widget.

3.  Configure the variable set.

    1.  Navigate to **Variable Set** related list.

        ![Variable set for record producer](../image/snlc-add-ext-signer-variableset.png)

    2.  Select **Edit**.

    3.  Add the widget by moving **External signatory details** from the Collection to the Variable set list.

        ![Add external signer widget](../image/snlc-add-variableset-extsigner.png "Add supporting docs variable set")

    4.  Select **Save**.

        ![External signer widget added](../image/snlc-extsigners-added.png)

4.  Enable the external signatories widget in edit request mode.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

    2.  Search for **Contract-generation variable change** and open the record.

    3.  Navigate to **Advanced** related list.

    4.  In the script, find the following code block.

        ```
                   if (documentType == 'third_party_contract') {
                          var contractRequestResponse = contractExecutionUtils.createOrEditContractRequest(current, documentType, contractType, signatureType, null, 'edit');
                          if (contractRequestResponse.success == false) {
                              current.comments = response.message;
                              current.update();
                              return;
                          }
                          contractCoreUtils.createOrUpdateDocumentsFromWidget({
                              ...commonArgs,
                              contractDocuments: current.variables.contract_documents + '',
        					  
                          });
        ```

    5.  Add the following code block after the located code block.

        ```
         var externalSigners = JSON.parse(current?.variables?.external_signatory_details + '' || '[]');
        contractExecutionUtils.processSigners(current, externalSigners, contractRequestResponse, documentType);
        ```

    6.  Save the business rule.

    External signatories document widget is available while you are editing third-party paper based request.


**Parent Topic:**[Configure Contract Management Pro for Legal Service Delivery](../concept/snlc-config-sn-legal-contracts.md)

