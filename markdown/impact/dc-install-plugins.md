---
title: Install Impact Value Management Data Collection Content Pack Apps dependent plugins
description: Install the dependent plugins for Impact Value Management Data Collection Content Pack apps
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Install Impact Value Management Data Collection Content Pack Apps dependent plugins

Install the dependent plugins for Impact Value Management Data Collection Content Pack apps

## Before you begin

Role required: admin

-   Install the ServiceNow Impact store application in your ServiceNow instance before you enable Value Management data collection apps plugins.
-   Install at least one dependency plugin to enable data collection jobs in Impact value management data collection apps. The only exception is Strategic Portfolio Management, which requires both dependency plugins to be installed to enable data collection functionality.

## Procedure

1.  Navigate to **System Definitions** &gt; **Plugins**.

2.  Search for the plugins that are required for the respective content pack installation.

3.  Ensure that all dependent plugins are installed before activating the Data Collection content pack jobs.

    The following dependent plugins must be installed to support the functionality of Data Collection apps:

<table id="choicetable_jpr_lyl_k2c"><thead><tr><th align="left" id="d45176e99">

Data Collection Content Pack

</th><th align="left" id="d45176e102">

Dependent plugins

</th></tr></thead><tbody><tr><td id="d45176e108">

**IT Operations Management \(ITOM\)**

</td><td>

Event Management Core \(sn\_em\_ai\)

</td></tr><tr><td id="d45176e117">

**HR Service Delivery \(HRSD\)

**

</td><td>

Human Resources Scoped App: Core \(com.sn\_hr\_core\)

</td></tr><tr><td id="d45176e129">

**Strategic Portfolio Management \(SPM\)

**

</td><td>

-   PPM Standard \(com.snc.financial\_planning\_pmo\)
-   Goal Framework \(sn\_gf\)


</td></tr><tr><td id="d45176e150">

**Application Portfolio Management \(APM\)**

</td><td>

Enterprise Architecture \(com.snc.apm\)

</td></tr><tr><td id="d45176e160">

**App Engine**

</td><td>

App Engine Studio \(sn\_app\_eng\_studio\)

</td></tr><tr><td id="d45176e169">

**Customer Service \(CSM\)**

</td><td>

Customer Service Management\(com.sn\_customerservice\)

</td></tr><tr><td id="d45176e178">

**Security Operations \(SecOps\)

**

</td><td>

-   Security Incident Response Dependencies \(Id: com.snc.si\_dep\)
-   Vulnerability Response Dependencies \(Id: com.snc.vul\_dep\)
-   Security Incident Response \(sn\_si\)
-   Vulnerability Response \(sn\_vul\)


</td></tr><tr><td id="d45176e205">

**Hardware Asset Management \(HAM\)**

</td><td>

Hardware Asset Management \(sn\_hamp\)

</td></tr><tr><td id="d45176e214">

**Software Asset Management \(SAM\)

**

</td><td>

-   Major Incident Management plugin\(com.snc.incident.mim\)
-   SaaS License Management plugin \(com.sn\_sam\_saas\_int\)


</td></tr><tr><td id="d45176e235">

**Integrated Risk Management \(IRM\)

**

</td><td>

-   GRC: Policy and Compliance Management \(sn\_compliance\)
-   GRC: Advanced Risk \(sn\_risk\_advanced\)
-   ServiceNow Audit \(sn\_audit\)
-   ServiceNow risk assessment \(sn\_risk\_assessment\)


</td></tr></tbody>
</table>
