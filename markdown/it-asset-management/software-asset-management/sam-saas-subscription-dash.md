---
title: Office 365 &amp; Adobe Cloud dashboard in Software Asset Management classic
description: View compliance analysis results related to Microsoft Office 365 and Adobe Cloud License Management in Software Asset Management classic.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for Adobe, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Office 365 &amp; Adobe Cloud dashboard in Software Asset Management classic

View compliance analysis results related to Microsoft Office 365 and Adobe Cloud License Management in Software Asset Management classic.

**Note:** The Office 365 &amp; Adobe Cloud dashboard is no longer available for new Yokohama users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Yokohama without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Yokohama. If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Yokohama but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to this dashboard. If you activated the workspace plugin \(before or after upgrading to Yokohama, you won’t be able to access this dashboard from the **Software Asset** navigation menu in your instance. You can however access this dashboard from the **Dashboards** navigation menu.

Access the dashboard by navigating to **All** &gt; **Software Asset** &gt; **Office 365 &amp; Adobe Cloud**.

You can filter by **Subscription Software Models** or **Subscription Publisher** using filter lists.

**Note:** The Subscription Publisher filter list always includes Microsoft and Adobe even when only one subscription publisher pack is active.

The dashboard is updated whenever a new reconciliation result is available. You can save charts in PNG or JPG format.

## Adobe

You can manage Adobe subscription information with Adobe I/O authentication integration.

**Note:** The add-on Adobe publisher pack \(com.sn\_samp\_adobe\) [plugin](../task/t_RequSoftwareAssetMgmt.md) must be installed to view Adobe subscription reporting.

Only Adobe software products that are recognized as subscription software are shown. [Adobe integration](adobe-cloud-integration.md) must be set up to view compliance information.

-   List of Active Subscriptions with no Active Adobe Software installs

    If a user has an active subscription but does not have any respective Adobe suite of products deployed.

    User Name \| Email ID \| Subscription Name \| List of devices assigned to users.

-   Optimization of Adobe install using SCCM metering data

    If user is underutilizing Adobe subscriptions

    User Name \| Email ID \| Subscription Name \| Subscription Cost \| List of devices assigned to users \| List of Adobe suite of products \| Last Access Time


## SaaS subscription reports

![](../image/SAMDash365.png "Office 365 and Adobe Cloud")

**Parent Topic:**[Software Asset Management publisher pack for Adobe](adobe-publisher-pack.md)

