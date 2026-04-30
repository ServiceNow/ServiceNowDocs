---
title: Self-Service Analytics concepts
description: You can quantify your self-service effectiveness by measuring case deflections.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Self-Service Analytics, Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Self-Service Analytics concepts

You can quantify your self-service effectiveness by measuring case deflections.

The Self-Service Analytics framework enables you to measure case deflection by defining user activity patterns for a deflection outcome. A case deflection is when you are able to provide a resolution using one of the self-service channels, such as Knowledge, Communities, Catalog, and Virtual Agent, to a user who intended to create a case and as a result, no case is created.

By default, the Self-Service Analytics framework is used by the Self-Service Analytics dashboard for customer service. The framework can also be used in dashboards of other applications that use the Subscriptions and Activity Feed Framework.

The system includes predefined configurations for the Self-Service Analytics framework components associated with consumers and customer contacts. You can also configure these components for other user entities.

## Self-service analytics components

Self-service analytics is based on the activity pattern associated with a deflection outcome. It consists of the following main components:

-   Activity pattern \(see [Activity pattern components](ssa-concepts.md#section_a22_kcl_rlb)\)
-   Deflection outcome \(see [Deflection outcome components](ssa-concepts.md#section_k4v_l52_tlb)\)

## Activity pattern components

-   **Activity pattern**

    A combination of pattern element, pattern element group, or both for a user entity such as consumers or customer contacts that is linked to an outcome. Each pattern element or pattern element group is implemented as regular expressions.

    Example: The activity pattern Contacts: Case: Confirmed Deflection is a combination of pattern element groups Self-Service: Helpful and Self-service actions: Optionally Many.

-   **Deflection outcome**

    An activity pattern can lead to a deflection outcome. See [Deflection outcome components](ssa-concepts.md#section_k4v_l52_tlb).

-   **Primary activity**

    The final activity that determines the outcome associated with an activity pattern based on whether it happens or not.

    Example: For the primary activity Customer created a case if the system does not find a match \(that is a case was not created\), the outcome Confirmed deflection is associated with the activity pattern Contacts: Case: Confirmed Deflection.

-   **Pattern element group**

    A logical combination of two pattern elements, pattern element group, or both and how many times the combination occurs. For more information, see [Pattern element group components](ssa-concepts.md#section_wkt_bq2_tlb).


The following figure illustrates the components of the activity pattern Contacts: Case: Confirmed Deflection.

![Components of the activity pattern Contacts: Case: Confirmed Deflection](../image/activity-pattern.png)

## Pattern element group components

-   **Pattern element group**

    A logical combination of two pattern elements, pattern element group, or both and how many times the combination occurs. Each pattern element group is implemented as regular expressions.

    The occurrence of the logical combination result is one of the following types:

    -   Once
    -   Optionally Once
    -   Optionally Many
    -   At Least Once
    -   Range
    Example 1: In the following table, the Knowledge engagements once pattern element group is true when it occurs only once and either Article viewed once is true or Article marked with positive feedback once is true.

    |Pattern element group|First Element|Second Element​|Operator|Occurrence​|
    |---------------------|-------------|---------------|--------|-----------|
    |Knowledge engagements once|Article viewed once|Article marked with positive feedback once|Or|Once​|

    Example 2: In the following table, the Self-service engagements optionally many pattern group is true when engagements either have not occurred or have occurred multiple times and either the Knowledge or catalog engagements once is true or the Communities or virtual agent engagements once is true.

    |Pattern element group|First Element|Second Element​|Operator|Occurrence​|
    |---------------------|-------------|---------------|--------|-----------|
    |Knowledge or catalog engagements once|Knowledge engagements once|Catalog engagements once|Or|Once|
    |Communities or virtual agent engagements once|Communities once|Virtual agent engagements once|Or|Once|
    |Self-service engagements optionally many|Knowledge or catalog engagements once|Communities or virtual agent engagements once|Or|Optionally Many|

-   **Pattern element**

    Denotes a single activity type and how many times it occurs. Each pattern element is implemented as regular expressions.

    Example: The pattern element Article viewed once denotes that the activity Viewed a knowledge article must occur once.

-   **Activity type**

    An action that a user \(consumer or customer contact\) performs.

    Example: The activity type Viewed knowledge article occurs when a user views a knowledge article.


The following figure illustrates the components of the pattern element group Knowledge engagements once.

![Components of the pattern element group Article content actions](../image/pattern-element.png)

## Activity context components

-   **Activity context**

    A collection of activity groups a user might perform such as Catalog, Knowledge, Case, Communities, and Virtual Agent.

    Example: The activity context Contact is a collection of activity groups Catalog, Knowledge, Case, Communities, and Virtual Agent associated with the customer contact.

-   **Activity group**

    A logical grouping of activity types performed on the same object type such as a knowledge article, community answer, or customer service case.

    Example: The activity group Knowledge is a logical grouping of the activities Viewed knowledge article and Marked the article helpful performed on a knowledge article.

-   **Activity context group**

    An activity group that has been added to a context.


The following figure illustrates the components of the activity context Contact.

![Components of the activity context Contact.](../image/activity-context.png)

## Deflection outcome components

-   **Deflection outcome**

    In the context of deflection, an activity pattern can lead to one of the following three outcomes:

    -   **Confirmed deflection**

        The self-service content definitely prevented a case from getting created.

    -   **Potential deflection**

        The self-service content was viewed and no case was created, but it's unclear whether the content is the factor that prevented the case from getting created.

    -   **No deflection**

        A case was created after the self-service content was viewed.

-   **Deflection configuration**

    Associates a window \(duration\) with an activity context. The window defines how long a system will wait for a case to be created to match with a deflection pattern.

    Example: To track the create case activity for a consumer within a day, set the window as 1 day.

    -   If the consumer created a case within that window, the deflection pattern matched is a No deflection.
    -   If the consumer did not create a case within that window, the deflection pattern matched is a Potential deflection.
    -   If the consumer did not create a case and the last activity is submitted positive feedback for any self-service channel content within that window, the deflection pattern matched is a Confirmed deflection.
-   **Deflection metrics**

    A transactional table that stores the outcome of matched patterns. By default, the scheduled job for Self-Service Analytics captures data and stores the generated data in the Deflection Metric \[ssa\_deflection\_metric\] table.

-   **Deflection pattern**

    Associates deflection configuration with an activity pattern. A deflection pattern is implemented as a table.


**Parent Topic:**[Self-Service Analytics](self-service-analytics.md)

**Related topics**  


[Configure Self-Service Analytics](../task/config-ssa.md)

