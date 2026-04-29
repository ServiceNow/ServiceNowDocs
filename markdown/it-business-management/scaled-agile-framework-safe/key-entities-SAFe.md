---
title: SAFe entities
description: Learn about the various SAFe entities that are used to successfully plan, track, and deliver your software products.
locale: en-US
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe entities

Learn about the various SAFe entities that are used to successfully plan, track, and deliver your software products.

-   **Epic**

    Epic in SAFe is the largest unit of work, which can be continuously worked through multiple program increments. Epic captures business hypotheses and is prioritized and assessed using the WSJF \(Weighted Shortest Job First is used to prioritize and sequence jobs to produce optimum business value\) score.

    An epic is further decomposed into features for implementation and delivery by SAFe ARTs.

-   **Feature**

    A SAFe feature is equivalent to an epic in Agile Development. It must be small enough for completion within a program increment cycle. It is prioritized and sequenced in an ART backlog based on its global ranking. A feature is further decomposed into user stories for implementation and delivery by SAFe teams.

-   **Story**

    A SAFe story is a brief statement encapsulating a product requirement or business case written in user-centric language. A story must be small enough for completion in one sprint. The estimated effort required to complete a story is measured in story points. More points are assigned to a story requiring more effort. Story points are arbitrary measurements of the effort \(not necessarily the time\) required to complete a story, based on the estimates from the SAFe team members.

-   **Agile Release Train**

    Agile Release Train \(ART\) comprises a set of teams working towards a single solution.

-   **Program Increment**

    A program increment is set period during which teams in an ART collaborate and produce to achieve agreed-upon goals. A program increment in SAFe is similar to a sprint in Agile Development, typically spanning 8–12 weeks. The most common form of program increment comprises four development sprints followed by one innovation and planning sprint.

-   **SAFe team**

    SAFe team is an autonomous, cross-functional team containing members possessing different skill-sets who work in collaboration to achieve a common goal.

    A user with the safe\_scrum\_master or safe\_art\_user role can create a SAFe team. You can assign these teams to SAFe work items such as stories, epics, and features.

    Once a SAFe team is created, you can add members to it.

    -   New customers: System administrator can add members to the team.
    -   Existing customers: A user with the safe\_scrum\_master or safe\_art\_user role can add members to your SAFe team.

        **Note:**

        You can restrict this function just to the system administrator by creating the **safe.disallow\_scrum\_add\_group\_member** property and setting it to **true**.

        For information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

-   **Sprint**

    Program Increments in SAFe are further segmented into sprints for teams involved in it, and are measured in terms of weeks.


-   **[Define an epic in SAFe](../task/create-SAFeepic.md)**  
Create an epic within SAFe. An epic is the largest unit of work that has one common objective such customer request, or business requirement. An epic is further decomposed into features for implementation and delivery by SAFe agile release trains \(ARTs\).
-   **[Define a feature in SAFe](../task/create-SAFefeature.md)**  
Create a feature in SAFe and break it down into smaller user stories for implementation and delivery by SAFe teams.
-   **[Define a story in SAFe](../task/create-SAFestory.md)**  
Create high-level definitions of your requirements in the form of stories in SAFe.
-   **[Define an Agile Release Train](../task/create-SAFeprogram.md)**  
From SAFe, define an Agile Release Train \(ART\) which is a group of agile teams working towards a single solution.
-   **[Define a program increment in SAFe](../task/create-SAFeprogramincrement.md)**  
With SAFe, define a program increment \(PI\). A program increment is typically 8–12 weeks long, during which an ART delivers incremental value in the form of working, tested software and systems.
-   **[Define a SAFe team](../task/create-SAFeteams.md)**  
From SAFe, create an agile team and associate it to an ART.

**Parent Topic:**[Essential SAFe](essential-overview.md)

**Related topics**  


[Components installed with Essential SAFe](../reference/installed-with-EssentialSAFe.md)

[Quick start tests for Essential SAFe](../../../administer/atf-quick-start-tests/reference/quick-start-tests-essentialSAFe.md)

[SAFe PI objectives](safe-pi-objectives.md)

[SAFe Board — ART level](program-level-tabs.md)

[SAFe Board — Team level](team-level-tabs.md)

