---
title: Group contract documents by contract type in a contract request
description: As an administrator, group the contract documents by contract type in a contract request.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [BU configuration, Group contract documents, Uptake steps CM Pro]
breadcrumb: [Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Group contract documents by contract type in a contract request

As an administrator, group the contract documents by contract type in a contract request.

## Before you begin

Role required: admin

## About this task

**Note:** In Legal Counsel Center and Contract Workspace, the contract documents are grouped based on the contract type, by default.

Customize the Standard Record Page \(SRP\) to display contract documents grouped by contract type in the Contract document tab through UI Builder, a web user interface builder. For more information, see [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=australia&pubname=australia-application-development&ft:locale=en-US).

![Grouping of contract documents](../image/cmpro-bu-ctypr-grouping-result.png "Contract document grouping")

## Procedure

1.  Navigate to **Now Experience Framework** &gt; **UI Builder**.

2.  Search and select your workspace.

3.  Navigate to **Record** &gt; **SRP record**.

4.  In the Page content list, under **Body** &gt; **Resizable panes** &gt; **left** &gt; **Main Tab** &gt; **Related List**, select **list related**.

    ![Select related list configuration for your workspace](../image/cmpro-bu-ctype-group-related-list.png "UI builder related list configuration")

5.  In the **Configure** pane, select **Group by** field.

    ![Select group from the Configure pane](../image/cmpro-bu-ctype-group-script.png "Configure pane")

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


## Result

The contract documents will be grouped by contract type in the Contract document tab while viewing a contract request.

**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md)

[Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md)

[Add Contract requests tab to the contract request record](cncore-add-relatedlist-conreq.md)

[Add amendment tabs to contract repository record](cncore-BU-amend-relatedlist.md)

[Add Contract documents tab to the contract repository record](cncore-add-con-doc-relatedl.md)

[Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Assign a role for configuring template mappings](cncore-tbl-access-config-role.md)

[Enable contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

[Configuring the Playbook tab on contract repository records](cmpro-config-playbook-tab.md)

