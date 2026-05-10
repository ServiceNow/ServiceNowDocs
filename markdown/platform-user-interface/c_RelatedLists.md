---
title: Related lists
description: Related lists appear on forms and show records in tables that have relationships to the current record.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Related lists

Related lists appear on forms and show records in tables that have relationships to the current record.

Users can view and modify information in related lists like any other list. Administrators can configure related lists to appear on forms and in hierarchical lists by [configuring a form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md). Related lists do not have a size limit.

**Note:**

Creating a record using a related list applies the list filter to the record and auto-populates the related field. This behavior applies to reference, string, Boolean, and menu fields when the criteria in the filter is set to **is** or **=**.

-   **[Select or create records in a related list](../task/t_SelectRelatedRecords.md)**  
When a form contains a related list, such as the **Incidents** related list in the problem form, you can select existing records or add new ones in the related list.
-   **[Configure when a related list loads](../task/t_ConfigureWhenARelatedListLoads.md)**  
If there are many related lists on a form or many records in the related lists, the form may load slowly. You can improve form response times by configuring related lists to load manually, on demand, or automatically, after the rest of the form loads.
-   **[Create a default filter for a related list](../task/t_CreateADefaultFilter.md)**  
Create a default filter for the records that load when your related list displays.
-   **[Configure the edit option](../task/t_ConfigureTheEditOption.md)**  
You can configure the edit option that allows users to add records to related lists in forms.
-   **[Create defined related lists](../../../administer/form-administration/task/t_CreateDefinedRelatedLists.md)**  
You can add default related lists to the form for all users to see when viewing records.
-   **[Add fields to selections in a related list](../../../administer/form-administration/task/t_AddingFieldsToARelatedList.md)**  
When you click **Edit** in a related list and select an item, information about the item appears below the list. You can expand the fields that appear for the item to provide more information.
-   **[Create a default filter for list selector records](../../../administer/form-administration/task/t_CreateDefaultRelatedRecSecFilter.md)**  
You can set a default filter to restrict which related records users can select when editing a reference field. Default filters are simple to set up but lack a dynamic filtering element, which prevents the end user from changing the default filter.

**Parent Topic:**[Forms in the classic environment](c_UsingForms.md)

**Related topics**  


[Configure form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-form-layout.md)

[Lists in the classic environment](../../using-lists/concept/c_UseLists.md)

