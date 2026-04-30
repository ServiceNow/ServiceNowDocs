---
title: Components installed with Localization Framework
description: The Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activates several related plugins that are not already active. With installation of the core plugins, optional plugins for the Localization Framework Hub and Spoke architecture are available.
locale: en-US
release: zurich
product: Localization Framework
classification: localization-framework
topic_type: reference
last_updated: "2026-03-16"
reading_time_minutes: 1
breadcrumb: [Activating the Localization Framework, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer]
---

# Components installed with Localization Framework

The Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) activates several related plugins that are not already active. With installation of the core plugins, optional plugins for the Localization Framework Hub and Spoke architecture are available.

<table id="table_ul5_xyw_xjb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Localization Framework \[com.glide.localization\_framework\]

</td><td>

Manage localization workflows across the platform and products.

</td></tr><tr><td>

Localization Framework for Service Catalog\[com.glide.localization\_framework.service\_catalog\]

</td><td>

Enables translation of Service Catalog items using Localization Framework.

</td></tr><tr><td>

Localization Framework for Virtual Agent Topic\[com.glide.localization\_framework.va\]

</td><td>

Enables translation of Virtual Agent topics using Localization Framework.

</td></tr><tr><td>

RWS Translation Management System Spoke for Localization Framework \[com.glide.localization\_framework.sdl\_spoke\]

</td><td>

Integrates Localization Framework with the RWS Translation Management System.

</td></tr><tr><td>

XTM Translation Management System Spoke for Localization Framework \[com.glide.localization\_framework.xtm\_spoke\]

</td><td>

Integrates Localization Framework with the XTM Translation Management System.

</td></tr></tbody>
</table><table id="table_n5b_lnk_d1c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Localization Framework Hub \[com.sn.localization\_framework.hub\]

Scope: sn\_lf\_hub

</td><td>

It's a framework that enables to fulfill the translation requests received from Localization Framework Spoke. After installation and configuration, the hub instance manages incoming translation requests.For more information, see [Localization Framework Hub and Spoke architecture](../concept/localization-framework-hub-spoke-architecture.md).

</td></tr><tr><td>

Localization Framework Spoke\[com.sn.localization\_framework.spoke\]

Scope: sn\_lf\_spoke

</td><td>

It's a framework that enables to fulfill the translation requests using Localization Framework Hub. After installation and configuration, the spoke instance submits its translation requests to the hub.

</td></tr></tbody>
</table>## Tables installed with Localization Framework

<table id="table_x51_3h5_p3c"><thead><tr><th>

Table label

</th><th>

Table name

</th></tr></thead><tbody><tr><td>

Settings

</td><td>

sn\_lf\_setting

</td></tr><tr><td>

Artifact Configurations\(Sn Lf Config\)

</td><td>

sn\_lf\_config

</td></tr><tr><td>

Localization Insight\(Sn Lf Insight\)

</td><td>

sn\_lf\_insight

</td></tr><tr><td>

Localization Project\(Sn Lf Project\)

</td><td>

sn\_lf\_project

</td></tr><tr><td>

Loclization Requested Item\(Sn Lf Requested Item\)

</td><td>

sn\_lf\_requested\_item

</td></tr><tr><td>

Localization Task\(Sn Lf Task\)

</td><td>

sn\_lf\_task

</td></tr><tr><td>

TMS Configuration\(Sn Lf Tms Config\)

</td><td>

sn\_lf\_tms\_config

</td></tr></tbody>
</table>**Parent Topic:**[Activating the Localization Framework](../concept/activation-localization-framework.md)

**Related topics**  


[Find components installed with an application](../../plugins/task/find-components.md)

