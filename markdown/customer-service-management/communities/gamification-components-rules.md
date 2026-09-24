---
title: Rules
description: Gamification rules allow you to configure points that users receive for activities on the community.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/gamification-components-rules.html
release: brazil
product: Communities
classification: communities
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Gamification components, Gamification, Using communities, Communities, Customer Service Management]
---

# Rules

Gamification rules allow you to configure points that users receive for activities on the community.

**Important:**

Starting with the Brazil release, Communities is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Gamification includes several pre-defined rules. The gamification administrator can use these rules, modify them as needed, or create new rules. These pre-defined rules include:

-   Comment marked as helpful: 5 points
-   Document marked as helpful: 5 points
-   Video marked as helpful: 5 points
-   Blog marked as helpful: 5 points
-   Answer marked as helpful: 20 points
-   Document bookmarked: 20 points
-   Blog bookmarked: 20 points
-   Video bookmarked: 20 points
-   Answer marked correct for a question: 40 points

When a user performs an activity that has a gamification rule, the user profile identified in the rule receives points. Points received through a gamification rule can be configured to accumulate toward:

-   Overall points across the entire community
-   Points in forums associated with the activity
-   Points in topics associated with the activity
-   Points in a track
-   Points assigned for a combination of forums, topics, and tracks

If users revert previous activities, the points associated with these activities are removed. As an example, if a rule has been defined and a user creates a blog, they are awarded points. The points are deducted when the blog is deleted. If a rule has not been defined and a user creates a blog, no points are awarded. If the user removes it once a rule has been defined, points are deducted even though none were awarded in the first place.

**Parent Topic:**[Gamification components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/gamification-components.md)

**Related topics**  


[Create a gamification rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/gamification-create-rule.md)

