---
title: Add signatories in self-served contract request
description: Add signatories in self-served contract requests when the contract is generated from a template configured with signature blocks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-update-sign-ss-cmr.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
breadcrumb: [Use self-served contract request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add signatories in self-served contract request

Add signatories in self-served contract requests when the contract is generated from a template configured with signature blocks.

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller or sn\_cm\_core.contract\_user

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request that is assigned to you or for which you're a collaborator.

3.  In the **Signatories** tab, select **Add**.

4.  On the Add Signatory form, indicate whether you are configuring an internal or external signatory by selecting **Internal** or **External**.

    \[Omitted image "cmpro-add-sign.png"\] Alt text: Add signatories in contract request.

5.  Configure the signatories.

<table id="choicetable_hm4_3vk_byb"><thead><tr><th align="left" id="d455507e112">

Option

</th><th align="left" id="d455507e115">

Steps

</th></tr></thead><tbody><tr><td id="d455507e121">

**Internal**

</td><td>

1.  In the **Internal Signer** field, enter the name of the signer.

The fields **Authorized signatory name**, **Signatory**, and **Signatory email** are automatically populated.

2.  In the **Order** field, enter the order in which the contract should be sent to the signer. The order value should be unique.
3.  In the **Signatory Role** field, select the role for the signatory.

**Note:** The field is enabled only for Docusign electronic signature. For wet signature and offline signature, the field is inactive and the default value is set to **Signer**.

The **Signatory Role** field is visible only when the **sn\_cm\_core.enable\_docusign\_signature\_roles** system property is set to `true`.

To enable this property, see [Enable signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-enable-signatory-roles.md). For more information about signatory roles, see [Signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-signatory-roles.md).

4.  Select **Add**.


</td></tr><tr><td id="d455507e215">

**External**

</td><td>

1.  In the **Authorized signatory name** field, enter the external signer's name.
2.  In the **Signatory** field, enter the external signer's title.
3.  In the **Signatory email** field, enter the external signer's email address.
4.  In the **Order** field, enter the order in which the contract should be sent to signers for an e-signature. The order value should be unique.
5.  In the **Signatory Role** field, select the role for the signatory.

**Note:** The field is enabled only for Docusign electronic signature. For wet signature and offline signature, the field is inactive and the default value is set to **Signer**.

The **Signatory Role** field is visible only when the **sn\_cm\_core.enable\_docusign\_signature\_roles** system property is set to `true`.

To enable this property, see [Enable signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-enable-signatory-roles.md). For more information about signatory roles, see [Signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-signatory-roles.md).

6.  Select **Add**.


</td></tr></tbody>
</table>
**Parent Topic:**[Use self-served contract request]()

