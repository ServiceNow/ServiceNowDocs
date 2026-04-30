---
title: SAML user provisioning
description: If users exist in your IdP but are not in your instance, SAML user provisioning can automatically create the users in your instance's User \[sys\_user\] table.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# SAML user provisioning

If users exist in your IdP but are not in your instance, SAML user provisioning can automatically create the users in your instance's User \[sys\_user\] table.

SAML user provisioning is supported for SAML 2.0 Update 1 when Multi-SSO is enabled.

## How SAML user provisioning works

When SAML user provisioning is enabled and the system encounters a new user that is not in the instance, the instance automatically creates a record in a temporary table with the name `u_imp_saml_user_<suffix>`, where `<suffix>` is an automatically generated text identifier. The system also creates transform map that specifies the data relationships between the import table and the User table. Each IdP in identified in the system has its own transform map. The transform map is created once for each IdP. Administrators can update it as necessary.

When the user logs in, they access an IdP to log in.

-   The system presents a list of all IdPs that are able to use SAML user provisioning. If there is only one IdP that can use SAML user provisioning, that one is used automatically.
-   If none of the above conditions are true, the system uses the [Auto Redirect IdP](../../single-sign-on/task/t_CreateASAML2Upd1SSOConfigMultiSSO.md).

