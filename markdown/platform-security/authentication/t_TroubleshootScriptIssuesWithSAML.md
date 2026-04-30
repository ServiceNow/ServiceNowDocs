---
title: Troubleshoot script issues with SAML
description: Troubleshoot script issues with SAML. You might encounter script issues if SAML is already active at the time that you activate Multiple Single Sign-On and if you already customized the installation exits.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Testing IdP connections, Multi-Provider SSO configurations, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Troubleshoot script issues with SAML

Troubleshoot script issues with SAML. You might encounter script issues if SAML is already active at the time that you activate Multiple Single Sign-On and if you already customized the installation exits.

## Before you begin

Role required: admin

## Procedure

1.  Back up the modified installation exit SAML2SingleSignon\_update1 and script include SAML2\_update1.

2.  Revert both the installation exit and script include to the version that is available with the baseline system.

3.  Activate or upgrade the **Integration - Multiple Provider Single Sign-On Installer** plugin.

    The system upgrades SAML and all necessary files to SAML 2 Update 1.

4.  Open the Multiple SSO properties page and select the **Enable Multi-Provider SSO** check box to enable it.

5.  Put the SAML2SingleSignon\_update1 installation exit changes into the baseline script include **MultiSSO\_SAML2\_Update1 and the SAML2\_update1** script include changes into the baseline SAML2\_update1 script include.


