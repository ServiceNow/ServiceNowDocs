---
title: Update the OIDC entities table
description: Update the OIDC entities table to replace dummy values created by the registry file with your Microsoft Teams tenant values.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Employee Center with Microsoft Teams for GCC-H or DoD, Microsoft Teams for GCC-H or DoD, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Update the OIDC entities table

Update the OIDC entities table to replace dummy values created by the registry file with your Microsoft Teams tenant values.

## Before you begin

Role required: admin

## Procedure

1.  In the Navigation filter, enter `oauth_oidc_entity_list.do`.

2.  Select the ServiceNow for Microsoft Teams App record.

3.  In the **Client ID** field in the OAuth OIDC entities table, enter `api://INSERT_COMPLETE_INSTANCE_URL_without_http(s)/ APPLICATION (CLIENT) ID`.

4.  Select the reference icon ![Reference icon](../../../common/image/Form_ReferenceLookupIcon.png) beside the **OAuth OIDC Provider Configuration** field.

5.  Select **Open Record**.

6.  In the **OIDC Metadata URL** field in the OIDC Provider Configuration table, enter your directory \(tenant\) Id.

7.  Select **Update**.


**Parent Topic:**[Integrating Employee Center with Microsoft Teams for GCC-H or DoD](../concept/ec-teams-integration-gcch.md)

