---
title: Configure script access to encrypted data
description: Execute a script to run the cryptographic module policy for a cryptographic purpose. Specific read \(decrypt/unwrap\) or write \(encrypt, wrap\) access can be defined based on the module access policy operation granularity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/configure-script-encryption.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Script access for cryptographic modules, Encrypting fields and attachments, Using Field Encryption, Field Encryption, Encryption]
---

# Configure script access to encrypted data

Execute a script to run the cryptographic module policy for a cryptographic purpose. Specific read \(decrypt/unwrap\) or write \(encrypt, wrap\) access can be defined based on the module access policy operation granularity.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## About this task

Examples of uses are for Business Rules and Script Includes. This procedure uses a script for Business Rules.

## Procedure

1.  Create a cryptographic module with the symmetric data encryption/decryption algorithm.

    Refer to [Create a cryptographic module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/create-cryptographic-module.md) for details. Specific access to the data or attachment is controlled with a module access policy with the following characteristics:

    -   Symmetric encryption: The script is able to encrypt data but unable to decrypt the data.
    -   Symmetric decryption: The script is able to decrypt uploaded encrypted data or attachment but unable to encrypt data or attachments.
    -   Symmetric encryption and decryption: The script is able to both encrypt and decrypt data or attachments.
2.  Navigate to **System Definition** &gt; **Business Rules**.

3.  Click **New**.

    \[Omitted image "business-rule-script.png"\] Alt text: New Business Rule record.

4.  Complete the form on the **When to run** tab and enter the script on the **Advanced** tab:

<table id="table_hvx_5lw_d4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the business rule.

</td></tr><tr><td>

Table

</td><td>

Select **Incident \[incident\]**from the drop-down list.

</td></tr><tr><td>

Application

</td><td>

**Global** is selected by default.

</td></tr><tr><td>

Active

</td><td>

Mark the rule as **Active**.

</td></tr><tr><td>

Advanced

</td><td>

Select the check box to display advanced options.

</td></tr><tr><td>

When to run tab

</td><td>

On the **When to run** tab, enable **Insert** and **Update** fields.

</td></tr><tr><td>

Advanced tab

</td><td>

On the **Advanced** tab, paste the following script text at line 3: ```

var gc = global.GlideCryptoModule.getModule('global.acme_mod');
var value = 'test';
var encrypted = gc.encryptData(value);
gs.info('value: ' + value);
gs.info('Encrypted: ' + encrypted);
var decrypted = gc.decryptData(encrypted);
gs.info('Decrypted: ' + decrypted);
gs.info(decrypted == value);

```

 **Note:** Refer to the "Business Rules Advanced Tab" image for details.

</td></tr></tbody>
</table>    \[Omitted image "business-rules-advanced.png"\] Alt text: Business Rule Advanced tab.

5.  Select **Submit**.

6.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience** &gt; **Configurations** &gt; **Access Policies** &gt; **** **All**.

    **Note:** For additional information, refer to [Create a module access policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/create-module-access-policy.md).

7.  Select **Create new**.

8.  Select an existing Field Encryption module to associate the Module Access Policy \(MAP\) with.

9.  Select **Create**.

10. Complete the form.

    \[Omitted image "fe-create-map.png"\] Alt text: Target script selection.

    Module Access Policies fields

    |Field|Description|
    |-----|-----------|
    |Policy name|Enter a name for the policy.|
    |Type|Select **Script** to control access by script.|
    |Script Table|Select a value from the script table drop-down list. For this example, select **Business Rule \[sys\_script\]**.|
    |Result|To give the script access to the module, select **Track** in the **Result** field.|
    |Crypto module|Displays the module with the symmetric data encryption/decryption algorithm that you selected.|
    |Active|Select to activate the policy.|
    |Target Script|Select the script document for the policy. Select the **Table name** and then the related document for the policy. For this example, select the Business Rule that you created in previous steps.|
    |Check script version|Select this option to direct the system to perform a version comparison anytime the script is run. If the script has been changed, the user is notified.|
    |Specify purpose|Optional. Enable  to  display  the  Crypto  Spec field  on  the  form.  Enable this option to configure granular operations, such as some users being able to encrypt, but not decrypt.|
    |Application|The  Application scope  is  auto-populated  by  your  current scope. |

11. Select **Save**.

    The Module Access Policy for the script is now available in the system.


-   **[View declined cryptographic module usage requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/view-declined-crypto-module-usage-requests.md)**  
View cryptographic modules that rejected encryption requests made by scripts because of unsupported encryption mechanisms.

**Parent Topic:**[Script access for cryptographic modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/script-map.md)

