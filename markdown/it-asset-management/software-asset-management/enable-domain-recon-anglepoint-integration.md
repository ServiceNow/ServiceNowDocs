---
title: Enable IBM reconciliation for specific domains
description: If you are using domain separation for the integration between the Software Asset Management publisher pack for IBM and an Authorized SAM Provider \(ASP\), enable IBM reconciliation only for specific domains.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Enable IBM reconciliation for specific domains

If you are using domain separation for the integration between the Software Asset Management publisher pack for IBM and an Authorized SAM Provider \(ASP\), enable IBM reconciliation only for specific domains.

## Before you begin

Role required: asset or domain\_admin

## Procedure

1.  Open the Domain Asset Process Settings \[alm\_domain\_asset\_process\_setting\] table by navigating to **All** &gt; **alm\_domain\_asset\_process\_setting\_list.do**.

2.  Double-click the **Run asset process** field for the domain that you want to enable reconciliation for.

3.  When prompted, set the value to **true** and then select the Save icon ![](../image/save-icon.png).

4.  Repeat steps 2 and 3 for each domain that you want to enable reconciliation for.

    **Important:** If you have both parent and child domains, you can enable reconciliation for either the parent domain or child domain. You cannot enable reconciliation for both parent and child domains.


**Parent Topic:**[Authorized SAM Provider \(ASP\) integrations for IBM](../concept/ibm-asp-integration.md)

