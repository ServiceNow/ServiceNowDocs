---
title: Add or delete tag keys for Tag Categorization
description: Tag keys define the values available within a tag category. Add or delete tag keys to keep your tag categorization structure current as data management and classification requirements change.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/tag-governance/update-tag-keys-tag-categorization.html
release: yokohama
product: Tag Governance
classification: tag-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Add or delete tag keys for Tag Categorization

Tag keys define the values available within a tag category. Add or delete tag keys to keep your tag categorization structure current as data management and classification requirements change.

## Before you begin

Verify that you have installed version 1.16.3 of Service Mapping Plus to access to the CI tag category and CI tag key tables. For more information, see [Install Service Mapping Plus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/service-mapping/install-service-mapping-plus.md).

Role required: tag\_governance\_admin

## Procedure

1.  Navigate to **All** &gt; **Tag Governance** &gt; **Tag Categories**.

2.  Verify that you're in the leaf domain.

    1.  In the page header, select the globe icon \[Omitted image "globe-outline-24.svg"\].

    2.  Select **Domain scope**, and choose the appropriate leaf domain.

3.  Select the tag category to which you want to add or delete tag keys.

4.  Under **CI tag keys**, either add a tag key or delete an existing tag key.

<table id="choicetable_dvx_hzd_5fc"><thead><tr><th align="left" id="d563500e139">

Action

</th><th align="left" id="d563500e142">

Steps

</th></tr></thead><tbody><tr><td id="d563500e148">

**Add a tag key**

</td><td>

1.  Double-click the empty row under **Tag key**, where you see **Insert a new row**.
2.  In the field, add a key name.
3.  Select the check mark icon \(\[Omitted image "icon-check-mark.png"\]\) to save the tag key.
4.  Repeat the previous steps to add more tag keys.
5.  Select **Update** to save your changes.


</td></tr><tr><td id="d563500e186">

**Delete a tag key**

</td><td>

1.  Under **Tag key**, select the delete icon \(\[Omitted image "marked-for-deletion.png"\]\) next to the tag key you want to remove.
2.  Select **Update** to save your changes.


</td></tr></tbody>
</table>5.  If you want to apply your changes immediately rather than waiting for the automatic update within 24 hours, select the **Re-Categorize Tags** button.


