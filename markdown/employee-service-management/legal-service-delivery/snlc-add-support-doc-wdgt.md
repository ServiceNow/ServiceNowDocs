---
title: Add supporting document widget in own-paper record producer
description: Add the supporting document widget to a record producer to enable uploading of supporting documents.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Add supporting document widget in own-paper record producer

Add the supporting document widget to a record producer to enable uploading of supporting documents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Legal Catalog** &gt; **Record Producers**.

2.  Select the own-paper record producer \(Example: Non-disclosure Agreement\) for which you want to add the supporting document widget.

3.  Configure the variable set.

    1.  Navigate to **Variable Set** related list.

        ![Navigate to Variable set related list](../image/snlc-add-suppdoc-wdg-variableset.png)

    2.  Select **Edit**.

    3.  Add the widget by moving **Upload Contract Documents** and **Upload documents optional interaction** from the Collection to the Variable set list.

        ![Adding supporting document widget variable list](../image/snlc-add-variableset-suppdocs.png "Add supporting docs variable set")

    4.  Select **Save**.

4.  Configure variables for **Upload documents optional interaction** variable set.![Configure variables](../image/snlc-add-suppdoc-wdg-variableset.png)

    1.  Select **Upload documents optional interaction** from the variable set related list.

    2.  Select **Variables** related list.

    3.  Set the value for **internal\_type\_of\_paper** to own\_paper and for **internal\_contract\_type** give sys\_id of the contract type associated with the record.

        To get sys\_id, go to contract type record, select and hold \(or right-click\) on the header and select **Copy sys\_id** Example: If you’re adding the widget to the Non-disclosure agreement record producer, add the sys\_id of the Non-disclosure agreement contract type.

    The supporting document widget is available in the own-paper record producers.![Suporting document widget added to the record producer](../image/snlc-suppdoc-added.png)

5.  Customize the standard ticket page to display the supporting document related list.

    1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration**.

    2.  Select the record with table sn\_lg\_ops\_request.

    3.  Navigate to **Tab configurations** related list.

    4.  Select **Supporting Documents**.

    5.  In the script, find the following code block.

        ```
        answer = gs.nil(contractExecutionGr) ? false : contractExecutionGr.request_type == sn_cm_core.CMConstants.CONTRACT_REQUEST_TYPE.AMENDMENT_REQUEST || contractExecutionGr.contract_configuration.document_type == sn_cm_core.CMConstants.DOCUMENT_TYPE.THIRD_PARTY_CONTRACT;
        ```

    6.  Replace it with the following code block.

        ```
        answer = gs.nil(contractExecutionGr) ? false : true
        ```

    7.  Save the tab configuration.

6.  Enable the supporting document widget in edit request mode.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

    2.  Search for **Contract-generation variable change** and open the record.

    3.  Navigate to **Advanced** related list.

    4.  In the script, find the following code block.

        ```
                msg = gs.getMessage("The legal request has been updated, and a new contract document revision will be generated based on the modified values.");
                          gs.addInfoMessage(msg);
                          var externalSigners = JSON.parse(current?.variables?.external_signatory_details + '' || '[]');
                          initiatePayload = {
                              ...initiatePayload,
                              externalSigners: externalSigners
                          };
        ```

    5.  Add the following code block after the located code block.

        ```
         contractCoreUtils.createOrUpdateDocumentsFromWidget({
                              ...commonArgs,
                              contractDocuments: current.variables.contract_documents + '',
                          });
        ```

    6.  Save the business rule.

    A supporting document widget is available while editing an own-paper based request.


**Parent Topic:**[Configure Contract Management Pro for Legal Service Delivery](../concept/snlc-config-sn-legal-contracts.md)

