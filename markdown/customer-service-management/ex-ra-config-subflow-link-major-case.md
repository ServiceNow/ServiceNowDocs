---
title: Configuring a subflow for the guidance action automation
description: Configure a subflow that you can use in a guidance to automatically link the proposed major case to the current case on a click of an action button.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example: Link the similar major case to the current case, Example configurations, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configuring a subflow for the guidance action automation

Configure a subflow that you can use in a guidance to automatically link the proposed major case to the current case on a click of an action button.

Configure and publish a subflow with the following inputs and action. For more information, see Create a subflow in Workflow Studio.

<table id="table_wxq_2dr_pzb"><thead><tr><th>

Field

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

Link major case

</td><td>

-

</td></tr><tr><td>

**Subflow Inputs &amp; Outputs** &gt; **Inputs**

</td><td>

-   Current case
-   Major case

</td><td>

Input type: Reference

</td></tr><tr><td>

**Actions**

</td><td>

Update Record

</td><td>

Update case record action to add the major case as the parent case to the current case.

</td></tr></tbody>
</table>![Subflow action that is configured to add the major case as a parent case to the current case.](../image/ex-ra-similar-major-case-subflow.png)

