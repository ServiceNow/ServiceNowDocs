---
title: Query Generation logs
description: Every call to a Query Generator and its results are logged in the Query Generation Log \[sn\_query\_gen\_log\] table.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-25"
reading_time_minutes: 4
breadcrumb: [Reference, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Query Generation logs

Every call to a Query Generator and its results are logged in the Query Generation Log \[sn\_query\_gen\_log\] table.

## Using the logs

Go to **Query Generation** &gt; **Administration** &gt; **Logs** to inspect failed or incorrect queries.

1.  Find the entry by user, date, or utterance.
2.  Check **Semantic Entities/Dimensions/Segments Count**
3.  Open **Query Constitutor Output** to see what was selected.
4.  Compare with **Semantic Filter Result** for raw semantic matches.

|Symptom|Likely cause|Fix|
|-------|------------|---|
|"Unable to understand" response|System cannot find a matching table|Improve entity description; rephrase with table name; verify AI search is running; verify that all Indexed Sources are fully processed.|
|Wrong table selected|Similar table names, no disambiguation|Add semantic usage instructions to differentiate.|
|Wrong table selected \(permissions\)|User lacks read access to the intended table or fields|Verify and grant table and field read ACLs for the intended data.|
|Missing field in results|Dimension turned off, unclear label, or field not in semantic layer|Check dimension is active; update label.|
|Related fields not pulled in|Referenced table missing from semantic layer or reference dimension turned off|Add and enable the referenced table entity; enable the reference dimension.|
|Wrong filter applied|Bad segment match|Fix segment name and description; disable the segment.|
|No filter when expected|No matching segment; phrasing too vague|Create a manual segment; rephrase question.|
|Segment from report is wrong|Auto-generated segment has stale or irrelevant filter|Disable the report segment source or the specific segment.|

|Column|Description|Shown by default?|
|------|-----------|-----------------|
|Created|Timestamp of the call to Query Generation|Yes|
|User|The user from the User \[sys\_user\] table who made the call. If this is blank, try Created by.|Yes|
|Utterance|The plain language question asked by the user|Yes|
|Status|The success or otherwise of the call|Yes|
|Error message|If the status is "error," this is the error message that is returned to the user.|Yes|
|Total time|Time in milliseconds it took for the AI to process the query and return the response|Yes|
|"X" time|Time in milliseconds each component X spent processing the query|Yes|
|Semantic Filter Results|Fields in the semantic layer tables that the query references, in JSON|Yes|
|Utterance Bank Results|Questions similar to the user's question \(Utterance\) that were found in the Utterance Bank and used to interpret the user's question, in JSON|Yes|
|Response|The JSON response to the query|Yes|
|Entities|The records in the Entities table that are referenced by the query. Each record corresponds to a facts table.|Yes|
|Query Constitutor Output|JSON of the query that is generated|Yes|
|Source|The application from which the question was asked. If the question was asked from the Now Assist panel when it was open in a page that is not part of an application, the UUID of that page is shown instead.|Yes|
|Response|The response that the LLM returns|Yes|
|Generative AI Log|The LLM used for the query|Yes|
|Conversation|Unique chat conversation ID, such as in a Now Assist Panel to Query Generation conversation|Yes|
|ACL Time|Time it took to validate the Access or Security of the user for the underlying table|No|
|Additional info|Start time, total calls, and other metadata about the AI Search run|No|
|Created by|Person who created the query. Includes ServiceNow® staff members logged on as maint.|No|
|Domain|Domain in which the query was created|No|
|Dot walked|Whether the query included dot walking between tables \(true/false\)|No|
|Entity has usage score|Whether the entity has a usage score \(true/false\)|No|
|Entity source|Whether the Source was in ENTITIES, USER SENSE, or SEGMENTS|No|
|Error code|The error code, if there was an error|No|
|Follow Up Generated|The number of follow-up questions that the LLM generated in response to the query|No|
|Follow Up Returned|How many of the generated follow-up questions are actually returned. The questions must refer to tables that the querying user can access and are in the semantic layer, for example.|No|
|LLM Time|Time spent by the large language model \(LLM\) on the query|No|
|Query Constructor Time|Time spent by the query constructor on the query|No|
|RAG time|Time spent by the retrieval-augmented generation \(RAG\) on the query|No|
|Semantic Dimensions count|Number of table records \(dimensions\) examined for the query|No|
|Semantic Entities Count|Number of tables \(entities\) examined for the query|No|
|Semantic Filter Results|Results of running the semantic filter|No|
|Semantic Filter Time|Time spent by the semantic filter|No|
|Semantic Segments Count|Number of segments examined for the query|No|
|Source Table|Name of table corresponding to Source Id|No|
|Tags|Any tags that you add to the log|No|
|Updated|Date stamp when log entry was last updated|No|
|Updated by|User responsible for last log entry update|No|
|Updates|Count of updates to the log entry|No|
|Utterance bank results|Similar examples extracted from utterance bank|No|
|Utterance bank time|Amount of time spent searching the utterance bank|No|

**Parent Topic:**[Query Generation reference](../concept/query-generation-reference.md)

**Related topics**  


[Common AI Data Explorer issues and fixes](../../ai-data-explorer/concept/ai-data-explorer-troubleshooting.md)

