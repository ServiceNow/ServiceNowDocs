---
title: Grant or restrict access to an external link
description: Control who can access external links by setting the user criteria, which allows access only to specific users, groups, roles, and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/employee-experience-foundation/grant-restrict-external-link.html
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an external link, Quick links, Customize the Employee Center with widgets, Configure your Employee Center portal, Configure, Employee Center, Employee Service Management]
---

# Grant or restrict access to an external link

Control who can access external links by setting the user criteria, which allows access only to specific users, groups, roles, and more.

## Before you begin

Role required: sp\_admin, taxonomy\_admin, or taxonomy\_manager

## Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **External Links**.

    The External Links module displays the list of existing external links.

2.  Click the external link that you want to grant or restrict access to.

3.  To grant access to the external link, click the **Available For** tab.

<table><thead><tr><th align="left" id="d475233e80">

To

</th><th align="left" id="d475233e83">

Do this

</th></tr></thead><tbody><tr><td id="d475233e89">

**Add a new user criteria**

</td><td>

1.  Click **New**.
2.  On the form, fill in the fields. For more information about the form fields and descriptions, see [User Criteria form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/ec-user-criteria-form.md)
3.  Click **Submit**.


</td></tr><tr><td id="d475233e123">

**Edit an existing user criteria**

</td><td>

1.  Click **Edit**.
2.  On the Edit Members form, select the required roles, users, and groups in the Collection column and move them to the Available For List column by clicking the right arrow icon \(\[Omitted image "right-arrow-icon.png"\] Alt text: Right arrow icon.\).
3.  Click **Save**.


</td></tr></tbody>
</table>4.  To restrict access to the external link, click the **Not Available For** tab.

<table><thead><tr><th align="left" id="d475233e169">

To

</th><th align="left" id="d475233e172">

Do this

</th></tr></thead><tbody><tr><td id="d475233e178">

**Add a new user criteria**

</td><td>

1.  Click **New**.
2.  On the form, fill in the fields. For more information about the form fields and descriptions, see [User Criteria form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/ec-user-criteria-form.md)
3.  Click **Submit**.


</td></tr><tr><td id="d475233e212">

**Edit an existing user criteria**

</td><td>

1.  Click **Edit**.
2.  On the Edit Members form, select the required roles, users, and groups from the Collection column and move them to the Not Available For List column by clicking the right arrow icon \(\[Omitted image "right-arrow-icon.png"\] Alt text: Right arrow icon.\).
3.  Click **Save**.


</td></tr></tbody>
</table>    **Note:** The Not Available For settings override the Available For settings. A user on the Not Available For list for an external link cannot access that external link, even if that user is also on the Available For list for that external link.


**Parent Topic:**[Create an external link](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/create-external-links.md)

