---
title: Using Now Assist for CMDB
description: If you have the sn\_cmdb\_user role, you can access several Now Assist for CMDB skills, agents, and agentic workflows.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-09-09"
reading_time_minutes: 5
---

# Using Now Assist for CMDB

If you have the sn\_cmdb\_user role, you can access several Now Assist for CMDB skills, agents, and agentic workflows.

## Agentic workflows used by Now Assist for CMDB

-   **Create configuration item**

    Occasionally, you might need to create a CI manually. To help you, the workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks IRE policies to determine the required attributes for the CI and request that information. After you provide sufficient data, the workflow uses IRE to ensure that the proposed CI is not a duplicate, and then creates the Cl. For more information, see [CI creator agentic workflow](../../now-assist-cmdb/concept/na-cmdb-awf-ci-creator.md).

-   **Provide advice on CMDB governance**

    Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to ensure that users can trust the data that they use for their work. For more information, see [CMDB governance agentic workflow](../../now-assist-cmdb/concept/na-cmdb-awf-governance.md).

-   **Search CMDB**

    The CMDB search agentic workflow enables you to search for CI data by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table search, depending on the information you provide. The workflow can infer CI relationship data to generate an appropriate query. For more information, see [CMDB search agentic workflow](../../now-assist-cmdb/concept/na-cmdb-awf-search.md).


## AI agents used by Now Assist for CMDB

-   **CI creator AI agent**

    The CI creator AI agent creates a new configuration item \(CI\) record in the CMDB.

-   **CMDB data certification and attestation manager AI agent**

    The CMDB data certification and attestation manager AI agent retrieves the data certification and attestation policies for a CI class and for similar classes. It can also create a data certification and an attestation policy.

-   **CMDB data manager AI agent**

    The CMDB data manager AI agent provides guidance on whether the fundamental data management processes are in place for the CMDB. It also helps admins to establish good CMDB processes.

-   **CMDB data ownership manager AI agent**

    The CMDB data ownership manager AI agent returns a link for the CI Class Manager \(the default value of a CI's **Managed by** field\). For a CI class, it determines ownership, validates ownership, and evaluates ownership quality.

-   **CMDB health metrics manager AI agent**

    The CMDB health metrics manager AI agent retrieves information on CMDB health jobs, health metrics status, and health scores.

-   **CMDB life cycle manager AI agent**

    The CMDB life cycle manager AI agent performs actions related to life-cycle management of CI classes: retrieve the life-cycle management policy and retirement definition for a CI class and create a life-cycle policy.

-   **CMDB principal class manager AI agent**

    The CMDB principal class manager AI agent determines whether the user can mark Cl classes as principal, suggests principal classes, and can mark or unmark a class as principal.

-   **CMDB search AI agent**

    The CMDB search AI agent searches the CMDB for a particular configuration item \(CI\) using single table query search or keyword query search and then displays a link to search results.

-   **CI summarizer AI agent**

    View a concise summary of key configuration item \(CI\) data directly on a CI form, in the workspace, or from any list. The summary can include discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests. For more information, see [Use the Now Assist CI summarizer AI agent](../../now-assist-cmdb/task/na-cmdb-agent-ci-summarizer.md).


## Running AI agents autonomously

**Important:** By default, all agentic workflow and AI agent records are read only.

To run the AI agents autonomously, you must first duplicate the agentic workflow and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

## Now Assist skills used by Now Assist for CMDB

-   **CI summarization**

    View a concise summary of key configuration item \(CI\) data directly on a CI form, in the workspace, or from any list. The summary can include discovery and class details, associated business services, security vulnerabilities, and related records like incidents, alerts, problems, and change requests. For more information, see [Use the Now Assist CI summarizer AI agent](../../now-assist-cmdb/task/na-cmdb-agent-ci-summarizer.md).

-   **Manage duplicate CIs**

    Resolve deduplication tasks with support from Now Assist. CMDB administrators follow step-by-step guidance to perform remediation, and can preview remediation results before applying a template. For more information, see [Use the Now Assist manage duplicate CIs skill](../task/now-assist-cmdb-mng-dupe-cis-skill.md).


