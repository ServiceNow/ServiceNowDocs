---
title: Configure widget loading order in Service Portal
description: Configure service portal pages to defer load the widgets on a page. The delay in loading of non-essential widgets helps to improve page loading speed and optimizes the use of resources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/configure-widget-loading-order.html
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configure widget loading order in Service Portal

Configure service portal pages to defer load the widgets on a page. The delay in loading of non-essential widgets helps to improve page loading speed and optimizes the use of resources.

## Before you begin

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  In **Service Portal Designer**, select a page.

4.  On the page, hover over the widget that you want to defer load.

5.  Select the **Form** icon\[Omitted image "Form\_icon.png"\] Alt text: Form icon to open a new form.

6.  Select the **Select the check box to defer load this widget** check box.

7.  Complete the fields in the form.

<table id="table_otc_4nx_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

In which order do you want to load the widget?

</td><td>

Select **Viewport** if you want the widget to load when it appears in the page view. Select **Parallel** to have the widget load after the page loads.

</td></tr><tr><td>

Device type

</td><td>

Select the type of device \(desktop, tablet, and mobile\) on which you want to defer load widgets.

</td></tr><tr><td>

Advance placeholder configuration

</td><td>

Select the check box to dynamically define the height and width of the widget.

</td></tr><tr><td>

Placeholder dimensions

</td><td>

Specify the height and width of the widget in each of the selected device types with the following code:```

{
  "mobile": {
  "height": "100%",  
  "width": "100%"
  },
  "desktop": {
  "height": "100px",
  "width": "100%"
  },
  "tablet": {
  "height": "100%",
  "width": "100%"
  }
}


```

</td></tr><tr><td>

Limit widget size to placeholder

</td><td>

Select the check box to retain the original placeholder dimensions and avoid layout shifts.

</td></tr><tr><td>

Placeholder Template

</td><td>

Define the custom skeleton loader. A default code is already available and can be edited for customization.

</td></tr></tbody>
</table>8.  Select **Save**.


## Result

Deferred loading of the widget is enabled.

-   **[Deferred loading of AI Search assets in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/defer-loading-ais-sp.md)**  
Deferred loading of AI Search on the Service Portal delays the loading of certain AI Search assets until the main page content is loaded. This delay helps the page to load faster, thus improving user experience in the portal. st.

**Parent Topic:**[Using portal widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/service-portal-widgets.md)

