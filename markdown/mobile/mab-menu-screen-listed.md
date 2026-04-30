---
title: Menu options in the categories home screen
description: Familiarize yourself with the various menu options in the Mobile App Builder categories home page.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile App Builder categories home screen, Mobile App Builder, Mobile app building tools, Building mobile apps, Mobile Platform]
---

# Menu options in the categories home screen

Familiarize yourself with the various menu options in the Mobile App Builder categories home page.

-   **Mobile app configs**

    The Mobile app configs category is the configuration option for ServiceNow applications on iOS and Android mobile devices. Select an option to personalize the app theme, set user access permissions, and create a navigation bar. You must select one configuration per app type. This category is based on the \[sys\_sg\_native\_client\] table.

    **Note:** You can open an existing Mobile Onboarding app configured from a previous release. However, you cannot create a new Mobile Onboarding app configuration.

<table id="table_mdx_sqk_qqb"><tbody><tr><td>

Select the **New** button \(![New button in categories home screen.](../image/mab-buttton-new-green-solid.png)\) to create a new mobile app configuration.Alternatively, select the name of a listed mobile app configuration to open the defined records for that configuration, in the Mobile App Builder record screen.

</td><td>

![Create new mobile app configuration screen.](../image/mab-create-config.png)

</td></tr></tbody>
</table>-   **Screens**

    Screens are the essence of the mobile app experience, enabling you to deliver unique and customized capabilities to provide different user experiences. Screens have different configurable components according to the screen type you select. This category is based on the \[sys\_sg\_screens\] table.

<table id="table_pys_c1r_qqb"><tbody><tr><td>

Select the **New** button \(![New button in categories home screen.](../image/mab-buttton-new-green-solid.png)\) to select a screen type to configure a new mobile screen. Alternatively, select the name of a listed screen to open the records required for that configuration, in the Mobile App Builder record screen.

</td><td>

![Create new mobile screen.](../image/mab-screen-select.png)

</td></tr></tbody>
</table>-   **Cards &amp; icons**

    Cards consist of layouts that show visuals, text, and data. Icons are symbols that act as actions or shortcuts when connected to other screens. With both of these items, you can create rich, interactive mobile experiences. This category is based on the tables \[sys\_sg\_icon\], \[sys\_sg\_view\_config\], \[sys\_sg\_view\_template\], and \[sys\_sg\_item\_view\].

<table id="table_eqh_f1r_qqb"><tbody><tr><td>

Select the **New** button \(![New button in categories home screen.](../image/mab-buttton-new-green-solid.png)\) to select a card type to configure.Alternatively, select the name of a listed card, card template, icon, or legacy card to open the records required for that configuration, in the Mobile App Builder record screen.

 **Note:** You are able to open and edit an existing legacy card configured from a previous release. However, you cannot create a new legacy card.

</td><td>

![Create a new card or icon screen.](../image/mab-card-icon-select.png)

</td></tr></tbody>
</table>-   **Functions**

    Use functions to define which actions users can perform within the mobile app. This category is based on the \[sys\_sg\_button\] table.

    Select the **New** button \(![New button in categories home screen.](../image/mab-buttton-new-green-solid.png)\) to create a new function. Alternatively, select the name of a listed function type to open the records required for that configuration, in the Mobile App Builder record screen.

-   **Data**

    Data items provide the data presented in a screen. Select the table you want data from and define the conditions that must be met for the data to be displayed. This category is based on the \[sys\_sg\_data\_item\] table.

<table id="table_r1k_nbr_qqb"><tbody><tr><td>

Select the **new** button \(![New button in categories home screen.](../image/mab-buttton-new-green-solid.png)\) to select a data item type. Alternatively, select the name of a listed data item to open the records required for that configuration, in the Mobile App Builder record screen.

</td><td>

![Create a new data item screen.](../image/mab-create-data.png)

</td></tr></tbody>
</table>-   **All mobile records**

    Use the **All mobile records** category to quickly find records within specific tables without the need to drill down into multiple layers of the ServiceNow AI Platform configuration tree. For example, a filter record can be selected here instead of having to select a list screen record and then drill down to the filter record.

<table id="table_pz3_xbr_qqb"><tbody><tr><td>

Use the **Record type** field to search and select the table you require. The results display a list of records of the selected record type. Use the search box \(![Search option for category results.](../image/mab-search-in-category.png)\) to filter the records from the list.

</td><td>

![Mobile App Builder All mobile records category with the record type drop-down displayed.](../image/mab-all-mobile-records.png)

</td></tr></tbody>
</table>
