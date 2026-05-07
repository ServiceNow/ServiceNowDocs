---
title: Session and configuration timeouts
description: Learn how timeouts for inactive or abandoned configurations improve system efficiency and prevent resource waste.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Session and configuration timeouts

Learn how timeouts for inactive or abandoned configurations improve system efficiency and prevent resource waste.

Because CPQ is a web-based application, we regulate our software usage by implementing certain timeouts on sessions, so as to not waste processing power on abandoned configurations.

Timeouts for the CPQ platform have two key mechanisms:

-   Session timeout: Set at 30 minutes of user inactivity.

    This applies to any end user or Admin interaction. When configuring a product or editing a rule, if nothing has been updated on any tab in this time, the session times out.

-   Configuration cache timeout: 15 minutes if abandoned \(browser closed or navigated away\)

    This cache can stay active for up to 2 hours. As long as the configuration UI remains open and is being updated, or the user has multiple browser tabs that they are configuring in, the cache will be maintained.


Here are a few example scenarios.

-   Scenario 1: If an end user is configuring, or if an Admin is creating a rule and stays on that tab, but does not update the site, the session will time out after 30 minutes.
-   Scenario 2: If a user calls a runtime API to configure a product, the 15-minute configuration cache timeout applies to make PATCH updates to the configuration, as there is no automatic heartbeat for this method.
-   Scenario 3: If an end user is actively configuring a product, that configuration session can remain active for up to 2 hours.
-   Scenario 4: If a user navigates to a different tab while in the middle of configuring, that configuration can still remain active for up to 2 hours as long as the user is still actively working with another configuration in CPQ.

    **Note:** While this behavior works well in CPQ, we cannot guarantee the same functionality in Salesforce iframe tabs. SFDC may not allow JavaScript to run on inactive tabs, potentially affecting the 2-hour timeout in that environment.

-   Scenario 5: If the CPQ configurator is in an SFDC iframe and the user navigates to a different tab, the 15-minute cache expiry for inactive sessions may occur.

The most effective approach to avoid a timeout is to manually save your configurations, especially when working across multiple tabs. This way, progress is not lost when completing other work.

**Parent Topic:**[CPQ reference](../reference/servicenow-cpq-reference.md)

