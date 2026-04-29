---
title: Activate or deactivate a component
description: Activate or deactivate a component to show or hide every instance of the components across third-party websites. By default, the ServiceNow components are active.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Update or create web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Activate or deactivate a component

Activate or deactivate a component to show or hide every instance of the components across third-party websites. By default, the ServiceNow components are active.

## Before you begin

Role required: sn\_embeddable\_core.emb\_admin

## Procedure

1.  Navigate to **All** &gt; **Web Embeddables** &gt; **Homepage**.

2.  In the Manage components section, select Action \(⋮\) on the component.

3.  Select **Activate**.

    **Note:** A confirmation dialog box appears. Review the information before proceeding. If your component is active, the **Deactivate** option appears.

4.  Select **Activate** on the confirmation modal.

    **Note:**

    -   A confirmation message appears `Component is now active and its existing instances may become visible on your websites.` Ensure the \[glide.uxf.lib.embeddables.enabled\] system property is set to true on your instance.
    -   If you deactivate a component, a confirmation message appears `Component is now inactive and its existing instances are hidden on your websites.`

## Result

Any existing component and its instances are hidden on your website.

