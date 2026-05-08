---
title: Configure how HR cases are created
description: Modify how search results for an employee appear and configure the default HR case creation form.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [case creation configuration]
breadcrumb: [HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure how HR cases are created

Modify how search results for an employee appear and configure the default HR case creation form.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

HR case creation has multiple steps:

-   Search for an employee or related case.
-   Create an initial HR case.
-   Complete the details of the case.

Using the **Case Creation Configuration** form you can control the information returned from a search and the required fields when creating an initial HR case.

**Note:** Zing text search is used to search on indexed fields in the User \[sys\_user\], HR Profile \[sn\_hr\_core\_profile\], and HR Case \[sn\_hr\_core\_case\] tables. Refer to Zing text indexing and search engine.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Case Creation Configuration**.

2.  On the form, modify the fields as appropriate.

<table id="table_hy3_vjw_bgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page size

</td><td>

Determines the maximum number of search results for each page break when using the **Search for Employee** form.**Note:** The default is 10. If there are more than 10 search results, the form divides the results into chunks of 10. It does not limit the search results to 10.

</td></tr><tr><td>

Minimum input length

</td><td>

Specifies the minimum number of characters that must be entered in the **Search for Employee** form to return results.

</td></tr></tbody>
</table>3.  Modify the default search behavior when searching by employee.

<table id="table_jcp_kkw_bgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display table

</td><td>

Displays employee information. Search uses the **HR Profile \[sn\_hr\_core\_profile\]** table when displaying information for an employee. This field is read-only.

</td></tr><tr><td>

Limit users on search

</td><td>

Option for adding filter conditions for searching for a user. For example, you could add a filter for only active users.

</td></tr><tr><td>

Additional display fields

</td><td>

Option for adding fields to help narrow a user search. The base system configuration provides fields for the user department, user employee number, and user location when applicable.

</td></tr><tr><td>

Links

</td><td>

A URL link configured in **Link Generator**. See [Link generator for HR Service Delivery](../concept/HRLinkGenerator.md).

</td></tr><tr><td>

User field

</td><td>

Read-only field that determines which users are displayed for a search the information displayed about them.

</td></tr><tr><td>

Force partial search

</td><td>

Option for providing the ability to enter a partial name to return search results. For example, when searching for Abraham Lincoln, users could enter `Abra` to return search results.

 Selecting this option also helps provide consistent search results when creating an HR case.

**Note:** If this option is not selected, users must enter the whole word to match.

</td></tr><tr><td>

Allow skipping verification

</td><td>

Option for providing the ability to enter or skip the employee name or case number when creating an HR case. For more information, see [Create an HR case](search-hr-case.md).For example, if your company receives a complaint from an external individual or an anonymous user, providing this option enables an HR agent to create a case without having to enter an employee name or case number.

</td></tr></tbody>
</table>4.  In the **Case Search** related list, modify the default search parameters when searching by case number.

    |Field|Description|
    |-----|-----------|
    |Case table|Read-only field that contains the **HR Case \[sn\_hr\_core\_case\]** table used for case search purposes.|
    |Limit cases on search|Option for adding filter conditions to your search. For example, you could add a filter to search only for active cases.|
    |User fields|Option for adding user fields to appear during a case search. The base system configuration provide fields for subject person, opened for, opened by, and watch list values when applicable.|

5.  In the **Employee Information** related list, modify the fields that appear in the **Employee Information** section of the **Case Creation** form.

    |Field|Description|
    |-----|-----------|
    |Left fields|Determines the fields that appear on the left side of the **Employee Information** section of the **Case Creation** form. The base system configuration displays fields for the user name and user employee number.|
    |Right fields|Determines the fields that appear on the right side of the **Employee Information** section of the **Case Creation** form. The base system configuration displays fields for the user email and user ZIP or postal code.|

6.  In the **Case Creation** related list, determine the default fields that appear in the **Case Creation** form.

<table id="table_k2w_llw_bgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task create table

</td><td>

Read-only field that contains the **HR Case \[sn\_hr\_core\_case\]** table used to show default case creation fields.

</td></tr><tr><td>

Limit services

</td><td>

Option for creating service conditions that determine the HR services that are available for specific employees. For example, you may not want to offer 401\(k\) benefits to employees outside of the United States.**Note:** HR services work with HR criteria to select the correct HR service for the subject person on the HR case. When a subject person is selected for an HR case, these fields determine the HR services available. When no subject person is selected, only services with no criteria are shown.

</td></tr><tr><td>

Fields minimum input length

</td><td>

Specifies the minimum number of characters that must be entered in a user search input field on the HR case creation form to return results.The value in this field affects searches in the following fields:

-   Subject person
-   Opened for
-   Opened by
-   Assigned to
-   Collaborators
-   Watch list
 A search request is not executed until the minimum number of characters are entered. A hint shows the minimum number of characters that must be entered to execute the search.

 The default value is 0. If the default value is used, a search is executed for each character entered.

**Note:** Placing a value in this field prevents a search from executing for every character entered that does not meet the minimum. The default value is 0

</td></tr><tr><td>

Left task fields

</td><td>

Determines the fields that appear on the Case Details Section \(CDS\). The base system provides the **COE** field, which is non-configurable.

</td></tr><tr><td>

Right task fields

</td><td>

Determines the fields that appear on the right side of the CDS. The base system configuration displays the **Opened for**, **Subject person**, and **HR service** fields.**Note:** Removing the **Subject person** field from the form or leaving it empty limits the HR services available to employees without associated HR criteria.

</td></tr><tr><td>

Bottom task fields

</td><td>

Determines the fields that appear on the bottom of the CDS. The base system configuration displays the **Work notes** field.

</td></tr></tbody>
</table>7.  In the **Case Creation Service Configurations** section, configure the HR case creation form for individual HR services.

    For more information, see [Configure the HR case creation form for an HR service](configure-case-creation-form-for-hr-service.md).

8.  Save your modifications.

    -   To save the modifications and remain on the form, click **Save**.
    -   To save the modifications and exit from the form, click **Update**.

**Parent Topic:**[HR Administration](../concept/c_AdministerHRServiceManagement.md)

