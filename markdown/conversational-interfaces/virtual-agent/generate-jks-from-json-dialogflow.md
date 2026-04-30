---
title: Generate a Java Keystore file from the JSON private key file
description: To use Google Dialogflow with Virtual Agent Bot Interconnect, the third step is to generate a JKS file from the JSON private key you created in the previous step.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Generate a Java Keystore file from the JSON private key file

To use Google Dialogflow with Virtual Agent Bot Interconnect, the third step is to generate a JKS file from the JSON private key you created in the previous step.

## Before you begin

Role required: admin

## Procedure

1.  In a text editor, open the JSON private key file you downloaded in the previous procedure.

2.  Copy the private key text, starting with the BEGIN PRIVATE KEY section and ending with the END PRIVATE KEY section.

    ![Select the text starting with –––--BEGIN PRIVATE KEY----- and ending with –––--END PRIVATE KEY-----](../images/ggl-dialogflow-copy-private-key.png)

3.  Remove the line return characters \(\\n\) from the key:

    1.  Paste the key text in a text editor, such as TextEdit or Notepad.

    2.  Click **Edit** &gt; **Find** &gt; **Find &amp; Replace** or **Edit** &gt; **Replace**.

    3.  In the **Find** field, type `\n`.

    4.  In the **Replace** field, press `Ctrl + Enter` or `Alt + Enter`.

    5.  Click **Replace All**.

    The key text will be formatted with line breaks.

4.  Save the formatted private key text as a `.pem` file.

    For example, `privatekey.pem`.

5.  In a web browser, open the URL that is listed in the JSON file for the**client\_x509\_cert\_url** parameter.

    For example, https://www.googleapis.com/robot/v1/metadata/x509/my-srvc-account%40my-agent-ukpy.iam.gserviceaccount.com. The certificates page opens.

6.  Copy the certificate that has the same private key ID that appears in the JSON file.

7.  Replace \\n with line breaks in the certificate, as described in step 3.

8.  Save the formatted certificate as a `.pem` file.

    For example, `certificate.pem`.

9.  Navigate to the folder that contains both the private key and certificate files.

10. Open a terminal window:

    1.  In Mac OS, right-click or ctrl-click the folder and select **New terminal at folder**.

    2.  In Windows, right-click the folder and select **Open in terminal**.

11. At the terminal's command prompt, create the JKS file as follows:

    1.  Enter the following command:

        `openssl pkcs12 -export -in [certificate file name] -inkey [private key file name] -certfile [certificate file name] -out testkeystore.p12`

        For example, if certificate.pem is the name of the certficate and privatekey.pem is the name of the private key:

        `openssl pkcs12 -export -in certificate.pem -inkey privatekey.pem -certfile certificate.pem -out testkeystore.p12`

    2.  When prompted for a password, enter the password of your choice using a minimum of six characters.

        A PKCS 12 file is created with the name `testkeystore.p12`.

    3.  Enter the following command:

        `keytool -importkeystore -srckeystore testkeystore.p12 -srcstoretype pkcs12 -destkeystore dialogflow.jks -deststoretype JKS`

        You will be prompted for a password multiple times. Use the same password you created in the previous step.


## Result

A JKS file is created.

**Parent Topic:**[Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-va-api-ggl-dialogflow.md)

**Previous topic:**[Create a service account and private key for the Google Dialogflow project](create-srvc-acct-key-dialogflow.md)

**Next topic:**[Configure connections to Google Dialogflow in your Virtual Agent Bot Interconnect instance](configure-sn-instance-google-dialogflow.md)

