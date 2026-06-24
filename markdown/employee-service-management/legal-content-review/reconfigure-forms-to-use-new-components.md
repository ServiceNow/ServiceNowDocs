---
title: Reconfigure forms to use new components
description: As an administrator, after installing Legal Content Review reconfigure forms to use the new content review record producer, catalog category, and content taxonomy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-content-review/reconfigure-forms-to-use-new-components.html
release: australia
product: Legal Content Review
classification: legal-content-review
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Legal Content Review, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Reconfigure forms to use new components

As an administrator, after installing Legal Content Review reconfigure forms to use the new content review record producer, catalog category, and content taxonomy.

## Before you begin

Role required: admin

## About this task

The content review request, that was part of Legal Request Management, has been moved to a new application Legal Content Review. With the new application, new content review components are available for Legal Content Review. You can reconfigure the intake forms to use the new content review record producer, catalog category, and content taxonomy depending on the following points.

-   If you use the new content review components, you must redo any customizations you made to the previous forms.
-   The previous content review components won’t be enhanced for new functionalities.

## Procedure

1.  Reconfigure the **Intake Form Content Review**.

    1.  In the navigation filter, enter `sn_lg_ops_category.list`.

    2.  From the list, select Legal Content Review.

    3.  In the **Request record producer** field, select the Lookup using list icon \(\[Omitted image "lookup-using-list.png"\] Alt text: Lookup using list icon\)

    4.  If you aren’t able to edit the form in the current application scope, select the word **here** in the message at the top of the page.

    5.  In the record producers list, select the Show/hide filter icon \(\[Omitted image "LSD-filter-icon.png"\] Alt text: Show/hide filter icon\).

    6.  In the **choose field** field, select **Application**.

    7.  In the condition field, select **is** if it is not displayed.

    8.  Enter Legal Content Review in the text box.

    9.  Select the **Run** button.

    10. Select **Content Review** from the list of record producers that belong to the Legal Content Review application.

    11. Select **Update**.

2.  Reconfigure the catalog item for Catalog item categories.

    1.  In the navigation filter, enter `sc_cat_item_category.list`.

    2.  In the Catalog item categories list, locate **Content Review** and select the Preview this record icon \(\[Omitted image "icon-global-search.png"\] Alt text: Preview this record icon\).

    3.  Select **Open Record**.

    4.  In the **Catalog item** field, select the Lookup using list icon \(\[Omitted image "lookup-using-list.png"\] Alt text: Lookup using list icon\).

        If you are unable to edit the record, select **here** in the access message at the top of the form.

    5.  In the catalog items list, select the show/hide filter icon \(\[Omitted image "LSD-filter-icon.png"\] Alt text: Show/hide filter icon\).

    6.  In the **choose field** field, select **Application**.

    7.  In the condition field, select **is** if it is not already displayed.

    8.  Enter `Legal Content Review` in the text box.

    9.  Select the **Run** button.

    10. Select **Content Review** from the list of catalog items that belong to the Legal Content Review application.

    11. Select **Update**.

3.  Reconfigure the catalog item for Connected Content.

    1.  In the navigation filter, enter `m2m_connected_content.list`.

        The Connected Content Catalog Item: Content Review form is displayed.

    2.  In the **Catalog item** field, select the Lookup using list icon \(\[Omitted image "lookup-using-list.png"\] Alt text: Lookup using list icon\).

    3.  In the catalog items list, select the show/hide filter icon \(\[Omitted image "LSD-filter-icon.png"\] Alt text: Show/hide filter icon\).

    4.  In the **choose field** field, select **Application**.

    5.  In the condition field, select **is** if it is not displayed.

    6.  Enter Legal Content Review in the text box.

    7.  Select the **Run** button.

    8.  Select **Content Review** from the list of record producers that belong to the Legal Content Review application.

    9.  Select **Update**.


**Parent Topic:**[Configure Legal Content Review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-content-review/setting-up-legal-content-review.md)

