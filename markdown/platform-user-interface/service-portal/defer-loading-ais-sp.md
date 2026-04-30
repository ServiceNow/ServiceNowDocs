---
title: Deferred loading of AI Search assets in Service Portal
description: Deferred loading of AI Search on the Service Portal delays the loading of certain AI Search assets until the main page content is loaded. This delay helps the page to load faster, thus improving user experience in the portal. st.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure widget loading order in Service Portal, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Deferred loading of AI Search assets in Service Portal

Deferred loading of AI Search on the Service Portal delays the loading of certain AI Search assets until the main page content is loaded. This delay helps the page to load faster, thus improving user experience in the portal. st.

A new system property, **glide.service\_portal.ais\_defer\_load\_enable.list**, has been added to control for which portals deferred loading is applied. This property accepts a comma-separated list of portal url\_suffix values. By default, deferred loading is enabled for the Service Portal.

**Note:** If the web embeddable feature is enabled, loading of the AI Search assets can’t be deferred. Instead, they load along with the other widgets on the portal page.

**Parent Topic:**[Configure widget loading order in Service Portal](configure-widget-loading-order.md)

