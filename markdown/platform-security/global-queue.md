---
title: Global queue v.2
description: The global queue concept provides a single virtual view of tasks that reside in multiple instances. The concept creates a custom application to provide a fulfiller view of work that resides in multiple instances without having to replicate tasks or data.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Concepts for service providers, Exploring domain separation, Domain separation for service providers, Access Management]
---

# Global queue v.2

The global queue concept provides a single virtual view of tasks that reside in multiple instances. The concept creates a custom application to provide a fulfiller view of work that resides in multiple instances without having to replicate tasks or data.

## Overview

![Global queue](../image/global-queue.png)

Service Providers with agents working on tasks from multiple systems tend to integrate the data back to a central instance, or a “swivel chair” between instances. While this method might be appropriate in some cases, it can be expensive and time-consuming to build and maintain. This method also opens the provider up to potential auditing and data requirement considerations such as General Data Protection Regulation \(GDPR\) in all of the instances where the data now lives.

Global queue v.2 is an alternative: With this method, agents can see data assigned to them from a single instance without sovereign data persisting on the instance they are logged into. For example, in cases where clients have data residency requirements, but allow access by agents from other countries, the provider could use a “follow-the-sun” Help Desk using global queue v.2.

Learn more about the [Global Queue v.2 Proof of Concept](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0960364) on the ServiceNow Knowledge site.

**Note:** In the Quebec release forward, the Global Queue Proof of Concept has been upgraded to Global Queue v. 2.

**Parent Topic:**[Concepts for service providers](sp-concepts.md)

