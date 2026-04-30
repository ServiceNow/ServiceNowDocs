---
title: Install Vaccine Administration Management
description: Vaccine Administration Management \(VAM\) is available on the ServiceNow Store.
locale: en-US
release: xanadu
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Vaccine Administration Management, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Install Vaccine Administration Management

Vaccine Administration Management \(VAM\) is available on the ServiceNow Store.

## Before you begin

Vaccine Administration Management requires the ServiceNow® Healthcare and Life Sciences Service Management application, the Appointment Booking plugin \(com.snc.appointment\_booking\) . The Virtual Agent plugin \(com.glide.cs.chatbot\) can optionally be installed to enable chatbot conversations in the self-service portal.

If you don't have a Healthcare and Life Sciences Service Management license, contact your ServiceNow account representative. The ServiceNow platform provides support for Column Level Encryption for the tables under the Vaccine Administration Management application. However, it is not activated as part of the initial app installation.

**Note:**

-   Installation of Vaccine Administration Management relies on Healthcare and Life Sciences Service Management Core \(com.sn\_hcls\) as a dependency plugin.
-   The customer is responsible for configuring the implementation to meet local compliance rules, regulations, and laws.
-   If your instance is already set up to use encryption contexts for column-level encryption, migration is required to use encryption modules. Contact Now Support for assistance with the migration.
-   To use Column Level Encryption Enterprise, customers must purchase the Column Level Encryption Enterprise SKU. The customer can install and activate Column Level Encryption Enterprise on a single instance \(and not on all account instances\) if the customer does not share data contained in the Column Level Encryption Enterprise encrypted fields between instances. To avoid fees for using Column Level Encryption Enterprise, existing ServiceNow customers can use Column Level Encryption that is provided at no additional cost or use a third-party encryption solution.
-   For further details on installing CLE with Encryption support for Vaccine Administration Management, see [Installing CLE with Encryption support for VAM \[KB0952557\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0952557).
-   Records under the sys\_platform\_encryption\_configuration table are added as part of VAM that encrypts fields which contain sensitive data. These records must be activated to enable encryption on the corresponding fields.

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Vaccine Administration Management`.

3.  Click **Install**.

    The Application installation dialog box opens.

4.  Click **Activate**.

    **Note:** The customer is responsible for configuring the implementation to meet local compliance rules, regulations, and laws, including to address protecting sensitive data on its production and non-production instances. This Vaccine Administration Management app is designed to utilize the CLE and KMF encryption that is enabled by installing the plugin. The customer may determine that it desires to skip this step for its instances that do not contain sensitive data \(such as an instance for testing that contains only dummy data\).

5.  Enable  Column Level Encryption Enterprise.

    1.  Go to  Now Support  and choose **Service Catalog ** from the menu.

        ![The Service Catalog is highlighted within the Now Support menu.](../image/catalog.png)

    2.  Click  **Activate Plugin**.

        ![The Activate Plugin option from the service catalog.](../image/activate-plugin.png)

    3.  In the  **What is your target instance ** field, specify your instance.

    4.  Select  **Plugin I'm looking for is not listed**.

    5.  Under  **Specify the name of the plugin**, enter  `Platform Encryption plugin (com.glide.now.platform.encryption)`.

    6.  In the  **Reason/Comments ** field, state that you need the plugin \(com.glide.now.platform.encryption\) for  Vaccine Administration Management.

        ![Comment box stating that the KMF plugin is needed for Vaccine Administration Management.](../image/vam-kmf-installation.png)

    7.  In the  **Select Maintenance Start Time ** field, select a start date and time value.

        ![Select Maintenance Start Time field where a start date and a time value can be selected.](../image/vam-install-select-maintenance-start-time.png)

    8.  Click **Submit**.

    The Key Management Framework plugin \(com.glide.kmf.global\) is now active on your new instances.

6.  If you're using the CLE and KMF plugins, generate a key so that fields can be encrypted.

    **Important:** Make sure that the admin has the sn\_kmf.cryptographic\_manager role to get access to the required tables.

    1.  Navigate to **Key Management** &gt; **Cryptographic Modules** &gt; **All**.

    2.  Click the sn\_vaccine\_sm.vm\_crypto\_module crypto module record.

    3.  In the Crypto Specifications related list, click the record that appears in the list.

    4.  Navigate to **Algorithm Definition** &gt; **Lifecycle Definition** &gt; **Key Origin** &gt; **Key Creation**.

        ![Key Creation view of crypto specification with completed fields and a Generate Key option highlighted.](../image/install-vaccine-management.png)

    5.  Click **Generate Key**.

        A key is created in the Module Keys related list on the sn\_vaccine\_sm.vm\_crypto\_module crypto module record.

        **Note:** To view the fields that are encrypted, navigate to **System Security** &gt; **Field Encryption** &gt; **Encrypted Field Configurations**.

        **Important:** Users with the admin role must have elevated roles to access the Field Encryption menu.

        You can encrypt additional data fields based on your requirements and configurations. For information about additional encryption capabilities including edge encryption, database encryption, and full disk encryption, see the [Data encryption white paper](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/resource-center/white-paper/wp-data-encryption-with-servicenow.pdf).


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)

