---
title: Use Multi-Provider SSO to set up an SSO approval for a SAML 2.0 authentication
description: An SSO approval with e-signature requires configuration on the SAML IdP and the ServiceNow instance.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [E-signature for Multi-Provider SSO, Multi-Provider SSO configurations, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Use Multi-Provider SSO to set up an SSO approval for a SAML 2.0 authentication

An SSO approval with e-signature requires configuration on the SAML IdP and the ServiceNow instance.

## Before you begin

Role required: admin

## About this task

The SAML IdP must support and honor the forceAuthn attribute in SAML assertion requests. E-signature doesn’t function without this IdP setting. Set up an approval with e-signature using credentials from a SAML 2.0 authentication.

## Procedure

1.  Activate or upgrade to SAML 2.0 with the [Activate Multi-Provider SSO plugin](t_ActivateMultipleProviderSSO.md).

2.  Activate the [Approval with E-Signature plugin](activate-approval-esignature.md).

3.  Navigate to **Multi-Provider SSO** &gt; **Identity Providers** and verify your 2.0 SAML IdP configuration Advanced tab shows the **Force AuthnRequest** attribute checked.

    Your SAML 2.0 IdP must support the **Force AuthnRequest** attribute, or e-signature isn’t supported.

4.  On the eSignature Approval tab, enter the following e-signature SAML properties.

<table id="choicetable_b2l_vpw_lz"><tbody><tr><td id="d188204e107">

**Assertion Consumer URL for eSignature authentication**

</td><td>

This property defaults to the appropriate URL. To configure this property, select the lock icon to make this field editable. After edits, select the icon to lock the field.

</td></tr><tr><td id="d188204e116">

**Assertion Consumer Index for eSignature authentication**

</td><td>

If your Service Provider has more than one URL set for the AssertionConsumerURL, you can set the index to use for eSignature, starting with index 1 or more.

</td></tr><tr><td id="d188204e128">

**AuthnRequest URL for eSignature Authentication**

</td><td>

You can enter the URL that points to the SAML 2.0 IdP AuthnRequest URL for eSignature authentication. If the URL is the same as the Assertion Consumer URL, you can leave this setting empty.

</td></tr><tr><td id="d188204e137">

**Authentication pop-up Dialog Width**

</td><td>

When a user approves a request using eSignature, a dialog opens and a user can enter credentials. This setting controls the width of that dialog box. The default is 500.

</td></tr><tr><td id="d188204e146">

**Authentication pop-up Dialog Height**

</td><td>

When a user approves a request using eSignature, a dialog opens and a user can enter credentials. This setting controls the height of that dialog box. The default is 300.

</td></tr></tbody>
</table>    ![eSignature Approval Tab](../image/esignature_approval_tab.png)

5.  Select the **Generate Metadata** button underneath the tabs to regenerate the service provider metadata.

6.  Copy the service provider metadata, and update it on the SAML IdP.


