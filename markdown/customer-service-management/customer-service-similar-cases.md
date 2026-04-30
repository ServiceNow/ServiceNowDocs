---
title: Similar case recommendations
description: The similar case recommendation feature enables customer service agents to easily find similar cases that can provide helpful information about a current case. This feature can also provide recommendations about cases that may be related to major issues.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Similar case recommendations

The similar case recommendation feature enables customer service agents to easily find similar cases that can provide helpful information about a current case. This feature can also provide recommendations about cases that may be related to major issues.

The similar case recommendation feature uses the following components:

-   **Additional search resources for contextual search**

    Additional search resources are provided for contextual search. These additional resources enable customer service agents to search open or resolved cases for information related to the current case.

-   **Predictive Intelligence similarity solution definitions**

    Several of the additional search resources have an associated Machine Learning \(ML\) similarity solution definition. These additional resources perform a contextual search based on the case short description and return a list of similar records.

-   **Predictive Intelligence in Agent Workspace**

    Predictive Intelligence can provide agents with a list of cases that are similar to the current case. These similar cases may provide helpful details or resolution information for the current case. Predictive Intelligence can also provide recommendations about potential major issues and major cases.


With the similar case/recommendation feature, customer service agents can:

-   Find cases that are similar to the current case.
-   Copy resolution notes and codes from resolved cases to the current case.
-   Link the current case to a similar case.
-   View a list of open cases similar to the current case and submit the current case as a major case candidate.
-   View one or more similar major cases and link the current case as a child to a major case.

Major issue managers can search for cases that are similar to a major case and add them as child cases.

## Using the feature in Agent Workspace and in the platform interface

With Agent Workspace, agents can:

-   Perform a search in Predictive Intelligence using the additional search resources.
-   Create a link from the current case to a selected case in the search results.
-   Copy resolution information from a selected case to the current case. This includes the resolution code and the resolution notes \(the agent must then save the case\).
-   View a list of similar cases that do not include major cases. This is a way to see that the current case might be a major case candidate.
-   View a list of similar cases that include one or more major cases. The major cases are displayed first in the list of results. Agents can use an available action to add the current case as a child of a major case.

With the platform interface, agents can:

-   Perform a search in the Related Search Results section on the Case form using the additional search resources. Agents can select these additional resources from a list by the **Related Search** field.
-   Create a link from the current case to a selected case in the search results.

## Plugins

The configuration for the similar case/recommendation feature is included with the Customer Service plugin \(com.sn\_customerservice\).

The similar case/recommendation feature has a dependency on the Contextual Search plugin \(com.snc.contextual\_search\). Activate the Contextual Search plugin to use contextual search and the additional search resources.

To use similar case/recommendation with the following features, activate the associated plugins:

-   Major Issue Management – activate the Major Issue Management plugin \(com.sn\_majorissue\_mgt\)
-   Predictive Intelligence – activate the Predictive Intelligence plugin \(com.glide.platform\_ml\)
-   Problem Management – activate the Problem Management Best Practice – Madrid – State Model \(com.snc.best\_practice.problem.madrid.state\_model\)

**Related topics**  


[Machine learning solutions for Customer Service Management](machine-learning-csm.md)

