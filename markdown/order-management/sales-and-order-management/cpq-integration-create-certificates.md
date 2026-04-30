---
title: Set up ServiceNow instance for CPQ Integration
description: Set up the ServiceNow instance and generate the JSON Web Token \(JWT\) and authenticate API calls to Logik.ai.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 3
breadcrumb: [CPQ Configurator, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up ServiceNow instance for CPQ Integration

Set up the ServiceNow instance and generate the JSON Web Token \(JWT\) and authenticate API calls to Logik.ai.

## Before you begin

Role required: admin

## Procedure

1.  Validate that the CPQ Integration application is installed on your ServiceNow instance by doing the following

    1.  Navigate to: https://&lt;service\_instance\_url&gt;/oauth\_entity.do?sys\_id=3b119df83b566210a0c0989e53e45a15

    2.  Check that the Logik.AI Admin UI Application Registry exists with a ClientID and secret.

        This information is used later.

2.  In a directory on your local machine, create the private and public certificates using OpenSSL, then use the keytool to convert the certificate from PKCS to JKS format.

    1.  Create the private key by entering: `openssl genrsa -out private.key 2048`

        The key is created in a file named private.key.

    2.  Create a self-signed certificate that uses the private key by entering: `openssl req -new -x509 -key private.key -out publickey.cer -days 3650`

        You’re prompted to enter information that is included in your certificate request. The certificate, named publickey.cer, contains the public key derived from the private key and metadata, such as subject and issuer. The certificate is digitally signed using the private key.

    3.  Create a PKCS\#12 keystore file \(a .p12 file\) by entering: `openssl pkcs12 -export -in publickey.cer -inkey private.key -out keystore.p12 -name "<cert_name>"`

        This keystore file bundles the signed certificate and private key together and sets the alias for the key+cert entry in the keystore. The file is encrypted using a password \(also called the export password\). This password is required to import and export the certificate.

    4.  Convert the .p12 \(PKCS\#12\) keystore file to .jks \(Java KeyStore\) format by entering: `keytool -importkeystore -srckeystore keystore.p12 -srcstoretype pkcs12 -destkeystore keystore.jks`

        -   You’re prompted for the export password from step 2c to read the private key and certificate from the .p12 file.
        -   You’re prompted to enter a new key store password to protect the JKS keystore file. Record and retain this password for later, since it’s required to set up the ServiceNow instance.
3.  In the ServiceNow instance, login in as admin and do the following:

    1.  Set CPQ Integration as the current scope by using the scope selection menu icon ![](../../../reuse/icons/product-icons/globe-outline-24.svg) in the Unified Navigation menu.

    2.  In the navigation filter, enter **sys\_properties.list** and open the **glide.security.file.mime\_type.validation** system property.

        Set the **Value** to false, then select **Submit**.

    3.  Navigate to https://&lt;service\_instance\_url&gt;/sys\_certificate.do?sys\_id=90b3439e2beeea1001bff246f291bf4b and do the following:

        -   Attach the keystore.jks file created in Step 2d to the Certificate record. Enter the key store password from step 2d in the Key store password field.
        -   Select **Active**.
        -   Save the certificate.
        -   \(Optional\). Validate the certificate using the Related Link for the K509 Certificate.
    4.  Navigate to https://&lt;service\_instance\_url&gt;/jwt\_keystore\_aliases.do?sys\_id=3ab40bde2beeea1001bff246f291bfc8.

        Enter the Key Store Password from Step 2d as the Signing Key and save the record.

    5.  In the navigation filter, enter **sys\_properties.list** and open the **glide.security.file.mime\_type.validation** system property.

        Set the **Value** to true, then select **Submit**.

4.  Set up API authentication by creating the integration user roles included with the Sales Customer Relationship Management applications:

    1.  Create an integration user.

        -   Navigate to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Users.**
        -   Create a new user by selecting **New**.
        -   Enter the UserID, First name, and Last name.
        -   Select **Submit**
        -   Open the user record, and in the Role tab, select **Edit**.
        -   Add the following roles:
            -   snc\_internal
            -   sn\_sales\_common.sales\_agent
            -   sn\_csm\_pricing.pricing\_integrator
            -   sn\_prd\_pm\_adv.catalog\_integrator
            -   sn\_quote\_mgmt\_core.quote\_integrator
            -   sn\_ind\_tmt\_orm.order\_integrator
            -   sn\_opty\_mgmt\_core.opportunity\_integrator
            -   sn\_sales\_cart.cart\_integrator
    2.  Navigate to: https://&lt;service\_instance\_url&gt;/oauth\_entity\_list.do?sysparm\_query=sys\_id=99a63a9e2baeea1001bff246f291bf57

5.  Personalize the list view to add the **OAuth Application User** column.

    Use the **Update Personalized List** icon.

    1.  From the list view, double click the **OAuth Application User** field to edit it.

    2.  Set the user created in Step 4a as the one the Logik.ai API record.

        If you can't modify this field, verify that you're in the correct scope \(CPQ Integration\).

    3.  Open this Logik.ai API record.

    4.  Select **Active** and save the record.

    5.  Switch to the global scope.

    6.  Create a new system property.

        -   In the navigation filter, enter `sys_properties.list`.
        -   Select **New**.
        -   Enter the property name `glide.oauth.inbound.client.credential.grant_type.enabled`.
        -   Select the edit icons for Read Roles and Write Roles and select admin for each.
        -   Set the **Value** to true.
        -   Select **Update**.

