---
title: Configure the ADFS relying party claim rules
description: Edit the claim rules to enable proper communication with the instance.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Configure the ADFS relying party claim rules

Edit the claim rules to enable proper communication with the instance.

## Before you begin

Role required: admin

## Procedure

1.  Log into the ADFS server and open the management console.

2.  Right-click the relying party trust and select **Edit Claim Rules**.

3.  Click the **Issuance Transform Rules** tab.

4.  Select **Add Rules**.

5.  Select **Send LDAP Attribute as Claims** as the claim rule template to use.

6.  Give the claim a name such as `Get LDAP Attributes`.

7.  Set the **Attribute store** to `Active Directory`, the **LDAP Attribute** to `E-Mail-Addresses`, and the **Outgoing Claim Type** to `E-mail Address`.

    ![Get attribute.](../image/Adfs-editReplyingPartyClaimRules-01.png)

    ```
    c:[Type == "http://schemas.microsoft.com/ws/2008/06/identity/claims/windowsaccountname", Issuer == "AD AUTHORITY"]  
    => issue(store = "Active Directory", 
    types = ("http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress"), 
    query = ";mail;{0}", param = c.Value);
    
    ```

8.  Select **Finish**.

9.  Select **Add Rules**.

10. Select **Transform an Incoming Claim** as the claim rule template to use.

11. Give the Claim a name such as `Email to Name ID`.

12. Set the **Incoming claim type** to the **Outgoing Claim Type** in the previous rule.

    For example, `E-Mail Address`.

13. Set the **Outgoing claim type** to `Name ID` and the **Outgoing name ID format** to `Email`.

    **Note:** These values must match the [Name ID policy](t_SetUpNameIDPolicy.md) you define during SAML 2.0 configuration.

14. Select **Pass through all claim values**.

    ![Email to Name ID.](../image/Adfs-editReplyingPartyClaimRules-02.png)

    This claim rule should look similar to the following rule language.

    ```
    c:[Type == "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress"]
     => issue(Type = "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier", 
    Issuer = c.Issuer, OriginalIssuer = c.OriginalIssuer, Value = c.Value, ValueType = c.ValueType, 
    Properties["http://schemas.xmlsoap.org/ws/2005/05/identity/claimproperties/format"] 
    = "urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress");
    
    ```

15. Click **Finish**.


