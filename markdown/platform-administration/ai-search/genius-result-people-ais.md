---
title: People Genius Results
description: People Genius Results display top search results from the User \[sys\_user\] table. Each People Genius Result answer card shows a single user record. You can view the user's full profile directly from the answer card.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Genius Result configurations in the base system, Genius Results, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# People Genius Results

People Genius Results display top search results from the User \[sys\_user\] table. Each People Genius Result answer card shows a single user record. You can view the user's full profile directly from the answer card.

![People answer card for Beth Anglin with View profile action link.](../image/genius-result-people.png "Sample People Genius Result answer card")

Select **View profile** to see the user's profile.

People Genius Results only support English searches.

The People Genius Result configuration is inactive in the base system. To learn how to activate it, see [Activate People Genius Results](../task/activate-people-genius-results-ais.md).

**Warning:** Don't activate the People Genius Result configuration if your instance has more than 100,000 records in any of the following tables:

-   Catalog Item \[sc\_cat\_item\]
-   Department \[cmn\_department\]
-   Location \[cmn\_location\]
-   User \[sys\_user\]

These tables are configured as vocabulary sources in the Default AI Search Genius Results Model specified in the People configuration's NLU trigger condition. If your instance has more than 100,000 records in any of the listed tables, training will fail for the NLU model and the People Genius Result configuration won't operate correctly.

-   **[Activate People Genius Results](../task/activate-people-genius-results-ais.md)**  
Enable AI Search's People default Genius Result configuration for use in your search profiles.

**Parent Topic:**[Genius Result configurations in the base system](default-genius-result-configs-ais.md)

