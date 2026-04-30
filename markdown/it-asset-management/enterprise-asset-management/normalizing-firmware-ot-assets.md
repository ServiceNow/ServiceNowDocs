---
title: Normalizing firmware for your operational technology \(OT\) assets
description: To standardize the publisher, product, and version of the firmware that is embedded into your OT assets, you must normalize the corresponding data in the associated firmware discovery models. By standardizing this information, you can track and manage your firmware more accurately and efficiently.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Normalizing firmware for your operational technology \(OT\) assets

To standardize the publisher, product, and version of the firmware that is embedded into your OT assets, you must normalize the corresponding data in the associated firmware discovery models. By standardizing this information, you can track and manage your firmware more accurately and efficiently.

**Note:** You can standardize this information only in the OT Asset Management application. See [OT Asset Management](ot-asset-management.md) for more information on the application.

To begin standardizing this information, you must use a discovery tool, such as the ServiceNow® Discovery application, to discover all firmware installations across your OT asset deployment. Each discovered firmware installation is associated with a corresponding firmware discovery model, which provides information about the discovered firmware publisher, discovered firmware product, and discovered firmware version. After the discovery process is complete, normalization runs on the associated firmware discovery models, matching the discovered firmware publishers, discovered firmware products, and discovered firmware versions against normalized equivalents in the Enterprise Asset Management Content Library. Each discovered firmware installation is then updated with a firmware model containing the normalized firmware publisher, firmware product, and firmware version that best match the associated firmware discovery model.

If a specific United Nations Standard Products and Services Code \(UNSPSC\) firmware classification, firmware product, firmware version, or Customer Premises Equipment \(CPE\) firmware mapping is not available in the Enterprise Asset Management Content Library, you can create a custom UNSPSC firmware classification, custom firmware product, custom firmware version, or custom CPE firmware mapping.

