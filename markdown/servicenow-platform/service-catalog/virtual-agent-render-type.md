---
title: Catalog item render types
description: A render type determines how a catalog item's form can be rendered to requesters. For example, in Virtual Agent a catalog item can be rendered as a conversation, window, or pop-up.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist in Conversational Catalog Request, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog item render types

A render type determines how a catalog item's form can be rendered to requesters. For example, in Virtual Agent a catalog item can be rendered as a conversation, window, or pop-up.

## Catalog item request using Conversational-agentic render type

The Conversational-agentic render type uses agentic AI to let users submit catalog item requests using a guided and natural language chat that means through conversations. Rather than showing all ﬁelds at once, a Now Assist collects user information step by step.

## Catalog item request using Web render type

TheWeb render type is the default and most widely used rendering mode for catalog items. When a catalog item is set to this render type, its request form is rendered as a standard web page inside a portal or the Now Platform UI.

## Catalog item request using a conversation render type

A user can submit a request in the conversation mode \(by answering the questions in line\) in Virtual Agent.

![Virtual Agent rendered as a conversation](../image/va-conversation-catalog.png)

## Catalog item request using a pop-up render type

A user can submit a catalog item request as a pop-up for items, which are not conversational. In a pop-up, Virtual Agent provides a link for the user to submit the request in a pop-up without navigating to a new tab. A non-conversational catalog item can be rendered as a pop-up only if it does not have any Custom, Custom with label, or UI Page variables.

**Note:** If you do not want to render your Virtual Agent conversation as a pop-up, set the **glide.sc.va.render\_type.legacy** property to true, which renders all non-conversational catalog items in the configured portal in a new tab.

![Virtual Agent rendered as a pop-up](../image/va-popup-catalog.png)

## Catalog item request using a window render type

A user can submit a catalog item request in a window. In a window, Virtual Agent provides a link for the user to submit the request in the Service Portal defined in the **sn\_itsm\_va.com.snc.itsm.virtualagent.portal\_url** property. A non-conversational item is rendered as a window if it has a Custom, Custom with label, or UI Page variable.

A catalog item is rendered as a window if it is of the following types:

-   Content Item
-   Order Guide
-   Wizard Launcher
-   Standard Change Template

![Virtual Agent rendered as a window](../image/va-window-catalog.png)

**Parent Topic:**[Now Assist in Conversational Catalog Request](now-assist-in-conversational-catalog-request.md)

