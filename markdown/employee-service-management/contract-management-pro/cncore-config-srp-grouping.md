---
title: Group contract documents by contract type in the contract request form
description: As an administrator, group the contract documents by contract type in the contract request form.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Group contract documents by contract type in the contract request form

As an administrator, group the contract documents by contract type in the contract request form.

## Before you begin

Role required: admin

## About this task

**Note:** In Legal Counsel Center and Contract Workspace, the contract documents are grouped based on the contract type, by default.

Customize the Standard Record Page \(SRP\) to display contract documents grouped by contract type in the Contract document tab through UI Builder, a web user interface builder. For more information, see [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Procedure

1.  Navigate to **Now Experience Framework** &gt; **UI Builder**.

2.  Search and select your workspace.

3.  Navigate to **Record** &gt; **SRP record**.

4.  In the Page content list, under **Body** &gt; **Resizable panes** &gt; **left** &gt; **Main Tab** &gt; **Related List**, select **list related**.

5.  In the **Configure** tab of the right pane, select **Group by** field.

6.  Enter the following code in the **Group by** field:

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

7.  Select **Apply**.


**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md)

[Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md)

[Add Contract requests tab to your workspace](cncore-add-relatedlist-conreq.md)

[Add amendment tabs to contract repository record](cncore-BU-amend-relatedlist.md)

[Display contract documents in a contract repository record](cncore-add-con-doc-relatedl.md)

[Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Provide permissions to configure default contract document information](cncore-tbl-access-config-role.md)

[Provide access to contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

