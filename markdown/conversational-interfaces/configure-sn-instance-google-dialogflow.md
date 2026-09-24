---
title: Configure connections to Google Dialogflow in your Virtual Agent Bot Interconnect instance
description: To use Google Dialogflow with Virtual Agent Bot Interconnect, the fourth step is to configure the connection in your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/configure-sn-instance-google-dialogflow.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using Google Dialogflow as a secondary bot, Virtual Agent Bot Interconnect, Conversational Interfaces]
---

# Configure connections to Google Dialogflow in your Virtual Agent Bot Interconnect instance

To use Google Dialogflow with Virtual Agent Bot Interconnect, the fourth step is to configure the connection in your ServiceNow® instance.

## Before you begin

[Generate a Java Keystore file from the JSON private key file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/generate-jks-from-json-dialogflow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  On the Connection &amp; Credential Aliases page, click the **Bot Interconnect Dialogflow Integration** record.

3.  Under Related Links, click **Create New Connection &amp; Credential**.

4.  Use the JSON file you downloaded in a [previous step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/create-srvc-acct-key-dialogflow.md) to fill in the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|A name for your credential. For example, `Dialogflow Connection`.|
    |Project ID \(project\_id\)|The value that corresponds with the **project\_id** parameter in the JSON file. For example, **my-agent-ukpy**.|
    |Service Account Email \(client\_email\)|The value that corresponds with the **client\_email** parameter in the JSON file. For example, **my-srvc-account@my-agent-ukpy.iam.gserviceaccount.com**.|
    |Private Key ID \(private\_key\_id\)|The value that corresponds with the **private\_key\_id** parameter in the JSON file. For example, **8347eb542980d21e0c22a3bd6cc577ce0ac3a1a1**.|
    |Keystore Password|The password that you used when you created the Java Keystore \(JKS\) file in a [previous step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/generate-jks-from-json-dialogflow.md).|
    |Keystore|Select the JKS file you created in a previous step.|

5.  Click **Create and Get OAuth Token**.


