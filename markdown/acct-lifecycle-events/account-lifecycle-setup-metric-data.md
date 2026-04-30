---
title: Setup the data context engine
description: Define and measure metrics to calculate the health score or generate risk signals for one or more engagements.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure customer success, Customer success, Customer Success Management]
---

# Setup the data context engine

Define and measure metrics to calculate the health score or generate risk signals for one or more engagements.

Data is collected either from performance indicators or external sources as defined in the data source and is used to calculate the health score, generate risk signals, or create success outcomes. The following diagram shows the high level data model.

![Data context engine flow](../image/account-lifecycle-data-context-engine.png)

To collect and use the data, you must setup the data source to specify whether data is being collected from PA indicators or external sources. In the context table, you must associate the data source with an engagement or success outcome table. Based on the context, you must specify the record in the context table for which this data is applicable. Data is stored in the Context Engine Data table and when the scheduled jobs are run, the heath score, risk signals, and success outcomes are updated.

To setup the data context engine, follow these steps:

-   [Define the data source](account-lifecycle-define-data-source.md)
-   [Set up the context engine mapper](account-lifecycle-define-context-engine-mapper.md)

After the data context engine has been set up, you can configure the health and risk definitions:

-   [Setup the engagement health definition](../task/account-lifecycle-setup-health-defn.md)
-   [Setup the engagement risk definition](../task/account-lifecycle-setup-risk-defn.md)

