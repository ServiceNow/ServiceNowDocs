---
title: Use guided setup for ServiceNow Vault
description: Use guided setup to begin using an application with ServiceNow Vault easily.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# Use guided setup for ServiceNow Vault

Use guided setup to begin using an application with ServiceNow Vault easily.

## Before you begin

Role required: Elevate to sn\_vault\_console.vault\_console\_admin role.

## Procedure

1.  Navigate to **All** &gt; **Vault** &gt; **Vault console**.

2.  In the **Guided vault** section, Select the **Get started** button for your application.

3.  In **Select app data** use the table to select the application data to be used with ServiceNow Vault, select **Preview classes** when finished

    |Label|Description|
    |-----|-----------|
    |Table|The table the data is located in.|
    |Column|The column the data is located in|
    |Existing Class|The current classification of the data|
    |Recommended Class|The recommended classification for the data.|
    |Application|The application scope of the data|

4.  In **Preview data classification** preview your data classification settings, when finished check agree and select the **Apply recommended classes** button.

    |Label|Description|
    |-----|-----------|
    |Table|The table the data is located in.|
    |Column|The column the data is located in|
    |Final class|The class the data will be assigned|
    |Application|The application scope of the data|

5.  In **Classification summary** review the results of the data classification, select **Next** when finished.

    Use [Data Classification](../../security/concept/data-classification.md) to review any data that failed to classify.

6.  In **Protect existing data** review the protection policies of the data.

    |Label|Description|
    |-----|-----------|
    |Table|The table the data is located in.|
    |Column|The column the data is located in|
    |Anonymization|Reports if a data anonymization policy can be, or already is applied to the data.|
    |Field encryption|Reports if a field encryption policy can be, or already is applied to the data.|
    |Zero trust access|Reports if a zero trust access policy can be, or already is applied to the data.|

7.  You can select **Available** to begin applying that columns respective application data protection policy, review [Vault tools and metrics](../concept/vault-tools.md) for more information.

8.  In **Protect real time data** review your real time data protection policies, select **Mark as complete** when finished.

    |Label|Description|
    |-----|-----------|
    |Name|The name of the ???|
    |Type|The data channel type.|
    |Real time anonymization|Reports if there is a real time anonymization policy available, or already applied to the data.|

    **Note:** Real time data will be protected across the entire instance and all applications,.


## Result

The select application now has classified data and protection policies. As well, it will now report relevant metrics to the [ServiceNow Vault console dashboard](../concept/vault-dashboard.md).

**Parent Topic:**[Configuring ServiceNow Vault](../concept/configuring-servicenow-vault.md)

