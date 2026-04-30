---
title: Configure Now Assist data overflow processing
description: Configure where Now Assist data is processed during periods of high traffic.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure general Now Assist settings, Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Configure Now Assist data overflow processing

Configure where Now Assist data is processed during periods of high traffic.

## Before you begin

Role required: sn\_generative\_ai.data\_steward

## About this task

By default, Now Assist data is handled in ServiceNow datacenters. During periods of high network traffic, data can be "burst" to Microsoft Azure datacenters to help keep consistent load times and avoid capacity overflow errors. Users with the data steward role can opt out of or into this behavior from the Now Assist Admin console.

Data processing is not supported in regulated markets.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  In the navigation pane, go to **Data sharing and processing** &gt; **Now overflow processing**.

3.  Select either **Opt out** or **Opt in**.

    Instances are opted in by default. You can change this setting at any time.


**Parent Topic:**[Configure general Now Assist settings](configure-now-assist-admin-settings.md)

