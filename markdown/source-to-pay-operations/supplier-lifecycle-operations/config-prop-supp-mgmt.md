---
title: Configure properties for Supplier Case Management
description: Use these properties to configure settings for the Supplier Case Management application from the Properties page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/config-prop-supp-mgmt.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Install Supplier Case Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure properties for Supplier Case Management

Use these properties to configure settings for the Supplier Case Management application from the Properties page.

Navigate to **All** &gt; **Supplier Case Management** &gt; **Properties**.

**Note:** The Properties page displays the properties for Craft only if you have installed the [Craft.io integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/slo-glossary.md) \(com.snc.sn\_supplier\_craft\) plugin. Select the question mark icon \(\[Omitted image "question-mark-icon.png"\] Alt text: Question mark icon.\) beside each property field to see the property name corresponding to that field.

<table id="table_xkn_zwh_dtb"><thead><tr><th>

Property

</th><th>

Action

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Supplier Case Management properties

</td></tr><tr><td>

Sys Id of the External User Registration Configuration for Onboarding a contact for a supplier.**sn\_supplier.external\_registration\_profile\_id**

</td><td>

Auto-populated with the sys ID of the user registration configuration you specified in the **Value** field of the **sn\_supplier.external\_registration\_profile\_id** system property.**Note:** Sys ID \(sys\_id\) is a 32-character GUID \(Globally Unique ID\) that uniquely identifies each record in an instance.

 For more information, see [Configure system property to send registration emails to external users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/sys-prop-reg-email.md).

</td></tr><tr><td>

Automatic creation of cases from email

 **sn\_supplier.slm\_email**

</td><td>

Automatically creates a supplier case if the incoming email address matches with the email address specified in this property.For more information, see [Enable automatic creation of supplier cases from incoming emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-email-properties.md).

</td></tr><tr><td>

Enable acceptance flow for supplier cases.**sn.slm.isAcceptedFlowEnabled**

</td><td>

If enabled, supplier cases can be closed only if the supplier contact accepts the case resolution. While waiting for the supplier contact's response, the case state changes to **Awaiting acceptance** and an email with the resolution details is sent to the supplier contact.

 If not enabled, supplier cases can be closed without requiring acceptance from the supplier contact.

 For more information, see [Complete a supplier case from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/complete-supplier-case.md).

</td></tr><tr><td class="sub-head" colspan="2">

Craft Integration Properties

</td></tr><tr><td>

API key for craft.**sn\_supplier\_craft.craft\_api\_query**

</td><td>

Enter the API key that you received with your enterprise account from Craft.

</td></tr><tr><td class="sub-head" colspan="2">

Supplier collaboration portal properties

</td></tr><tr><td>

Allow "Activity Configurations" and "Filters" to be picked from all application scopes.**sn\_supplier\_sp.allow\_all\_apps\_configuration**

</td><td>

Type: Yes \| NoSelect the check box to enable this property.

For more information, see [Set the property to configure activity configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/set-sys-prop-activity-config.md).

</td></tr></tbody>
</table>-   **[Enable automatic creation of supplier cases from incoming emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/config-email-properties.md)**  
The supplier administrator can set this property to create a supplier case automatically from an incoming email.
-   **[Email format for contacts linked with multiple suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/email-format-for-contacts-linked-with-multiple-suppliers.md)**  
Contacts linked with multiple suppliers have to include the supplier's legal name while sending emails for automatic creation of cases.

**Parent Topic:**[Install Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-supp-mgmt.md)

**Related topics**  


[Components installed with Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/installed-with-supp-mgmt.md)

[Explicit Roles in Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/slo-explicit-roles-plugin.md)

[Application plugin installation sequence in Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/slm-plugin-list.md)

