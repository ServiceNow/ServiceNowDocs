---
title: Extension points in Telecommunications Customer 360
description: Use scripted extension points to configure the display of the cards on the Telecommunications Customer 360 consumer page.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-22"
reading_time_minutes: 2
breadcrumb: [Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Extension points in Telecommunications Customer 360

Use scripted extension points to configure the display of the cards on the Telecommunications Customer 360 consumer page.

To access the available extension points, type `sys_extension_point.list` in the application navigator and select **Enter**. You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is executed.

|Extension point|Description|
|---------------|-----------|
|sn\_telecom\_c360.ContactCardDataProvider|Control the data displayed on the Contact card for an account, consumer, or contact record. You can customize which fields appear, override the card title and avatar logic, or change how the editable state is determined.|
|sn\_telecom\_c360.InsightCardDataProvider|Control the configuration for the Customer insight card and shows AI-generated insights. You can customize which Now Assist skill configuration is used and whether insights are triggered automatically when the card loads.|
|sn\_telecom\_c360.DataVisualizationDataProvider|Define which reports appear on the Data visualization card and how context record values are mapped to report filters. You can add custom filter logic or support filter types not handled by the default implementation.|
|sn\_telecom\_c360.BillingsDataProvider|Customize how billing accounts and invoices are retrieved for the Billings card. You can change how billing accounts are linked to the context record, add custom invoice filtering or sorting logic, or adjust how invoice amounts and statuses are displayed.|
|sn\_telecom\_c360.ProductsServicesDataProvider|Customize how the Products &amp; services card retrieves product inventory data, applies filters, and creates change orders. You can add support for different product tables, change how filter options are built, or modify the change order creation logic.|
|sn\_telecom\_c360.AllTasksDataProvider|Customize which task tables appear on the All tasks card and what actions are available in the card header. You can add or remove task tables, apply custom filters, or change the create action configuration.|
|sn\_telecom\_c360.ProductsRelatedDataProvider|Add custom pill types to individual product rows on the Products &amp; Services card. Each implementation provides data for one type of related record \(such as cases or incidents\) linked to a sold product.|
|sn\_telecom\_c360.CardViewModel|Control whether a specific card is visible on the Customer 360 workspace. Implement isMatch to identify which card your view model applies to, and implement isVisible to define the conditions under which that card should be shown. By default, any card with no matching view model is visible.|
|sn\_telecom\_c360.VoiceInteractionDataProvider|Control the behavior of the Customer 360 record page when it is opened as a sub page from a voice interaction. Implement the provided methods to customize whether the consumer lookup alternate flow is enabled, and which cards or layout columns are hidden in the voice interaction sub page context.|

**Related topics**  


[bundle-crapiref.extension-points]

[bundle-crapiref.scripted-extension-points]

[bundle-crapiref.ui-extension-points]

[bundle-crapiref.client-extension-points]

