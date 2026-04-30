---
title: Group contract documents by contract type in the contract request form
description: As an administrator, group the contract documents by contract type in the contract request form.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Add and configure contract request functionality, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Group contract documents by contract type in the contract request form

As an administrator, group the contract documents by contract type in the contract request form.

## Before you begin

Role required: admin

## About this task

**Note:** In Legal Counsel Center and Contract Workspace, the contract documents are grouped based on the contract type, by default.

Customize the Standard Record Page \(SRP\) to display contract documents grouped by contract type in the Contract document tab through UI Builder, a web user interface builder. For more information, see [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **Now Experience Framework** &gt; **UI Builder**.

2.  Search and select your workspace.

3.  Navigate to **Record** &gt; **SRP record**.

4.  In the Page content list, under **Body** &gt; **Resizable panes** &gt; **left** &gt; **Main Tab** &gt; **Related List**, select **list related**.

5.  Define the grouping by selecting the **Config** tab and under the **Default display** section, enter the following code in the **Group by** field:

    ```
    function evaluateProperty({api, helpers}) {
      var isContractRequestForm = api.item.value.parentTable =="sn_cm_core_contract_request";
      var isContractRevisionTab = api.item.value.table == "sn_cm_core_document_revision";
      if( isContractRequestForm && isContractRevisionTab){
        return 'document';
      }
    return '';
    }
    ```

    **Note:** If the field is not editable, select the scope applicable to your workspace in the **Select an application** drop-down list at the top of the page.

6.  Select **Apply**.


**Parent Topic:**[Add and configure contract request functionality](../concept/cncore-uptake-steps.md)

