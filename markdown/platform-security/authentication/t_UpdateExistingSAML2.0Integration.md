---
title: Update your existing SAML 2.0 integration
description: Update your existing SAML 2.0 integration.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Update your existing SAML 2.0 integration

Update your existing SAML 2.0 integration.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

Request the SAML 2.0 Update 1 plugin. Contact Customer Service and Support to request the SAML 2.0 Single Sign-On - Update 1: security enhancements plugin. The plugin applies updated versions of the SAML2SingleSignon installation exit \(login script\), SAML2Logout installation exit \(logout script\), and SAML2 script include \(script object\).

Merge customizations from existing installation exit scripts into new scripts. The update saves an inactive copy of the integration's original installation exit scripts. You can use these copies to merge any customizations that you made to the login and logout scripts to the new versions of these installation exits.

|Original Installation Exit Script Name|Original Script Status|New Installation Exit Script Name|New Script Status|
|--------------------------------------|----------------------|---------------------------------|-----------------|
|SAML2SingleSignon|Inactive|SAML2SingleSignon\_update1|Active|
|SAML2|Inactive|SAML2\_update1|Active|
|SAML2Logout|Inactive|SAML2Logout\_update1|Active|

You can navigate to the SAML 2.0 login and logout installation exit scripts using these paths:

-   **SAML 2 Single Sign-on** &gt; **Login script**.
-   **SAML 2 Single Sign-on** &gt; **Logout script**.
-   **System Definition** &gt; **Installation Exits**.

You can navigate to the SAML 2.0 update 1 script include using these paths:

-   **SAML 2 Single Sign-on** &gt; **Script object**.
-   **System Definition** &gt; **Script Includes**.

Test the Update.

## Procedure

1.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) called glide.authenticate.sso.saml2.debug with a value of true.

2.  Attempt SAML 2.0 login.

3.  Review the system log.

    SAML2 validation errors begin with the text SAML2ValidationError.

4.  Identify and fix typical login errors.

    For more information, see [Multi-SSO \(SAML 2.0\) errors and fixes](../reference/saml-errors.md).


