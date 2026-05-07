---
title: Use guided setup for ServiceNow Vault
description: Use guided setup to begin using an application with ServiceNow Vault easily.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# Use guided setup for ServiceNow Vault

Use guided setup to begin using an application with ServiceNow Vault easily.

## Before you begin

Role required: Elevate to sn\_vault\_console.vault\_console\_admin role.

To secure custom apps, install the Now Assist for Vault application and make sure that all Now Assist for Vault skills and workflows are enabled. See [Install Now Assist for Vault](../../now-assist-vault/task/configuring-now-assist-vault.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Vault** &gt; **Vault console**.

2.  In the Guided vault section, select **Get started** for your application within the **ServiceNow apps** tab.

    To begin the guided setup for your custom applications, go to the **Custom apps** tab. Select the **+ Add custom app** button, choose the app that you want to secure from the drop-down list, and then select **Get started**. Or you can use Ask Now Assist to secure your custom applications through conversational prompts. For example, select **Ask Now Assist**. In the Now Assist panel, start the conversation with `Find and secure my custom apps`. See [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

3.  In **Select app data**, use the table to select the application data to be used with ServiceNow Vault and select **Review selection** when finished.

    |Label|Description|
    |-----|-----------|
    |Table|The table the data is located in.|
    |Column|The column the data is located in.|
    |Existing Class|The current classification of the data.|
    |Class to add|The proposed classification for the data.|
    |Reason|The primary reason for the proposed class to add.|

    The proposed classes are based on table column names and application context.

4.  In **Preview data classification**, review your data classification settings.

    |Label|Description|
    |-----|-----------|
    |Table|The table the data is located in.|
    |Column name|The column the data is located in.|
    |Final class|The class the data will be assigned.|

    When finished, check **Agree** and select **Classify data**.

5.  In **Classification summary**, review the results of the data classification and select **Next** when finished.

    Use [Data Classification](../../security/concept/data-classification.md) to review any data that failed to classify.

6.  In **Protect existing data**, review the protection policies of the data.

    |Label|Description|
    |-----|-----------|
    |Table|The table the data is located in.|
    |Column|The column the data is located in.|
    |Anonymization|Reports if a data anonymization policy can be, or already is applied to the data.|
    |Field encryption|Reports if a field encryption policy can be, or already is applied to the data.|
    |Zero trust access|Reports if a zero trust access policy can be, or already is applied to the data.|

7.  Begin applying that column's respective application data protection policy by selecting **Available**.

    Review [Vault tools and metrics](../concept/vault-tools.md) for more information.

8.  In **Protect real-time data, review your real-time data protection policies**.

    |Label|Description|
    |-----|-----------|
    |Name|The name of the channel or column of a table.|
    |Type|Indicates whether the data is from a channel or column.|
    |Real-time anonymization|Reports if there is a real-time anonymization policy available, or already applied to the data.|

    **Note:** Real-time data is protected across the entire instance and all applications.

    Select **Done** when finished.


## Result

The selected application now has classified data and protection policies. It also reports relevant metrics to the [ServiceNow Vault console dashboard](../concept/vault-dashboard.md).

