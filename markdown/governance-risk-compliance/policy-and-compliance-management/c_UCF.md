---
title: Integrate with UCF Common Controls Hub to manage compliance frameworks
description: Compliance administrators can download content from Network Frontiers Unified Compliance Framework \(UCF\) to use as GRC authority documents, citations, controls, and control objectives. The documents can be updated on pre-defined intervals. You must have a UCF Common Controls Hub account to create shared lists and import them into the ServiceNow instance.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure UCF integration using UCF CCH, Manage UCF integration, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Integrate with UCF Common Controls Hub to manage compliance frameworks

Compliance administrators can download content from Network Frontiers Unified Compliance Framework \(UCF\) to use as GRC authority documents, citations, controls, and control objectives. The documents can be updated on pre-defined intervals. You must have a UCF Common Controls Hub account to create shared lists and import them into the ServiceNow® instance.

If your organization wants to use UCF Common Controls Hub as the source for your controls library, you can purchase a subscription from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) or see [Common Controls Hub](https://commoncontrolshub.com/pricing/). For more information, see [Unified Compliance Framework](https://www.unifiedcompliance.com/company/).

**Note:** The previous arrangement for free access to UCF content inclusive of your GRC license ended November 30, 2018. All customers must purchase a subscription from Unified Compliance directly.

**Warning:** All data imported from UCF Authority Documents is read-only and must be protected. Do not customize the authority documents, citations, or control objectives on any UCF fields transformed into GRC tables.

1.  Sign up for a [UCF CCH](https://commoncontrolshub.com/pricing/) account and customize your basic subscription to include API Access.
2.  [Activate Compliance UCF](../../grc-common/task/activate-grc-comp-ucf.md).
3.  [Create a Now Support Case for UCF-CCH account integration information](../task/create-hi-request-ucf-integration.md).
4.  [Configure the UCF integration using the UCF Common Controls Hub](../task/configure-UCF-integration.md).
5.  [Download a UCF shared list](../task/download-a-shared-list.md).

## Import authority document using single shared list

Every authority document already imported into the ServiceNow® instance must be in any shared list you wish to import from the UCF CCH. This prevents inconsistencies between what is in the UCF CCH \(which may have changed\) and what you’ve already imported.

![Graphic shows all authority documents reimported with the new one](../image/cch-shared-okay.png "Shared list import successful")

![Graphic shows a mismatch of the imported authority documents](../image/cch-shared-not-okay.png "Shared list import unsuccessful")

An error is rendered since SOX is not being reimported within this Shared List.

## Import authority documents using multiple shared lists

If you need to import more than 100 authority documents then you must import them into multiple shared lists, as there is a limitation that a shared list can contain only 100 authority documents. You can create multiple shared list \(SL\), for example SL1 to import 100 authority documents and SL2 for the rest of the authority documents. Group similar authority documents as one group when you import the authority documents into multiple shared list, so that there is no dependency of the documents between the multiple shared list.

To support multiple shared list, the system property **sn\_comp\_ucf.deactivate\_deprecated\_docs** that is by default **true**, must be set to **false**.

-   If the system property is set to true, then the existing validation is done to check if the authority documents imported are already imported in the ServiceNow instance.
-   If the system property is set to false, then the imported authority documents are not validated at all.

Set the property as false and import the UCF content in multiple shared list. If the authority documents, citations, and control objectives that are imported in the shared list are deprecated, then such documents will not be deactivated in the ServiceNow instance. Instead, the user must manually validate the documents and the links between the citation and control objectives. An email is sent with the links to the mapping between the citation and control objectives.

## UCF and GRC terminology differences

Authority documents in the UCF content are organized and mapped to their proper citations, which in turn are mapped to a common set of controls. The terminology between UCF and the GRC applications differs slightly as explained in the following table.

|UCF|GRC application|
|---|---------------|
|Authority Document|Authority Document|
|Citation|Citation|
|Control|Control Objective|

-   **[Create a Now Support Case for UCF-CCH account integration information](../task/create-hi-request-ucf-integration.md)**  
After establishing your UCF CCH account, use the Now Support Service Portal to initiate the account integration process.
-   **[Download a UCF shared list](../task/download-a-shared-list.md)**  
In order for compliance managers to download UCF authority documents from the UCF CCH, the list must be marked as Shared. When updating Authority Documents or adding new ones, you must update all your authority documents to ensure that the common controls framework remains in sync with the authority documents you are using.

**Parent Topic:**[Configure the UCF integration using the UCF Common Controls Hub](../task/configure-UCF-integration.md)

