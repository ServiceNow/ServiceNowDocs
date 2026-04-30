---
title: Deduplicating IBM software installations
description: To track and manage your IBM licenses, you can integrate the IBM publisher pack with an authorized Software Asset Management provider, IBM License Metric Tool \(ILMT\), or BigFix Inventory. If you are switching between an authorized Software Asset Management provider integration and either an ILMT or BigFix Inventory integration, you can deduplicate software installations that have the same edition, version, and language but are discovered through different sources.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Deduplicating IBM software installations

To track and manage your IBM licenses, you can integrate the IBM publisher pack with an authorized Software Asset Management provider, IBM License Metric Tool \(ILMT\), or BigFix Inventory. If you are switching between an authorized Software Asset Management provider integration and either an ILMT or BigFix Inventory integration, you can deduplicate software installations that have the same edition, version, and language but are discovered through different sources.

If you discover the same IBM software installation through multiple sources, such as Anglepoint and ILMT, the Software Asset Management application creates a separate software installation record for each discovery of that software installation. You can resolve these duplicate software installation records by running the **SAM - Deduplicate Install Table** scheduled job, which ensures that only one duplicate software installation record is marked as active and included in reconciliation. See [Duplicate software installations in the Software Asset Management application](deduplicating-software-installations-sam.md) for more information on deduplication.

By default, the Software Asset Management application prioritizes IBM software installations that are discovered through ILMT or BigFix Inventory. When you run the **SAM - Deduplicate Install Table** scheduled job, records for all IBM software installations that are discovered through ILMT or BigFix Inventory are marked as active, while records for the same software installations that are discovered through an authorized Software Asset Management provider are marked as inactive. If an IBM software installation is discovered through an authorized Software Asset Management provider only, the corresponding record is marked as active.

To prioritize IBM software installations that are discovered through authorized Software Asset Management providers instead, you can update the value of the **Use Servicenow Software Asset Management and Discovery for IBM license compliance** property \(**com.snc.samp.ibm.use\_samp\_ibm\_licensing**\) by navigating to **All** &gt; **System Properties** &gt; **All Properties**. From the list of available system properties, search for and select the **com.snc.samp.ibm.use\_samp\_ibm\_licensing** property. When the system property record opens, set the **Value** field to `true` and then select **Update**. Each time you subsequently run the **SAM - Deduplicate Install Table** scheduled job, records for all IBM software installations that are discovered through an authorized Software Asset Management provider are marked as active, while records for the same software installations that are discovered through ILMT or BigFix Inventory are marked as inactive. If an IBM software installation is discovered through ILMT or BigFix Inventory only, the corresponding record is marked as active.

**Note:** The **Use Servicenow Software Asset Management and Discovery for IBM license compliance** property supports domain separation.

**Parent Topic:**[Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md)

