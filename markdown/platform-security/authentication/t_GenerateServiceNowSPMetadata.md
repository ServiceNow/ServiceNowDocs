---
title: Generate instance service provider \(SP\) metadata for SAML
description: As part of your SSO configuration, you can generate the instance SP metadata to provide to the IdP.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an external identity provider, Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Generate instance service provider \(SP\) metadata for SAML

As part of your SSO configuration, you can generate the instance SP metadata to provide to the IdP.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

The IdP needs the instance SP metadata to authenticate and forward requests.

## Procedure

1.  Choose your installed SSO plugin:

<table id="choicetable_eqz_pd4_pdb"><tbody><tr><td id="d50405e74">

**Multi-Provider SSO**

</td><td>

Navigate to **Multi-Provider SSO** &gt; **Identity Providers**. Choose an IdP and click the **Generate Metadata** button. The integration automatically generates the instance's SP metadata from the system property settings.

</td></tr><tr><td id="d50405e95">

**SAML 2 SSO**

</td><td>

Navigate to **SAML 2 Single Sign-on** &gt; **Metadata**. The integration automatically generates the instance's SP metadata from the system property settings.

</td></tr></tbody>
</table>2.  Copy the SP metadata in the text box.

    For example:

    ```
    <EntityDescriptor xmlns="urn:oasis:names:tc:SAML:2.0:metadata" entityID="https://yourinstance.service-now.com">
     	<SPSSODescriptor AuthnRequestsSigned="false" WantAssertionsSigned="true" protocolSupportEnumeration="urn:oasis:names:tc:SAML:2.0:protocol">
    		<SingleLogoutService Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect" Location="https://yourinstance.service-now.com/navpage.do" />
    		<NameIDFormat>urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress</NameIDFormat>
    		<AssertionConsumerService isDefault="true" index="0" Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST" Location="https://yourinstance.service-now.com/navpage.do" />
    		<AssertionConsumerService index="1" Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST" Location="https://yourinstance.service-now.com/consumer.do"/>
    	</SPSSODescriptor>
    </EntityDescriptor>
    ```

3.  Provide the instance SP metadata to the IdP.

    For example, SSOCircle allows a user to provide the SP metadata online.


