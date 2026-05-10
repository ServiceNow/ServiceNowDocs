---
title: Configure self-registration for external users
description: Configure self-registration for external users.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Install Supplier Collaboration Portal, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure self-registration for external users

Configure self-registration for external users.

## Before you begin

**Note:** You must do this task after installing the Supplier Collaboration Portal.

Role required: admin

## About this task

Ensure that you have activated the com.snc.external\_user\_self\_registration plugin. For more information, see [Activate External User Self-Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/external-user-registration-plugin.md).

## Procedure

1.  Navigate to **External User Self-Registration** &gt; **User Registration Configurations** and select **New**.

2.  On the User Registration Configuration form, fill in the fields.

    For more information about the form fields and descriptions, see [Create a user registration configuration for external users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/external-user-configuration.md).

3.  From the form context menu, select **Save**.

4.  Select the **Registration** tab, and do the following:

    1.  In the Mandatory column for the **First name** and **Last name** fields, double-click and select **true** to make these fields mandatory.
    2.  Select the green check mark icon \(![Green check mark icon.](../image/green-check-mark.png)\) to save your changes.
5.  Configure the **Verification** tab to verify the identity of the registered users.

    When the user verification flow triggers, an activation link is sent to the user's registered email address.

6.  Select the **Transformation** tab, select and open the **u\_reg\_xmap\_\[number\]** transformation map that maps the registered users from the User Acti Req \[number\] source table to the User \[sys\_user\] target table.

7.  In the **Target table** field, search and select **Vendor Contact \[vm\_vdr\_contact\].**

8.  From the form header, right-click the header bar and select **Save**.

9.  Scroll down and select the **Field Maps** tab, and then select **New**.

10. Select the **Use source script** check box.

    The Source script box is displayed.

11. In the return string, enter supplier\_registration in lowercase letters exactly as shown.

    ```
    answer = (function transformEntry(source) {
    
    	// Add your code here
    	return "supplier_registration"; // return the value to be put into the target field
    
    })(source);
    ```

12. From the **Target field** list, select **Source**.

13. Select **Submit**.

14. Select the **Onboarding** tab and in the **User onboarding flow** field, search for and select **Supplier Contact Onboarding**.

15. Select the **Advanced** tab.

16. In **Registration form field configuration** section, in the **Account signup** form, add the form fields **Supplier name** \(u\_supplier\_name\) and **Relationship contact email** \(u\_relationship\_contact\_email\).

    Then select the preview this record icon to open the record.

    **Note:**

    -   The **Supplier name** field has been added in the Xanadu December 2024 upgrade. To enable and register this field, customize the registration form by adding the new supplier field with field label: Supplier name and column name: u\_supplier\_name. For more information, see [Configure a user registration configuration for external users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/external-user-configuration.md).
    -   If you need to add a supplier contact whose email domain differs from the supplier's domain, you must also [Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md).
17. In the Variables related list, select and open the **First name**, **Last name**, **Email**, and **Supplier name** records individually.

18. In the First name variable record, select the **Mandatory** check box and select **Save**.

    Repeat this step for the Last name, Email, and Supplier name variable records.

    **Note:** The **Supplier name** field has been added in the Xanadu December 2024 upgrade. This field is available only after **M2M mapping between supplier contact and suppliers** is enabled.

19. Select **Save**.

20. For sending personalized emails to contacts who want to self-register, select the **Catalog Client Scripts** tab.

21. Select **New**.

22. In the **Name** field, enter a name.

23. From the **Type** list, select **onLoad**.

24. In the **Script** box, copy and paste the code.

    ```
    function onLoad() {
        function getParameterValue(name) {
            var url = top.location.href;
            var value = new URLSearchParams(url).get(name);
            if (value) {
                return value;
            }
            return false;
        }
    
        if (this && this.location && this.location.pathname) {
            if (getParameterValue("email")) {
                g_form.setValue("email", getParameterValue("email"));
                g_form.setReadOnly("email", true);
            }
            if (getParameterValue("supplier_name") && (getParameterValue("supplier_name") != "null")) {
                g_form.setValue("u_supplier_name", getParameterValue("supplier_name"));
                g_form.setReadOnly("u_supplier_name", true);
                g_form.setValue("supplier_name", getParameterValue("supplier_name"));
                g_form.setReadOnly("supplier_name", true);
    
            }
            if (getParameterValue("relationship_contact_email") && (getParameterValue("relationship_contact_email") != "null")) {
                g_form.setValue("u_relationship_contact_email", getParameterValue("relationship_contact_email"));
                g_form.setReadOnly("u_relationship_contact_email", true);
                g_form.setValue("relationship_contact_email", getParameterValue("relationship_contact_email"));
                g_form.setReadOnly("relationship_contact_email", true);
    
            }
        }
    
    
    }
    ```

25. Select **Save**.


## What to do next

Do the following:

-   Configure the sn\_supplier.external\_registration\_profile\_id system property to ensure that registration emails are sent to external users. For more information, see [Configure system property to send registration emails to external users](sys-prop-reg-email.md).
-   Configure the Vendor Contact table to send emails to contacts during self-registration. For more information, see [Configure the Vendor Contact table to send invitation emails during self-registration](config-vendor-contact-table.md).
-   If you do this task after installing the Supplier Collaboration Portal, map the external user registration configuration that you just created to the Supplier Collaboration Portal. For more information, see [Map the self-registration configuration to Supplier Collaboration Portal](map-ext-user-to-supp-central.md).

-   **[Configure the flow to create approval records for all supplier contact invite requests](invite-contact-approval.md)**  
Typically, an approval record is created only when a supplier contact self-registers to get access to the Supplier Collaboration Portal. However, a supplier admin can configure the Supplier Contact Onboarding flow to create approval records even when a supplier manager adds or invites a new supplier contact.
-   **[Map the self-registration configuration to Supplier Collaboration Portal](map-ext-user-to-supp-central.md)**  
Map the external user self-registration configuration to the Supplier Collaboration Portal.
-   **[Configure system property to send registration emails to external users](sys-prop-reg-email.md)**  
Configure the sn\_supplier.external\_registration\_profile\_id system property to ensure that registration emails are sent to external users for accessing the Supplier Collaboration Portal.
-   **[Configure the Vendor Contact table to send invitation emails during self-registration](config-vendor-contact-table.md)**  
Configure the Vendor Contact \[vm\_vdr\_contact\] table to send invitation emails to supplier contacts during the self-registration process.
-   **[Enable notifications about self-registration errors](enable-supp-admin-emails.md)**  
Add the sn\_slm.admin role to the groups to enable supplier admins to receive an email if a supplier contact encounters an error during self-registration.

**Parent Topic:**[Install Supplier Collaboration Portal](install-supp-central.md)

**Related topics**  


[Configure the flow to create approval records for all supplier contact invite requests](invite-contact-approval.md)

[Map the self-registration configuration to Supplier Collaboration Portal](map-ext-user-to-supp-central.md)

[Configure system property to send registration emails to external users](sys-prop-reg-email.md)

