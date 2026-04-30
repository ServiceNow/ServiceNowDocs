---
title: Overall technique mitigation coverage calculator
description: The overall technique mitigation coverage is determined based on the formula defined in the mitigation coverage calculator.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Map your mitigation coverage to a technique, MITRE-ATT&amp;CK administration, MITRE-ATT&amp;CK framework overview, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Overall technique mitigation coverage calculator

The overall technique mitigation coverage is determined based on the formula defined in the mitigation coverage calculator.

## Before you begin

-   Role required: sn\_ti.admin, sn\_si.admin: create, write, delete access
-   Role required: sn\_ti.read: read access

## About this task

-   You can set to active only one mitigation coverage calculator per domain.
-   The base system mitigation coverage calculator is an average calculator.
-   Any customizations to the calculator script should ensure that the final output is a numeric value between 0 through 100.
-   The mitigation coverage definition is applied based on the range of the final output.

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **MITRE ATT&amp;CK Administration** &gt; **Mitigation Coverage Calculator**.

    The following illustration shows the default mitigation coverage calculator.![The illustration shows the default mitigation calculator.](../image/mitre-mitigation-calculator.gif)


**Parent Topic:**[Map your mitigation coverage to a technique](map-your-mitigation-coverage-to-a-technique.md)

