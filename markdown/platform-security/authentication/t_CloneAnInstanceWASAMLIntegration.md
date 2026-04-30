---
title: Clone an instance with a SAML integration
description: Clone an instance with a SAML integration. Before you clone an instance that uses SAML 2.0, preserve the SAML SSO-related settings on the target instance or you might make the target instance inaccessible.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Clone an instance with a SAML integration

Clone an instance with a SAML integration. Before you clone an instance that uses SAML 2.0, preserve the SAML SSO-related settings on the target instance or you might make the target instance inaccessible.

## Before you begin

Role required: admin

## Procedure

1.  On the source instance, navigate to **System Clone** &gt; **Preserve Data** &gt; **Core Instance Properties**.

2.  Make sure that the following SAML SSO-related properties are preserved using conditions.

    -   glide.authenticate
    -   glide.security
    -   glide.entry
    -   glide.script
    -   glide.session
    -   glide.saml2
    -   com.glide.communications
    -   com.snc.integration.saml\_esig
    ![Data preserver SAML.](../image/DataPreserverSAML.png)

    **Note:** When you create the clone, include attachments so that certificates carry over to the target instance. Also, make sure the **Theme** check box is cleared so these properties are preserved regardless of whether you preserve the instance theme.

3.  On the source instance, navigate to **System Clone** &gt; **Preserve Data** to preserve the SAML certificates on sys\_certificate and SAML users on sys\_user related to SAML/SSO/Multi SSO.

    If you need them, export them into XML, then manually import them on the target.

    **Warning:** Do not try to clone the SAML/SSO/Multi SSO setup from one system to another. Most transfers of SAML/SSO or Multi SSO settings do NOT work because they must be configured on the identity provider. If you overwrite a working setup, the target instance will fail to authenticate so your target instance will become inaccessible. Also, do not change the sys\_id of your Multi SSO provider record; doing that will force your users to flush their cookies. For more information about cloning precautions, see [Checklist before cloning an instance](https://support.servicenow.com/kb_view.do?sysparm_article=KB0657100).

4.  Exclude the Multi SSO tables sso\_properties, digest\_properties and saml2\_update1\_properties.

5.  Manually create the SAML/SSO/Multi SSO records on each instance independently and set up the records on your identity provider as well.

6.  Make sure that you manually create a LOCAL admin account on sys\_user \(not in LDAP or SAML\) record on the target instance and with a sys\_id that does not exist on the source instance.

7.  Click **Update**.


