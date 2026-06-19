---
title: Create a custom clone profile
description: Clone profiles act as reusable clone templates to establish consistent clone outcomes. Clone profiles enable you to set up exclusions, preservers, and cleanup scripts for specific clone scenarios.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/configure-clone-profile.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-09-30"
reading_time_minutes: 1
breadcrumb: [Configure, Instance Clone, Configure core features, Administer]
---

# Create a custom clone profile

Clone profiles act as reusable clone templates to establish consistent clone outcomes. Clone profiles enable you to set up exclusions, preservers, and cleanup scripts for specific clone scenarios.

## Before you begin

Role required: clone\_admin

Here are a few basics about clone profiles:

-   Clone profiles can be duplicated via the clone admin console when opening any clone profile.
-   The system profile is provided by default and can't be changed. If you leave the clone profile field empty when requesting a clone, the system uses the excluded tables, data preservers, and cleanup scripts configured under the [Definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/clone-exclusions-preservers-cleanupscripts.md) tab.
-   Exclusions and preservers that are listed under the system profile are automatically added to all other clone profiles the user creates.
-   You can choose to prepare different profiles for individual use cases. For example, a different profile for upgrades, dev testing, IT app testing, HR app testing and so on.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Home**.

2.  Navigate to **Configurations** &gt; **Clone Profiles**

3.  Select **New**.

4.  Fill in the new clone profile form.

    For field information, see [Clone options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/clone-options.md).


