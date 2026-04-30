---
title: Test the ADFS configuration
description: Test your ADFS configuration to verify that it is properly functioning as an identity provider.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Test the ADFS configuration

Test your ADFS configuration to verify that it is properly functioning as an identity provider.

## Before you begin

Role required: admin

## Procedure

1.  Open an Internet Explorer browser.

2.  Navigate to your ADFS portal.

    For example, `https://samportal.example.com/adfs/ls/idpinitiatedsignon.aspx`. This page contains a drop-down list of all configured Relying Party Trusts.

3.  Select the relying party that is associated with your instance.

4.  Click **Continue to Sign In**.

    If you have configured the SAML 2.0 external authentication properly, you should be automatically logged into the instance.

5.  Test a direct login URL by navigating to `https://samportal.example.com/adfs/ls/idpinitiatedsignon.aspx?logintoRP=https://company.service-now.com`.


