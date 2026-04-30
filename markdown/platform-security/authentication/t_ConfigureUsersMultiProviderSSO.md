---
title: Configure users for Multi-Provider SSO
description: Administrators can configure Multi-Provider SSO for individual users or for all users who belong to a company. You cannot configure Multi-Provider SSO for groups.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Configure users for Multi-Provider SSO

Administrators can configure Multi-Provider SSO for individual users or for all users who belong to a company. You cannot configure Multi-Provider SSO for groups.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Right-click an identity provider record and select **Copy sys\_id**.

3.  Copy the data to your clipboard.

4.  Navigate to a user record or a company record.

5.  Configure the form and add the **SSO Source** field.

6.  In the **SSO Source** field, enter one of the following:

    -   **SAML users**: enter **sso:** followed by the sys\_id of the identity provider's record.
    -   **SSO Federation users**: enter **federation:** followed by the sys\_id of the federation record.
7.  Click **Update**.


