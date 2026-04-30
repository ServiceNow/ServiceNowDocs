---
title: Manage use cases for Now Assist in Contract Management
description: Manage use cases for Now Assist in Contract Management by updating the fields, deactivating them when not in use, deleting when no longer required, or copying existing use cases to create new ones.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Update use cases, Modify use cases, Edit use cases, Delete use cases, Deactivate use case, Copy use case]
breadcrumb: [Managing skills for Now Assist in Contract Management, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Manage use cases for Now Assist in Contract Management

Manage use cases for Now Assist in Contract Management by updating the fields, deactivating them when not in use, deleting when no longer required, or copying existing use cases to create new ones.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_contract\_config

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

2.  Navigate to **Employee** &gt; **CM Pro**.

3.  On the tile of your activated skill that you want to modify, select **Edit** in the options menu \(![Options menu icon.](../image/cmpro-na-three-dot-icon.png)\).

    ![Active skills in Contract management pro.](../image/cmpro-na-active-skills.png "Active skills in Now Assist in Contract Management")

4.  In the skill guided setup, select **Use cases**.

5.  Select the actions icon ![Actions icon.](../image/cmpro-na-three-dot-icon.png) on the use case that you want to update, delete, deactivate, or copy.

    -   **Edit**

        Modify the use case by adding new fields, or updating, deactivating, or deleting existing fields.

        For more information on the **Field** form, see [Field form for document extraction setup](https://www.servicenow.com/docs/access?context=document-extraction-single-field-form&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and [Question form for document Q&amp;A setup](https://www.servicenow.com/docs/access?context=document-qna-single-field-form&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

        The base system use cases, **CM Pro - Contract Metadata Extraction** for contract metadata extraction, **CM Pro - Contract Obligation Extraction** for obligation extraction, and **CM Pro - Contract Analysis** for contract analysis cannot be edited, deleted, or deactivated. To customize these use cases, make a copy of the base system use cases and update the copied versions.

        **Note:** If you create your own use case or customize a copy of an available use case, be sure to test it thoroughly to ensure accuracy. You can upload a document in the Test outputs tab to test how the contract analysis skill works with the updated use case.

    -   **Make a copy**

        Copy an existing use case to create a new use case with the same fields and field groups. You can edit, delete, or deactivate the fields and field groups in the new use case.

    -   **Deactivate**

        Deactivate a use case to temporarily make it unavailable for the skill.

        The **Reactivate** option appears when a use case is deactivated. Use this option to activate a use case.

    -   **Delete**

        Delete a use case when it is no longer required for the skill.


## Result

Now Assist applies the updated use case for contract analysis or metadata extraction.

**Parent Topic:**[Managing skills for Now Assist in Contract Management](cmpro-manage-na-skills.md)

**Related topics**  


[Manage use case mappings for Now Assist in Contract Management](../task/cmpro-manage-use-case-map.md)

[Manage clause mappings for contract analysis](../task/cmpro-manage-clause-mappings.md)

[Manage expected response mappings for contract analysis](../task/cmpro-manage-expected-response.md)

[Deactivate skills for Now Assist in Contract Management](../task/cmpro-deactivate-na-skills.md)

[Create use cases for contract metadata extraction](../task/cmpro-na-usecase-me.md)

[Create use cases for contract analysis](../task/cmpro-na-usecase-ca.md)

[Create use cases for contract obligation extraction](../task/cmpro-na-use-case-obext.md)

[Select large language models for use cases in Now Assist in Contract Management](../task/cmpro-na-manage-llm.md)

