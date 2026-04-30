---
title: Parent and child security incident relationships
description: You can associate and track the impact of any given issue using parent and child security incident relationships in Security Incident Response.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View information in a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Parent and child security incident relationships

You can associate and track the impact of any given issue using parent and child security incident relationships in Security Incident Response.

Using the **Related Records** tab, you can add a **Parent security incident** issue to any Security Incident Response form. This feature automatically makes the incident a child that appears in the **Related Lists - Child Security Incidents** tab of the parent issue.

**Note:** You cannot make an existing parent security incident its own child by using the same number for both incidents.

![Adding a Parent security incident](../image/SI_Parent2Child.png)

![Viewing a Child security incident](../image/SI_Childview.png "Child Security Incident")

You can add one or more **Child Security Incidents** to any security incident record, as well, using the **Edit** button in the **Child Security Incidents** tab. In the following example, all three records are connected.

![Viewing the grandparent, parent, and child security incidents](../image/SI_Parent-Child_Grandparent.png "Grandparent, Parent, and Child security incidents")

Note:

-   All work notes recorded in the parent are propagated to any active children in **Activities** under the **Incident Details** tab.
-   The **Parent** field is used to associate the security incident with a parent record, such as a major incident, problem, or change request, that is outside the Security Incident module. For grouping multiple security incidents to a main security incident, the **Parent security incident** field is used.

When a parent is closed or canceled, any active children are also closed or canceled. Any active **Response Tasks** on the child incidents are canceled. If there are no other open **Tasks**, the child incident is closed. When closed, the **Post Incident Interview** records the closure and the information found on the **Closure Information** tab is propagated from the parent to the children.

![Child response task closed and post incident review updated](../image/ChildResponseTaskClosed.png "Close Child Response task")

