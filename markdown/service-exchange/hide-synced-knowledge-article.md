---
title: Hide a synced knowledge article
description: Hide a knowledge article that was synced to the target instance through Foundation Data Sync \(FDS\) so that it's no longer visible to other users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/hide-synced-knowledge-article.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [knowledge articles, Foundation Data Sync, FDS, hide articles]
breadcrumb: [Configure inbound FDS as consumers, Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Hide a synced knowledge article

Hide a knowledge article that was synced to the target instance through Foundation Data Sync \(FDS\) so that it's no longer visible to other users.

## Before you begin

The knowledge article must be synced to your instance through FDS.

Role required: admin

## About this task

Knowledge articles synced from a source instance aren't owned by the target instance, so actions like Retire and Checkout don't apply to them. Use **Hide** to prevent other users from seeing a synced article, without affecting the article on the source instance. You can unhide the article at any time.

Hiding a knowledge article adds the existing **Any user** user criteria to the article's **Cannot Read** field. Unhiding removes it. When **Cannot Read** and **Can Read** both apply to the same user, **Cannot Read** takes priority.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Knowledge Articles**.

2.  Modify the filter to view the list of knowledge articles.

3.  Open the synced knowledge article you want to hide.

    Articles created directly on the instance don't show the **Hide** action.

4.  Select **Hide**.


## Result

The article is no longer visible to other users. The action changes to **Unhide** so you can restore visibility later. If the source instance sends an updated version of the article, the hidden state is preserved. Any additional access restrictions the source sends are added rather than replacing your hidden setting.

**Related topics**  


[Knowledge article sync via FDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/service-exchange/knowledge-base-assignment.md)

