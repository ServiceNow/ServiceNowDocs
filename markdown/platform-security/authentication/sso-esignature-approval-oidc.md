---
title: Use Multi-Provider SSO to set up an SSO approval for an OIDC authentication
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

# Use Multi-Provider SSO to set up an SSO approval for an OIDC authentication

An SSO approval with e-signature requires configuration on the SAML IdP and the ServiceNow instance.

## Before you begin

Role required: admin

## About this task

The SAML IdP must support and honor the forceAuthn attribute in SAML assertion requests. E-signature doesn’t function without this IdP setting. Set up an approval with e-signature using credentials from a SAML 2.0 authentication.

## Procedure

1.  Activate the [Approval with E-Signature plugin](activate-approval-esignature.md).

2.  Navigate to **Multi-Provider SSO** &gt; **Identity Providers** and verify your OIDC provider configurations

3.  On the eSignature Approval tab, enter the following e-signature SAML properties.

<table id="choicetable_b2l_vpw_lz"><tbody><tr><td id="d156554e73">

**Assertion Consumer URL for eSignature authentication**

</td><td>

This property defaults to the appropriate URL. To configure this property, select the lock icon to make this field editable. After edits, select the icon to lock the field.

</td></tr><tr><td id="d156554e82">

**Authentication pop-up Dialog Width**

</td><td>

When a user approves a request using eSignature, a dialog opens and a user can enter credentials. This setting controls the width of that dialog box. The default is 800.

</td></tr><tr><td id="d156554e91">

**Authentication pop-up Dialog Height**

</td><td>

When a user approves a request using eSignature, a dialog opens and a user can enter credentials. This setting controls the height of that dialog box. The default is 900.

</td></tr></tbody>
</table>    ![OIDC eSignature Approval](../image/sso-esignature-approval-oidc.png)

4.  Select **Submit** if you are configuring the E-signature during the initial OIDC setup or **Update** if you want to update the details in the E-signature.


