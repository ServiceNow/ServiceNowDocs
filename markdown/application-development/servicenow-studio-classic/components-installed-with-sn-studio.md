---
title: Components installed with ServiceNow Studio
description: Activating the ServiceNow Studio plugin installs tables, roles, and dependencies automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/components-installed-with-sn-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Installing ServiceNow Studio, Configure, ServiceNow Studio, Developing your application, Building applications]
---

# Components installed with ServiceNow Studio

Activating the ServiceNow Studio plugin installs tables, roles, and dependencies automatically.

## What tables and roles does ServiceNow Studio install?

|Table|Description|
|-----|-----------|
|Resources \[sn\_sns\_resources\]|Populates the Resources section at the bottom of the home page.|
|Experience Configurations \[sn\_udc\_experience\_configuration\]|Stores default role access configurations for the experience switcher. This table is not configurable.|
|Experience Visibility Controls \[sn\_udc\_experience\_visibility\_control\]|Enables you to grant non-default roles access to the experience switcher. This table is configurable.|

ServiceNow Studio does not include specific roles. The Admin and Delegated Developer roles are used. For more information, see [ServiceNow Studio personas and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-personas-roles.md).

## What plugin does ServiceNow Studio install?

The ServiceNow Studio \[sn\_sns\] plugin installs with several dependencies.

<table id="table_xfk_wxh_zdc"><thead><tr><th>

Plugin \[ID\]

</th><th>

Description

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

ServiceNow Studio\[sn\_sns\]

</td><td>

ServiceNow Studio provides a unified environment for all ServiceNow development activities.

</td><td>

-   sn\_udc
-   sn\_studio\_commons
-   sn\_app\_obj\_wizards
-   sn\_deploy\_pipeline

</td></tr></tbody>
</table>**Parent Topic:**[Installing ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/installing-servicenow-studio.md)

