---
title: Monitor risks using GRC Performance Analytics Indicators
description: You can link Risk Management risk statement and risks to Performance Analytics indicators, breakdowns and thresholds. You can associate Performance Analytics indicators with risk statements, and risks to view scorecards and trends and analyze current conditions and trends.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Risk Management, Governance, Risk, and Compliance]
---

# Monitor risks using GRC Performance Analytics Indicators

You can link Risk Management risk statement and risks to Performance Analytics indicators, breakdowns and thresholds. You can associate Performance Analytics indicators with risk statements, and risks to view scorecards and trends and analyze current conditions and trends.

The risks and controls associated with a PA indicator or PA indicator/breakdown/element automatically monitor any PA threshold with the same PA indicator or PA indicator, breakdown, or element relationship. Any PA threshold breach is reported at the risk or control and Performance Analytics indicators relationship level within a breach counter.

## PA threshold breach impact

When a risk or control and Performance Analytics indicators relationship breach counter is different than zero \(for example, a PA threshold with the same PA indicator or PA indicator, breakdown, or element relationship has breached\), and if no opened issue exists, then an issue is created which is associated to the risk or control. Also for risks, the **Indicator failure factor** represents the number of risk and Performance Analytics indicators relationships with a breach counter different than zero.

## Reset all PA Indicator breach counters

Reset breach counters associated to a risk or control by clicking **Reset all PA Indicator breach counters** or opening the specific relationship and clicking **Reset Breach Counter**.

## GRC PA indicator breach reports

There are two reports for the reporting of breaches:

-   Risk PA Indicator Breaches
-   Control PA Indicator Breaches

-   **[Activate GRC: Performance Analytics Integration](../../grc-common/task/activate-grc-pa-prem-integ.md)**  
The GRC: Performance Analytics Integration plugin provides an integration between Performance Analytics and the Risk Management and Policy and Compliance Management applications. This plugin provides more insight into organizational risk and compliance performance.
-   **[Associate a PA indicator with a risk statement or control objective](../../grc-indicators/task/associate-pa-indicator-grc-content.md)**  
You can associate Performance Analytics indicators with risk statements and policy statements to analyze trends related to the risk or policy.
-   **[Associate a PA indicator with risks and controls](../../grc-indicators/task/associate-pa-indicator-grc-item.md)**  
You can associate Performance Analytics indicators with risks and controls to analyze trends related to the entity that risk or control belongs to.
-   **[Update associated GRC indicators for a set of items](../../grc-indicators/task/update-associted-indicators-set-of-items.md)**  
You can update all the items belonging to a GRC content record so each item is individually related to the PA indicator.

**Parent Topic:**[Using Risk Management](using-risk-mgmt.md)

