---
title: Configure properties for Supplier Lifecycle Operations
description: Use these properties to configure settings for the Supplier Lifecycle Operations application from the Properties page.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure properties for Supplier Lifecycle Operations

Use these properties to configure settings for the Supplier Lifecycle Operations application from the Properties page.

Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Properties**.

**Note:** The Properties page displays the properties for Craft only if you have installed the Craft.co Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_craft\) plugin. Click the question mark icon \(![Question mark icon.](../image/question-mark-icon.png)\) beside each property field to see the property name corresponding to that field.

<table id="table_xkn_zwh_dtb"><thead><tr><th>

Property

</th><th>

Action

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Supplier lifecycle properties

</td></tr><tr><td>

Sys Id of the External User Registration Configuration for Onboarding a contact for a supplier.**sn\_supplier.external\_registration\_profile\_id**

</td><td>

Auto-populated with the sys ID of the user registration configuration you specified in the **Value** field of the **sn\_supplier.external\_registration\_profile\_id** system property.**Note:** Sys ID \(sys\_id\) is a 32-character GUID \(Globally Unique ID\) that uniquely identifies each record in an instance.

 For more information, see [Configure system property to send registration emails to external users](../task/sys-prop-reg-email.md).

</td></tr><tr><td>

Automatic creation of cases from email

 \[sn\_supplier.slm\_email\]

</td><td>

Automatically creates a supplier case if the incoming email address matches with the email address specified in this property.For more information, see [Enable automatic creation of supplier cases from incoming emails](../task/config-email-properties.md).

</td></tr><tr><td>

Decide whether or not to enable google maps API functionality on Supplier manager workspace. Enablement of Geo Map method and Geo Map key/client will still be required.

 \[sn\_supplier.geo\_map\_enabled\]

</td><td>

Type: Yes \| NoSelect the check box to enable this property.

</td></tr><tr><td class="sub-head" colspan="2">

Craft Integration Properties

</td></tr><tr><td>

API key for craft.**sn\_supplier\_craft.craft\_api\_query**

</td><td>

Enter the API key that you received with your enterprise account from Craft.

</td></tr><tr><td class="sub-head" colspan="2">

Geo map properties

</td></tr><tr><td>

Defines which method of authentication should be used for Google Maps API used in Geo map component.**sn\_supplier.geo\_map.google.method**

</td><td>

Select one of the following options from this list:-   client-id
-   key

</td></tr><tr><td>

Map key from Google for Geo map component, tied to the URL of the server. To obtain a new key, visit [http://www.google.com/apis/maps/signup.html](http://www.google.com/apis/maps/signup.html) for details.**sn\_supplier.geo\_map.google.key**

</td><td>

If you select **key** from the **Defines which method of authentication should be used for Google Maps** drop-down list, enter the map key.

</td></tr><tr><td>

Client ID for Google Maps API for Business used in Geo map component. To obtain your own key, visit [http://www.google.com/enterprise/earthmaps/maps.html](http://www.google.com/enterprise/earthmaps/maps.html) for details.**sn\_supplier.geo\_map.google.client**

</td><td>

If you select **client-id** from the **Defines which method of authentication should be used for Google Maps** drop-down list, enter the client ID.

</td></tr><tr><td>

Defines whether to use places API from Google for Geo map component \(Enable when same Google key has active places lib subscription\).**sn\_supplier.geo\_map.google.use\_places\_lib**

</td><td>

Type: Yes \| NoSelect the check box to enable this property.

</td></tr><tr><td class="sub-head" colspan="2">

Supplier collaboration portal properties

</td></tr><tr><td>

Allow "Activity Configurations" and "Filters" to be picked from all application scopes.**sn\_supplier\_sp.allow\_all\_apps\_configuration**

</td><td>

Type: Yes \| NoSelect the check box to enable this property.

For more information, see [Set the property to configure activity configurations](../task/set-sys-prop-activity-config.md).

</td></tr></tbody>
</table>-   **[Enable automatic creation of supplier cases from incoming emails](../task/config-email-properties.md)**  
The supplier administrator can set this property to create a supplier case automatically from an incoming email.
-   **[Email format for contacts linked with multiple suppliers](../task/email-format-for-contacts-linked-with-multiple-suppliers.md)**  
Contacts linked with multiple suppliers have to include the supplier's legal name while sending emails for automatic creation of cases.

**Parent Topic:**[Install Supplier Lifecycle Operations](../task/install-supp-mgmt.md)

