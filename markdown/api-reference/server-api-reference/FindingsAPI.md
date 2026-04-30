---
title: Findings - Scoped, Global
description: The Findings API provides methods for handling how an Instance Scan check produces findings.Increases the count of the current finding.If the current finding is from a linter check, this method increments the current finding count and simultaneously passes the linter node object to the finding.Sets the source of the current finding based on the provided GlideRecord.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Findings - Scoped, Global

The Findings API provides methods for handling how an Instance Scan check produces findings.

This API is included with the Instance Scan \(com.glide.instance\_scan\) plugin and runs in the `sn_instance_scan` namespace. For more information, see [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

In Instance Scan, checks run on each record in the scope of a scan on the instance to generate findings. Each finding holds information about an issue record and which check it violated. Findings methods are used in Instance Scan checks as part of the engine object passed to the user. Add the code to the **Script** field in the check form.

See also:

-   [Getting started with checks](https://www.servicenow.com/docs/access?context=hs-intro-health-check&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)
-   [Findings](https://www.servicenow.com/docs/access?context=hs-findings&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Findings - increment\(\)

Increases the count of the current finding.

The finding count starts at zero for each record that a check analyzes in a scan. When called, this method increments the finding count. The count indicates that a finding is to be generated for the current record.

This method can be called multiple times to signify that this finding has multiple occurrences of a check violation in the current record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to count the number of records with a failed state in a table type check. For more information, see [Create a table type check](https://www.servicenow.com/docs/access?context=hs-create-table-health-check&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
(function(engine) {
  if (current.getValue("state") == "failed") {
    engine.finding.increment();
  }
})(engine);
```

## Findings - incrementWithNode\(Object node\)

If the current finding is from a linter check, this method increments the current finding count and simultaneously passes the linter node object to the finding.

Use this method in the Script field in the [Linter Check form](https://www.servicenow.com/docs/access?context=hc-linter-check&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). This method saves information about the given node, such as a line number in a current finding's details column.

See also:

-   [Advanced linter check scripts](https://www.servicenow.com/docs/access?context=hs-linter-check-scripts&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)
-   [LinterCheckAstNode API](../../LinterCheckAstNode/concept/LinterCheckAstNodeAPIBoth.md#)

|Name|Type|Description|
|----|----|-----------|
|node|Object|Node object from the linter check.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to increment linter type nodes in a linter check. For information on using linter check methods, see [LinterCheckAstNode API](../../LinterCheckAstNode/concept/LinterCheckAstNodeAPIBoth.md#).

```
(function(engine) {
  engine.rootNode.visit(function(node) {
    if (node.getTypeName() === "NAME" &&
        node.getNameIdentifier() === "soughtFunction" &&
        node.getParent().getTypeName() === "CALL") {
      engine.finding.incrementWithNode(node);
    } 
  });
})(engine);
```

## Findings - setCurrentSource\(GlideRecord source\)

Sets the source of the current finding based on the provided GlideRecord.

Use this method in the **Script** field of a Script Only check. This method is not used for any other checks because they automatically set the source as the current record during the scan. For more information, see [Create a script only check](https://www.servicenow.com/docs/access?context=hs-create-script-health-check&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|source|GlideRecord|The record to set as the source record for the current finding. This value is added as a reference in the Source field of the Scan Findings \[scan\_finding\] table.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to set the current source to an incident record in a script only check. For more information, see [Create a script only check](https://www.servicenow.com/docs/access?context=hs-create-script-health-check&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
(function(engine) {
  var gr = new GlideRecord('incident');
  gr.get('2f99f330730210100a5310c92bf6a798');
  engine.finding.setCurrentSource(gr);
  engine.finding.increment();
})(engine);
```

