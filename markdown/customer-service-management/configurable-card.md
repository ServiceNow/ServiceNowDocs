---
title: Configurable Cards feature configuration
description: The Configurable Cards feature enables you to add and customize the features in Engagement Messenger that aren’t available by default.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Engagement Messenger reference, Reference, Customer Service Management]
---

# Configurable Cards feature configuration

The Configurable Cards feature enables you to add and customize the features in Engagement Messenger that aren’t available by default.

<table id="table_opq_wb1_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choose how to display the card

</td><td>

The type of display for the feature card on the messenger's home page. The available options are:-   **Use an image in a card**: Shows a feature card as a clickable image.
-   **Use a title and subtitle in a card**: Shows a title and subtitle text as a display feature card

</td></tr><tr><td>

Image

</td><td>

An image that appears as a feature card on the messenger's home page and has a portal or catalog link embedded in it.The requirements for using images are:

-   Supported formats are .jpg, .png, .bmp, and .gif.
-   Dimensions are a minimum of 120x370px and a maximum of 250x370px.

 **Note:** This field appears only when **Use an image in a card** is selected from the **Choose how to display the card** field.

</td></tr><tr><td>

Use a title and subtitle in a card

</td><td>

-   **Title text:** Title of the feature widget in the messenger.
-   **Subtitle text**: Description for the feature widget in the messenger.

 **Note:** This field appears only when **Use a title and subtitle in a card** is selected from the **Choose how to display the card** field.

</td></tr><tr><td>

Page type

</td><td>

The type of page that opens when the feature card is clicked. -   **Catalog Item**: The catalog item that opens within the messenger when the user clicks on the feature card.
-   **Portal Page**: The portal page that opens within the messenger when the user clicks on the feature card. You can configure additional parameters to load specific content from the portal page. For more information about embedding portal pages on Engagement Messenger, see [Requirements for embedding portal pages in Engagement Messenger](https://community.servicenow.com/community?id=community_article&sys_id=9a1b08a91be30114a59033f2cd4bcbc4).

</td></tr><tr><td>

Enable for unauthenticated users

</td><td>

Option for enabling this feature for guest users who visit the website that hosts the messenger.

</td></tr><tr><td>

Enable for authenticated users

</td><td>

Option for enabling this feature for users who sign in to the website that hosts the messenger.

</td></tr><tr><td colspan="2">

**Note:** Engagement Messenger honors access permissions defined for the portal page or catalog item. If the users do not have access, the feature card will not appear on the messenger.

</td></tr></tbody>
</table>![Configurable cards displaying a list of features you can customize. In this example, the portal page displays an image as a card on the Engagement Messenger home page.](../image/em-config-card-portal-image.png "Use an image in a card")

![Configurable cards displaying a list of features you can customize. In this example, the portal page displays a title and subtitle as a card on the Engagement Messenger home page.](../image/em-config-portal-title-subtitle.png "Use title and subtitle in a card")

<table id="table_bds_3xm_wsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title text

</td><td>

Title of the feature card in the messenger.

</td></tr><tr><td>

Show an image for each link

</td><td>

Option to display an image along with a link on the messenger's home page.

</td></tr><tr><td>

Add up to five links

</td><td>

Displays external website links on the messenger’s home page.**Note:** You can add a maximum of five links.

</td></tr><tr><td>

Enable for unauthenticated users

</td><td>

Option for enabling this feature for guest users who visit the website that hosts the messenger.

</td></tr><tr><td>

Enable for authenticated users

</td><td>

Option for enabling this feature for users who sign in to the website that hosts the messenger.

</td></tr></tbody>
</table>![Configurable cards displaying a list of features you can customize. In this example, embedded links are added to the Engagement Messenger home page.](../image/em-config-cards-links.png "Featured links")

<table id="table_jnv_wxm_wsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choose a way to display records

</td><td>

Determines the appearance of records on the messenger.-   **Each record displays as a link**: Shows a title and list of records from the selected table on the messenger's home page. It displays up to five records on the messenger home screen.
-   **Each record displays as a card**: Shows a feature card through which users can access data from the selected table.

</td></tr><tr><td>

Enable for unauthenticated users

</td><td>

Option for enabling this feature for guest users who visit the website that hosts the messenger.

</td></tr><tr><td>

Enable for authenticated users

</td><td>

Option for enabling this feature for users who sign in to the website that hosts the messenger.

</td></tr><tr><td class="sub-head" colspan="2">

Homepage

</td></tr><tr><td>

Title text

</td><td>

Title of the feature card displayed in the messenger.

</td></tr><tr><td>

Subtitle text

</td><td>

Description for the feature card displayed in the messenger.

</td></tr><tr><td class="sub-head" colspan="2">

Display of records

</td></tr><tr><td>

Choose table

</td><td>

Determines the table that the card displays records from, either on your ServiceNow instance or from a remote third-party source.

</td></tr><tr><td>

Number of records to show

</td><td>

The total records to be shown as links on the messenger's home page. The maximum value is five. **Note:** This field is applicable only when **Each record displays as a link** is selected from the **Choose a way to display records** field.

</td></tr><tr><td>

Page title

</td><td>

Title of the messenger page that appears when a custom feature card is clicked.

**Note:** This field is applicable only when **Each record displays as a card** is selected from the **Choose a way to display records** field.

</td></tr><tr><td>

Display field

</td><td>

The field from the selected table that you want to use as the primary display field.

</td></tr><tr><td>

Details field

</td><td>

The fields to display on the card that represent your data. You can select up to four detail fields. **Note:** Applicable only when **Each record displays as a card** is selected from the **Choose a way to display records** field.

</td></tr><tr><td>

Portal page to open

</td><td>

The portal page to display when the user selects any link or card.

</td></tr><tr><td>

Condition for records

</td><td>

Condition that restricts the records that appear in a list in the messenger.

</td></tr><tr><td colspan="2">

**Note:** Engagement Messenger honors Access Control rules \(ACLs\) defined for any tables in your ServiceNow instance. If users don’t have access, the feature card doesn't appear on the messenger.

</td></tr></tbody>
</table>![Configurable cards displaying a list of features you can customize. In this example, you can use multiple form fields to create and show record as link using Mobile phones card.](../image/em-config-cards-data-table-1.png "Record displays as a link")

![Configurable cards displaying a list of features you can customize. In this example, you can use multiple form fields to create and show record as card using Mobile phones card.](../image/em-config-cards-data-table-2.png "Record displays as a card")

