---
title: Generate a Java Keystore \(JKS\) file and configure security on your ServiceNow instance
description: To use Google Dialogflow as your NLU provider for Virtual Agent, use the private key you downloaded to generate a JKS file and set up authentication in your ServiceNow instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 4
keywords: [Java Keystore, Google Dialogflow, NLU, JKS, Virtual Agent, private key]
breadcrumb: [Configure Google Dialogflow ES as the NLU provider for Virtual Agent, Configure Natural Language Understanding in Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Generate a Java Keystore \(JKS\) file and configure security on your ServiceNow instance

To use Google Dialogflow as your NLU provider for Virtual Agent, use the private key you downloaded to generate a JKS file and set up authentication in your ServiceNow instance.

## Before you begin

Make sure the Java Development Kit \(JDK\) is installed on the system.

Role required: admin

## About this task

**Note:** Google Dialogflow uses OAuth2.0 for authentication.

## Procedure

1.  Open a command shell window.

2.  To create a JKS file from the P12 file, do the following:

    1.  Run the following command:

        ```
        keytool -importkeystore -srckeystore /local_dir/myprivatekey.p12 -srcstoretype pkcs12 -destkeystore /local_dir/myprivatekey.jks -deststoretype JKS
        ```

        In this example, `/local_dir/myprivatekey.p12` points to the private key that you downloaded in the previous step.

    2.  When prompted, enter `notasecret` for the destination keystore password and the source keystore password.

        `notasecret` is the private key password you noted from the previous step. You will enter this password three times.

    A JKS file is created in the same directory.

3.  In your ServiceNow instance, add the JKS file to the Google Dialogflow X.509 certificate record:

    1.  Navigate to **All**, and then enter `sys_certificate.list` in the filter.

    2.  Select Google Dialogflow X.509 Certificate to open the record.

    3.  On the form, fill in the fields as follows.

        |Field|Value|
        |-----|-----|
        |Type|Select **Java Key Store**.|
        |Key store password|Enter the private key password that you specified when creating the JKS file \(`notasecret`\).|
        |Active|Select this option to activate the certificate.|

    4.  Select the attachment icon and upload the JKS file to the record.

    5.  Under Related Links, select **Validate Stores/Certificates**.

        You should see a `Valid key_store` message.

    6.  Select **Update**.

4.  In your ServiceNow instance, update the Google Dialogflow JWT \(JSON Web Token\) Keystore alias record.

    1.  Navigate to **All**, and then enter `jwt_keystore_aliases.list` in the filter.

    2.  Select Google Dialogflow JWT Keystore to open the record.

    3.  On the form, fill in the fields as follows.

        |Field|Value|
        |-----|-----|
        |Signing Keystore|Select **Google DialogFlow X.509 Certificate**.|
        |Signing Algorithm|Select **RSA 256**.|
        |Signing Key|Enter the private key password that you specified when creating the JKS file \(`notasecret`\).|
        |Key Id|Leave this field empty.|

    4.  Select **Update**.

5.  In your ServiceNow instance, update the Google Dialogflow JWT provider record.

    1.  Navigate to **All**, and then enter `jwt_provider.list` in the filter.

    2.  Select Google Dialogflow JWT Provider to open the record.

    3.  In the **Signing Configuration** field, select **Google DialogFlow JWT Keystore**.

    4.  In the Standard Claims related list, enter the email address for your Google Dialogflow agent service account as the **Claim Value** for the **iss** entry.

        ![The Google DialogFlow JWT Provider configuration form displays the Signing Configuration and the iss record. The iss claim value is the agent service account email address.](../images/ggl-df-jwt-provider-config.png)

        For more information, refer to [Create a service account and private key in Google Dialogflow ES](vad-create-srvc-acct-key-dialogflow.md).

    5.  Select **Update**.

6.  In your ServiceNow instance, update the Google Dialogflow NLU OAuth Provider record:

    1.  Navigate to **All**, and then enter `oauth_entity.list` in the filter.

    2.  Select Google Dialogflow NLU to open the record.

    3.  On the form, fill in the fields as follows.

        |Field|Value|
        |-----|-----|
        |Client ID|Enter the unique ID for your Google Dialogflow agent service account that you saved from a previous step.|
        |Client Secret|Enter the private key password that you specified when creating the JKS file \(`notasecret`\).|
        |Default Grant Type|Select **JWT Bearer**.|

    4.  Select **Update**.

7.  In your ServiceNow instance, update the **GoogleDialogFlowESNLUPrediction** system alias.

    1.  Navigate to **All**, and then enter `sys_alias.list` in the filter.

    2.  Select **GoogleDialogFlowESNLUPrediction** to open the record.

    3.  Select the **Connection Attributes** tab and find the **EnvID** record.

    4.  In the **Default value** column, update the value with the name of the Google Dialogflow environment where the agent was published.

        The default value is **prod**.

        ![The EnvID column is highlighted in the list with a default value of prod.](../images/ggl-es-nlu-prediction-credentials.png)

    5.  Select **Update**.

8.  Specify Google Dialogflow ES as your NLU provider in Virtual Agent.

    For more information, see [Configure Natural Language Understanding in Virtual Agent](configure-nlu-settings.md).


**Parent Topic:**[Configure Google Dialogflow ES as the NLU provider for Virtual Agent](../concept/configure-dialogflow-es-integration.md)

**Previous topic:**[Create a service account and private key in Google Dialogflow ES](vad-create-srvc-acct-key-dialogflow.md)

**Next topic:**[Activate the Google Dialogflow ES service and enable it in your instance](activate-ggl-df-es-service.md)

