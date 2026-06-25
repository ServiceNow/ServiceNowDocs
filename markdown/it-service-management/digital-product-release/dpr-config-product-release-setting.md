---
title: Configure product-level release settings
description: Configure release settings for a product or service that are applied whenever a release is created or executed for that product.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-config-product-release-setting.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 2
keywords: [product-level settings, release settings, configure product]
breadcrumb: [Use, Digital Product Release, IT Service Management]
---

# Configure product-level release settings

Configure release settings for a product or service that are applied whenever a release is created or executed for that product.

## Before you begin

Role required: sn\_dpr\_model.release\_admin or sn\_dpr\_model.product\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the products and services icon \(\[Omitted image "dpr-icon-products.png"\] Alt text: Products and services icon.\).

3.  Select a product or service from the list.

4.  Select **Release settings**.

5.  Configure the release defaults for the product.

    **Note:** If you don't set these values, all respective records are displayed when you create releases.

<table id="table_g4z_yhj_cjc"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Release readiness dates

</td><td>

Option to enable scheduling of releases for the product outside defined release targets.This setting appears when the **sn\_dpr.out\_of\_band\_release\_allowed** system property value is true.

</td></tr><tr><td>

Release calendars

</td><td>

Calendars available for targeting releases.

</td></tr><tr><td>

Release templates

</td><td>

Release templates that can be applied to new releases.

</td></tr><tr><td>

Change models

</td><td>

Controls which change models and standard change templates are available when creating and linking change requests for a release.**Note:** This list displays only those change models that have **Available in 'Create New'** selected and standard change templates that are active.

</td></tr><tr><td>

CI classes

</td><td>

Determines the CI selection available during release execution to the CI classes most relevant to the product.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

The release settings for the product are saved and are used in the following flows:

-   The release creation flows show only the configured templates and calendars by default.
-   Change request creation shows only the configured change models and standard change templates.
-   Configuration item selection shows only CIs of the configured classes.

**Parent Topic:**[Using Digital Product Release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-using-digital-product-release.md)

**Related topics**  


[Create a release with a wizard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-release-guided.md)

[Create a release for a product or service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-release.md)

[Create a release readiness target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-create-rls-readiness-target.md)

[Manage change requests in a release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-work-release-change-request.md)

[Manage configuration items in a release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-work-release-config-items.md)

