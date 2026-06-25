---
title: Reconfigure forms to use new components
description: As an administrator, after installing Legal Simple Privacy reconfigure forms to use the new privacy assessment record producer, catalog category, and content taxonomy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-simple-privacy/reconfigure-post-install-privacy.html
release: australia
product: Legal Simple Privacy
classification: legal-simple-privacy
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Legal Simple Privacy, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Reconfigure forms to use new components

As an administrator, after installing Legal Simple Privacy reconfigure forms to use the new privacy assessment record producer, catalog category, and content taxonomy.

## Before you begin

Role required: admin

## About this task

The privacy assessment legal request that was part of Legal Request Management has been moved to a new application Legal Simple Privacy. With the new application, new privacy assessment components are available for Legal Simple Privacy. You can reconfigure the intake forms to use the new privacy assessment record producer, catalog category, and content taxonomy depending on the following points.

-   If you use the new privacy assessment components, you must redo any customizations you made to the previous forms.
-   The previous privacy assessment components won’t be enhanced for new functionalities.

## Procedure

1.  Reconfigure the **Intake Form Privacy Assessment**.

    1.  In the navigation filter, enter `sn_lg_ops_category.list`.

    2.  From the list, select **Privacy Assessment**

    3.  In the **Request record producer** field, select the Lookup using list icon \(\[Omitted image "lookup-using-list.png"\] Alt text: Lookup using list icon\)

    4.  If you aren’t able to edit the form in the current application scope, select the word **here** in the message at the top of the page.

    5.  In the record producers list, select the Show/hide filter icon \(\[Omitted image "LSD-filter-icon.png"\] Alt text: Show/hide filter icon\).

    6.  In the **choose field** field, select **Application**.

    7.  In the condition field, select **is** if it is not displayed.

    8.  Enter Legal Simple Privacy in the text box.

    9.  Select the **Run** button.

    10. Select **Privacy Assessment** from the list of record producers that belong to the Legal Simple Privacy application.

    11. Select **Update**.

2.  Reconfigure the catalog item for Catalog item categories.

    1.  In the navigation filter, enter `sc_cat_item_category.list`.

    2.  In the Catalog item categories list, locate **Privacy Assessment** and select the Preview this record icon \(\[Omitted image "icon-global-search.png"\] Alt text: Preview this record icon\).

    3.  Select **Open Record**.

    4.  In the **Catalog item** field, select the Lookup using list icon \(\[Omitted image "lookup-using-list.png"\] Alt text: Lookup using list icon\).

        If you are unable to edit the record, select **here** in the access message at the top of the form.

    5.  In the catalog items list, select the show/hide filter icon \(\[Omitted image "LSD-filter-icon.png"\] Alt text: Show/hide filter icon\).

    6.  In the **choose field** field, select **Application**.

    7.  In the condition field, select **is** if it is not already displayed.

    8.  Enter `Legal Simple Privacy` in the text box.

    9.  Select the **Run** button.

    10. Select **Privacy Assessment** from the list of catalog items that belong to the Legal Simple Privacy application.

    11. Select **Update**.

3.  Reconfigure the catalog item for Connected Content.

    1.  In the navigation filter, enter `m2m_connected_content.list`.

        The Connected Content Catalog Item: Privacy Assessment form is displayed.

    2.  In the **Catalog item** field, select the Lookup using list icon \(\[Omitted image "lookup-using-list.png"\] Alt text: Lookup using list icon\).

    3.  In the catalog items list, select the show/hide filter icon \(\[Omitted image "LSD-filter-icon.png"\] Alt text: Show/hide filter icon\).

    4.  In the **choose field** field, select **Application**.

    5.  In the condition field, select **is** if it is not displayed.

    6.  Enter Legal Simple Privacy in the text box.

    7.  Select the **Run** button.

    8.  Select **Privacy Assessment** from the list of record producers that belong to the Legal Simple Privacy application.

    9.  Select **Update**.


**Parent Topic:**[Configure Legal Simple Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-simple-privacy/setting-up-legal-simple-privacy.md)

**Related topics**  


[Install Legal Simple Privacy]()

