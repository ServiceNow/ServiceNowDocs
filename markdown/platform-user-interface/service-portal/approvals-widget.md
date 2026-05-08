---
title: Approvals widget
description: Users can approve or reject items directly within Service Portal. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Approvals widget

Users can approve or reject items directly within Service Portal. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

## Using the widget

The Approvals widget displays data from the Approvals \[sysapproval\_approver\] table. If the user has been assigned to approve a request, the approval record is displayed in the widget.

![Approvals widget](../image/WidgetApprovals.png)

You can enable e-signature for the approvals widget to require reauthentication for your users. For more information on enabling e-signature, see [Enable e-signature for Service Portal](../task/enable-esignature-sp.md#).

## Instance options

Use the instance options to change the appearance of the approvals widget.

|Field|Description|
|-----|-----------|
|Bootstrap color|Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.|
|Glyph|Add an icon to display beside the widget name.|
|Buttons stacked side by side|If this check box is selected, the Approve and Reject buttons appear horizontally beside each other. If this check box is cleared, the Approve and Reject buttons appear stacked vertically.|
|Max number of elements shown in the list|Limit the number of approvals users see on a page. The default number is 10. Only enter numbers greater than 0.|
|Who can view instances/who cannot view instances|Control who can or can’t view a widget instance with [user criteria](user-criteria.md). User criteria must be enabled for this option to appear.|
|Comments mandatory for rejection|Require approvers to provide comments when rejecting an approval. The comments are added to the Approval record. By default, providing comments is optional.|

**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

