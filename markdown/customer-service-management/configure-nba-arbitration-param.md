---
title: Configure the arbitration parameters in Recommended Actions
description: Configure the recommended actions by the frequency of issues or by the order of priority so that your agents get the guidance that they must help resolve customer issues.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configure the arbitration parameters in Recommended Actions

Configure the recommended actions by the frequency of issues or by the order of priority so that your agents get the guidance that they must help resolve customer issues.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author

## About this task

A mathematical formula determines the priority of the recommended actions that are displayed to the agents. For most cases, you should use the default values to ensure that the relevant recommended actions are available for a given context. If you want to alter the frequencies, you can modify the values.

The recommended actions in the New state appear by ranking. For example, the score for these actions is calculated by the order of frequency and the priority order of the rule.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Arbitration Configuration**.

2.  On the Arbitration Configuration form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Rule Order Weight \(sn\_nb\_action.rule\_order\_weight\)|Weight given to an action based on the priority of the rule that recommends it. The default value is 0.9.|
    |Recommendation Order Weight \(sn\_nb\_action.recommendation\_order\_weight\)|Weight given to an action based on the priority of the rule that recommends it. The default value is 0.9.|
    |Frequency Weight \(sn\_nb\_action.frequency\_weight\)|Weight applied based on the number of times an action is recommended across rules. The default value is 1.5.|

3.  Select **Save**.


