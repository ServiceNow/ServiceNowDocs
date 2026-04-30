---
title: Process Mining release notes
description: The ServiceNow Process Mining application enables analysts and process owners to view their business processes, analyze them, and make decisions that improve their processes. Process Mining was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Process Mining release notes

The ServiceNow® Process Mining application enables analysts and process owners to view their business processes, analyze them, and make decisions that improve their processes. Process Mining was enhanced and updated in the Yokohama release.

## Process Mining highlights for the Yokohama release

-   Now Assist based work notes analysis
-   Process configuration builder introduced
-   Content pack importer introduced for process configurations
-   Process Mining evaluation project available for HR and CSM
-   Access control \(ACL\) rules updated

See [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

**Important:** Process Mining is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Now Assist based work notes analysis](https://www.servicenow.com/docs/access?context=worknotes-analysis&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Work notes analysis is now enhanced using Now Assist to understand the operational reasons behind activity transitions by examining the work notes and comments recorded around the time of these transitions.

-   **[Process configuration builder introduced](https://www.servicenow.com/docs/access?context=create-process-config&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Configure and view the process configurations efficiently by using the new comprehensive Process configuration builder. It is a guided setup to configure and view the process configurations.

-   **[Content pack importer introduced for process configurations](https://www.servicenow.com/docs/access?context=po-content-pack&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Import and customize the content pack process configuration templates to activate new features. Content pack process configuration templates are now read-only.

-   **[Process Mining evaluation project available for HR and CSM](https://www.servicenow.com/docs/access?context=evaluation-pm-inci-manag&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Ability to try out the sample mining and limited features available for HR and CSM without an entitlement. For the advanced features, you can purchase a license.

-   **[Access control \(ACL\) rules updated](https://www.servicenow.com/docs/access?context=access-control&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    The ACL rules have been updated for broader visibility on the try-out version while also increasing the security.

    -   No Process Mining role is required to access a shared project and to generate Platform Analytics insights for some tables.
    -   Some breakdown filters or activity definitions are blocked for certain users based on the column access.
-   **[Process Mining performance improved](https://www.servicenow.com/docs/access?context=analyst-workbench-overview&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    The following improvements boost Process Mining performance and lead to quicker insights:

    -   Introduced lazy loading of improvement opportunities and variants for faster workspace loading.
    -   Introduced applying a transition filter before mining to reduce scope of data and speed up the mining process.
    -   Improved Process Mining workbench load time.
-   **[Transition filters enhanced](https://www.servicenow.com/docs/access?context=node-to-node-conditions&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    The enhanced transition filters now provide more flexibility and precision in filtering the process map by providing the following:

    -   Ability to use `OR` clause on steps to create a more complex and nuanced criteria for process transitions.
    -   Include predicates like "is empty" and "is not empty" allowing for more refined control over the conditions under which transitions occur, ensuring that workflows are both comprehensive and adaptable to a variety of scenarios.
    -   Ability to select more than one value with a single click that contains a specific text.
-   **[Enhanced the Process Mining engine](https://www.servicenow.com/docs/access?context=set-activity-def&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Key updates include:

    -   Defining integer fields as activity definitions.
    -   Grouping journal fields to identify how quickly an agent reacted to an assigned case.
    -   Defining the order of simultaneous activities on the graph.
-   **[Addition﻿al breakdown capacity for Process Mining on external data](https://www.servicenow.com/docs/access?context=external-dataset&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Ability to import a maximum of 10 breakdown fields enabling to segment and analyze specific subsets of the external process data using Process Mining.

-   **[API for accessing Process Mining data](https://www.servicenow.com/docs/access?context=define-workflow-model&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Create, mine, and access Process Mining data via an API \(ProcessMiningIntegrationAPI\). For more information, see the API documentation.


## UI changes

-   **[Usability improvements introduced](https://www.servicenow.com/docs/access?context=explore-process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    A few improvements are introduced for ease of usability.

    -   View the improvement opportunities on the Summary and Insights page as a card view or list view.
    -   Rename the scheduled tasks that help to identify and view a specific result.

## Activation information

Process Mining is available with activation of the sn\_po plugin. For details, see [Activating Process Mining](https://www.servicenow.com/docs/access?context=activating-process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Platform Analytics experience provides a single center for consuming the data from all Platform Analytics products. Use Process Mining with Platform Analytics insights to optimize your indicator data sources.


**Parent Topic:**[Platform Analytics release notes](../analytics-intelligence-reporting/analytics-intel-report-rn-landing.md)

