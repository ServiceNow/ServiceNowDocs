---
title: Control what happens on a click
description: Since a CMS system uses multiple pages you have to tell the system which page to use to display drill through content.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMS gauge support, Content types, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Control what happens on a click

Since a CMS system uses multiple pages you have to tell the system which page to use to display drill through content.

In the normal \(non CMS\) system, when you click a bar in a bar chart or a wedge on a pie chart, you drill through and your current screen is replaced with a list of records meeting the chart's criteria. For example, if you have a gauge of **Incidents by Category** and you click the bar labeled **Hardware** you drill through to a list of all incidents with a category=hardware.

Within the CMS system, there is a similar drill through mechanism at work, but you must manually specify which page to display.

There are two different models of the drill through, use an in-place target frame to receive the content, or use another page to display the content.

## Using an In-Place Target

An in-place target is a named iframe on the same CMS page as the gauge. When the gauge is clicked, the drill-through content appears within that iframe rather than changing out the CMS page. The gauge \(and the rest of the page other than the target\) remain in place and active.

## Using a Gauge Target Page

A gauge target page is a separate CMS page that is used to display the drill-through content from a gauge. When a gauge is clicked, the current CMS page is replaced with the gauge target page and the drill-through content is rendered within that second page.

-   **Gauge Target Page**

    To set a site default, select **Gauge Target Page**, on the site configuration page. This page is used as the drill-through target for any gauges in the system that do not have a more specific gauge page specified in their content type.

-   **Gauge Page**

    To set a content-type specific page, you can specify a **Gauge Page**, on a content type page. Any gauges for this type of content then use that page for any drill through.

    **Note:** The gauge target on a particular content type overrides the default, site level, gauge target.

-   **Gauge Target block**

    A gauge target page is a normal CMS page, with one special requirement. Somewhere on that page, there must be a **Gauge Target block**. This market block tells the system where to output the drill through data.


**Parent Topic:**[CMS gauge support](../concept/c_CMSGaugeSupport.md)

**Related topics**  


[CMS gauge support](../concept/c_CMSGaugeSupport.md)

[Put a gauge on a CMS page](../task/t_PutAGaugeOnACMSPage.md)

