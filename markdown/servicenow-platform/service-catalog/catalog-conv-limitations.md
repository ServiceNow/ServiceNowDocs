---
title: What makes catalog items non-conversational in premium chat
description: Let's understand what determines whether a catalog item can deliver a fully conversational experience in the Premium Chat interface.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-04-30"
reading_time_minutes: 2
breadcrumb: [Conversational catalog request reference, Now Assist in Conversational Catalog Request, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# What makes catalog items non-conversational in premium chat

Let's understand what determines whether a catalog item can deliver a fully conversational experience in the Premium Chat interface.

Premium chat is a conversational interface powered by Now Assist. Instead of filling out a traditional form, requesters can request catalog items through conversations. For a catalog item to work in this mode, it needs to meet certain conditions.

-   Conversation turned off using the **turn\_off\_nowassist\_conversation** property, preventing the item from appearing in Premium chat mode, regardless of how the item is designed.
-   The catalog item has been flagged to open as a form and not a chat using the **make\_item\_non\_conversational** property. This is used for complex items where a structured form is preferred over a guided conversation.
-   When a catalog item has more than the configured maximum number of questions \(Using the **sn\_now\_assist\_cr.og.question\_threshold** property, which has a default value as 4\), it can be complex to handle as a natural back-and-forth conversation.
-   Catalog items use client-side scripts that change the form dynamically as the user fills it in. For example, hiding certain fields based on earlier answers, or running a calculation. These scripts only work in a traditional browser form and can't be replicated inside a chat window, so the item can't be made conversational while these scripts are active.
-   Similar to scripts, UI policies are rules that change what requesters see on the form based on their inputs. Because these rules depend on the form rendering in a browser, they aren't compatible with the step-by-step chat approach.
-   Every field on the catalog item is either hidden from the user, pre-filled with a default value, or set to read-only. Since there are no questions left, there is nothing for a conversational experience to do.
-   Some questions types, such as check box, Custom, Render UI Page, Custom with Label, Lookup Select Box, List Collector, Lookup Multiple Choice, Masked, Table Question, Requested For, Attachment Question, Table Name aren't supported.
-   Some fields let users pick a value from a list \(for example, choosing a specific laptop model from a catalog\). Items with this kind of advanced filtering fall back to the traditional form.
-   If any question on the catalog item influences the cost or pricing of what is being requested, the item can't be handled conversationally. Pricing implications aren't yet supported in the chat interface.
-   Some catalog items include a section where the user can add multiple rows of information. For example, ordering accessories for several employees at once. This kind of repeating, table-style input is not yet supported in a Premium chat interface.
-   Certain catalog item types, such as order guides, wizard, content items, or standard change templates, have a structure that is more complex than a simple request. These types are not eligible for the conversational experience and open as a traditional form.

**Note:**

-   Conversational catalog items that don't support agentic AI may be discoverable, but they don't appear within conversation in the Premium chat experience. These catalog items open as forms that requesters can fill out and submit.
-   Meeting these requirements doesn't require rebuilding a catalog item from scratch. Often, small adjustments, such as reducing the number of visible questions, removing an unused client script, or switching a field type, are enough to make an item eligible for the full agentic AI experience.

**Parent Topic:**[Conversational catalog request reference](../reference/conversational-catalog-request-reference.md)

