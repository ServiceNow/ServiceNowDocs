---
title: Create TRM product form
description: The Create TRM product form lets you add a software or hardware product directly to the TRM library. The record is created immediately without an approval request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-new-trm-prod-form.html
release: australia
topic_type: reference
last_updated: "2026-07-23"
reading_time_minutes: 2
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Create TRM product form

The Create TRM product form lets you add a software or hardware product directly to the TRM library. The record is created immediately without an approval request.

## Details section

<table id="table_details_section"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

The type of the TRM product. Select **Software** or **Hardware**. The fields displayed in the form change based on the type selected.

</td></tr><tr><td>

Company

</td><td>

Company of the TRM product. Look up and select a company from the list.

</td></tr><tr><td>

Category

</td><td>

Category of the product. Look up and select a category from the TRM Categories page.

</td></tr><tr><td>

Name

</td><td>

Name of the TRM product.

</td></tr><tr><td>

TRM Phase

</td><td>

Phase of the product. Use the following list:-   Approved
-   Approved with Constraints
-   Divest
-   Evaluation
-   Unapproved

</td></tr><tr><td>

Investment direction

</td><td>

Purpose for the investment. Use the following list:-   Divest
-   Eliminated
-   Invest
-   Maintain

</td></tr><tr><td>

Business Justification

</td><td>

Business justification for the product.

</td></tr><tr><td>

Approval

</td><td>

The approval status of the TRM product. Defaults to **Not Yet Requested** when the form opens.

</td></tr></tbody>
</table>## TRM product lifecycles section

This section appears on the **TRM product lifecycles** tab. After you fill in the mandatory fields on the **Details** tab, select **Add version/edition** to display the lifecycle fields and add a lifecycle record. Adding lifecycle records is optional.

**Note:**

-   For software products: You can add up to 5 version and edition combinations, with a maximum of 10 phases per combination.
-   For hardware products: You can add up to 5 hardware models, with a maximum of 10 phases per hardware model.

<table id="table_lifecycle_section"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version

</td><td>

The version of the TRM software product. This field appears only when a TRM product of type Software is selected in the **Type** field.To create a TRM software product lifecycle with a wildcard, end the version with an asterisk \(\*\).

</td></tr><tr><td>

Edition

</td><td>

The edition of the TRM software product. This field appears only when a TRM product of type Software is selected in the **Type** field.

</td></tr><tr><td>

Hardware model

</td><td>

The hardware model for the lifecycle record. This field appears only when a TRM product of type Hardware is selected in the **Type** field.

</td></tr><tr><td>

TRM phase

</td><td>

Phase of the product lifecycle. Look up and select a phase from the TRM Phases as defined in the Setup page \(Enterprise Architecture Workspace &gt; Setup &gt; TRM Phases\). This field is required.

</td></tr><tr><td>

Phase start date

</td><td>

Start date of the product lifecycle phase. This field is required.

</td></tr><tr><td>

Phase end date

</td><td>

End date of the product lifecycle phase.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[Request a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-request-a-trm-products.md)

[Add or edit your TRM products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-edit-my-trm-prod.md)

[Create a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle.md)

