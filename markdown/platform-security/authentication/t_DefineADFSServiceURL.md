---
title: Set up ADFS for SAML
description: Set up ADFS for SAML. This procedure uses ADFS 2.0 and shows samportal.example.com as the ADFS website. Replace this with your ADFS website address.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Set up ADFS for SAML

Set up ADFS for SAML. This procedure uses ADFS 2.0 and shows samportal.example.com as the ADFS website. Replace this with your ADFS website address.

## Before you begin

Role required: admin

## Procedure

1.  Log into the ADFS 3.0 server and open the management console.

2.  Right-click **Service** and select **Edit Federation Service Properties**.

    ![Edit Federation Service Properties.](../image/ADFSEditFSProperties01.png)

3.  Confirm that the General settings match your DNS entries and certificate names.

    ![Edit properties.](../image/ADFSEditFSProperties02.png)

4.  Browse to the certificates and export the Token-Signing certificate.

    1.  Right-click the certificate and select **View Certificate**.

    2.  Select the **Details** tab.

    3.  Click **Copy to File**.

        The Certificate Export Wizard opens.

    4.  Select **Next**.

    5.  Ensure that the **No, do not export the private key** option is selected, and then click **Next**.

    6.  Select **DER encoded binary X.509 \(.cer\)**, and then click **Next**.

    7.  Select where you want to save the file and give it a name and click **Next**.

    8.  Select **Finish**.

        The instance requires that this certificate be in PEM format. You can convert this certificate using client tools or online tools such as SSL Shopper.

5.  Use the DER/Binary certificate that you just created, and export it in Standard PEM format.


