---
title: Add a new company
description: You can add companies that represent vendors, manufacturers, or customers with whom you do business. These companies provide a way to categorize users, groups, and assets.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating users, companies, departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a new company

You can add companies that represent vendors, manufacturers, or customers with whom you do business. These companies provide a way to categorize users, groups, and assets.

## Before you begin

Role required: user\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Companies**.

2.  Click **New**.

3.  Complete the form with the company details.

<table id="table_x3s_msg_m4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the company.

</td></tr><tr><td>

Phone

</td><td>

Company phone number.

</td></tr><tr><td>

Fax phone

</td><td>

Company fax number.

</td></tr><tr><td>

Manufacturer

</td><td>

Whether the company is a manufacturer.

</td></tr><tr><td>

Vendor

</td><td>

Whether the company is a vendor.

</td></tr><tr><td>

Stock symbol

</td><td>

Three or four letter stock symbol for the company.

</td></tr><tr><td>

Stock price

</td><td>

Current price at which company stock is sold.

</td></tr><tr><td>

Street

</td><td>

Mailing street address of the company.

</td></tr><tr><td>

City

</td><td>

City in which the company is located.

</td></tr><tr><td>

State

</td><td>

State or province in which the company is located.

</td></tr><tr><td>

Zip/Postal code

</td><td>

Zip or postal code for the company.

</td></tr><tr><td>

Notes

</td><td>

Any information about the company that would be helpful for others to know.

</td></tr><tr><td class="sub-head" colspan="2">

Fields that can be added by Personalize a form:

</td></tr><tr><td>

Latitude

</td><td>

The latitude of the company, if applicable. This field is populated by a business rule called **get\_lat\_long**. Deactivate this business rule to prevent the system from overwriting any values populated in the field manually. Latitude is expressed as a floating point data type. Latitude from upgraded versions of ServiceNow expressed in any format other than floating point appears in a column called **Old Latitude**. The system attempts to convert all latitude values from previous versions to the floating point notation, where possible.**Note:** This field doesn't display by default. You can add it by personalizing the form.

</td></tr><tr><td>

Longitude

</td><td>

The longitude of the company, if applicable. This field is populated by a business rule called **get\_lat\_long**. Deactivate this business rule to prevent the system from overwriting any values populated in the field manually. Longitude is expressed as a floating point data type. Longitude from upgraded versions of ServiceNow expressed in any format other than floating point appears in a column called **Old Longitude**. The system attempts to convert all longitude values from previous versions to the floating point notation, where possible.**Note:** This field doesn't display by default. You can add it by personalizing the form.

</td></tr></tbody>
</table>    **Note:** The IT Finance application adds a Finance view to the Company form. The Finance view adds a chart that shows expenses that were allocated to the company.


## What to do next

Normalize company data to create consistency when referring to a company name, such as a vendor or manufacturer. For more information see, [Normalization data services](../../normalization/concept/c_NormalizationOverview.md).

**Parent Topic:**[Creating users, companies, and departments](../../roles/concept/using-user-administration.md)

