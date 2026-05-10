---
title: Setting up Insurance claims workspaces and dashboards
description: You can set up the workspace and dashboards for each persona by using the Insurance claims application.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Insurance claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Setting up Insurance claims workspaces and dashboards

You can set up the workspace and dashboards for each persona by using the Insurance claims application.

## Workspaces included in Insurance claims

The following workspaces are included in Insurance claims:

-   Claim Summary \(360\)
-   Claim Workspace

For more information about these workspaces, see [Insurance claims landing pages and workspaces](insurance-claims-flow-workspace.md).

You can modify these workspaces in UI Builder. You can also customize the subpages in these workspaces by creating a variant. For more information about this customization, see [Create a page variant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-variant.md).

## Setting up workspaces by persona

The following table lists some guidelines on how to set up a workspace for each persona.

<table id="table_mzq_2yv_zcc"><thead><tr><th>

Element

</th><th>

Persona

</th><th>

Guidelines

</th></tr></thead><tbody><tr><td rowspan="3">

Landing page

</td><td>

FNOL Representative

</td><td>

This common landing page is defined in the FSO Core and can be used as-is with little modification.To make additional UI changes, use UI Builder. For more information, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md).

</td></tr><tr><td>

Processor

</td><td>

Create a landing page for the line of business by basing it on an existing landing page. Refer to the included Claims Processor landing page as an example by navigating to **All** &gt; **Platform Analytics** &gt; **Dashboards**, and then selecting **Claims Processor Landing Page**.

</td></tr><tr><td>

Adjuster

</td><td>

Create a landing page for your line of business by basing it on an existing landing page. Refer to the included Claims Adjuster landing page as an example by navigating to **All** &gt; **Platform Analytics** &gt; **Dashboards**, and then selecting **Claims Adjuster Landing Page**.

</td></tr><tr><td rowspan="3">

Modules and Lists

</td><td>

FNOL Representative

</td><td>

This module or list is defined by the base system for Insurance claims. To make additional UI changes, use UI Builder. For more information, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md).

</td></tr><tr><td>

Processor

</td><td>

This module or list is defined by the base system for Insurance claims.For a new line of business, create list categories and lists for the processor role.

</td></tr><tr><td>

Adjuster

</td><td>

This module or list is defined by the base system for Insurance claims.For a new line of business, create list categories and lists for the adjuster role.

</td></tr><tr><td>

Record

</td><td>

All

</td><td>

Other workspace-related configuration, like the changes that are related to a record, can be done through UI Builder. By default, Insurance claims uses the Record default configuration from the Customer Service Management \(CSM\) application.For more information, see [Workspaces](../../fso-common/concept/fso-workspace.md) and [Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md).

</td></tr><tr><td>

Claim workspace

</td><td>

Adjuster

</td><td>

This adjuster workspace UI Builder page has been set up in Insurance claims.If necessary, you can clone this workspace and modify it to be more specific to your particular line of business.

For more information, see [Workspaces](../../fso-common/concept/fso-workspace.md) and [Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md).

</td></tr><tr><td>

Claim summary \(360\) page

</td><td>

Processor, Adjuster, Manager

</td><td>

The Claim 360 UI Builder page is set up in theFSO Core and is available in claims applications. It can be cloned and modified to create a specific claim summary page for a particular line of business.To enable a claim summary on a case, enable the CSM default record page and define the correct order.

For more information, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-overview.md).

</td></tr></tbody>
</table>## Dashboards included in Insurance claims

To modify the conditions on the landing pages, navigate to **All** &gt; **Platform Analytics** &gt; **Dashboards**. Select the dashboards and edit them by using UI Builder.

For more information on the included dashboards and their layouts, see [Insurance claims landing pages and workspaces](insurance-claims-flow-workspace.md).

**Note:** The FNOL landing page is built into Financial Services Operations Core. Any changes to this page may impact other applications.

For more information on landing pages as dashboards, see [Dashboard landing pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-ws-landing-page-dashboard.md).

