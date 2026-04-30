---
title: WalkWorkflow - Global
description: The WalkWorkflow script include provides methods to walk a workflow and return a list of successors for each activity along with a shortest path order that indicates the activity depth in the workflow.Constructor for Walkworkflow class.Computes the full sequence for every path.Computes the sequences of activities.Outputs the internal state of this class to gs.print\(\).Outputs the sequences internal to this class to gs.print\(\).Outputs the shortest path orders internal to this object to gs.print\(\).Returns all the activities at the specified shortest path order.Returns the activity sequences.Walks the workflow and sets up the activity shortest path ordering.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# WalkWorkflow- Global

The WalkWorkflow script include provides methods to walk a workflow and return a list of successors for each activity along with a shortest path order that indicates the activity depth in the workflow.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Walkworkflow - Walkworkflow\(GlideRecord workflowVersion\)

Constructor for **Walkworkflow** class.

|Name|Type|Description|
|----|----|-----------|
|workflowVersion|GlideRecord|GlideRecord on table wf\_workflow\_version of the workflow version to analyze.|

|Type|Description|
|----|-----------|
|Workflow|Workflow object just created.|

## Walkworkflow - computeFullSequences\(\)

Computes the full sequence for every path.

Does not combine paths at Join activities. After calling this method, call getSequences\(\) to yield the computed sequences.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## Walkworkflow - computeSequences\(\)

Computes the sequences of activities.

All sequences leading up to a join end at the join and then a single sequence from the join is computed. This ensures that all sequences can be walked up to a join, and then the sequence can be walked from the join. After calling this method a call to getSequences\(\) will yield the computed sequences.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## Walkworkflow - dump\(\)

Outputs the internal state of this class to gs.print\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## Walkworkflow - dumpSequences\(\)

Outputs the sequences internal to this class to gs.print\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## Walkworkflow - dumpShortestPathOrders\( description\)

Outputs the shortest path orders internal to this object to gs.print\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## Walkworkflow - getActivitiesAtOrder\(Number order\)

Returns all the activities at the specified shortest path order.

|Name|Type|Description|
|----|----|-----------|
|order|Number|The order number the client is interested in.|

|Type|Description|
|----|-----------|
|String Array|An array of activity sys\_ids at the specified order. If an empty array is returned, there are no more activities.|

## Walkworkflow - getSequences\( \)

Returns the activity sequences.

The walk\(\) method must have been called prior to calling this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|A string of \|-delimited sequences. Each sequence is a comma-delimited list of activity ids \(table wf\_workflow\_activity\).|

## Walkworkflow - walk\(Boolean fullSequences\)

Walks the workflow and sets up the activity shortest path ordering.

After calling this method the client would call the various accessor methods to obtain relevant data about the workflow.

|Name|Type|Description|
|----|----|-----------|
|fullSequences|Boolean|\(Optional\) If **true**, computes the full sequences. Default is false.|

|Type|Description|
|----|-----------|
|void| |

