---
title: LinterCheckAstNode - Scoped, Global
description: The LinterCheckAstNode API provides methods for getting abstract syntax tree \(AST\) node details in linter checks.Retrieves the string value of a name node type. A name node represents a simple identifier that is not a keyword, such as a function or variable name.Gets the parent node object of the accessed node.Gets the type of the accessed node.Accesses each node in the subtree starting from this node and executes a given callback function on each node.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# LinterCheckAstNode - Scoped, Global

The LinterCheckAstNode API provides methods for getting abstract syntax tree \(AST\) node details in linter checks.

This API is included with the Instance Scan \(com.glide.instance\_scan\) plugin and runs in the `sn_instance_scan` namespace. For more information, see [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Use the methods in this class to run linter checks on AST node types by adding code to the **Script** field in the [Linter Check form](https://www.servicenow.com/docs/access?context=hc-linter-check&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). For more information, see [Advanced linter check scripts](https://www.servicenow.com/docs/access?context=hs-linter-check-scripts&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Create a linter check to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated. You can use the abstract syntax tree to analyze issues with the code.

Access methods in this API using the Instance Scan engine.rootNode object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## LinterCheckAstNode - getNameIdentifier\(\)

Retrieves the string value of a name node type. A name node represents a simple identifier that is not a keyword, such as a function or variable name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|If the linter object is a name node type, return the name as a string. Null otherwise.|

The following example uses the Findings API [incrementWithNode\(\)](../../Findings/concept/FindingsAPI.md#) method in a linter check. Use this method in the Script field of the [Linter Check form](https://www.servicenow.com/docs/access?context=hc-linter-check&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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

## LinterCheckAstNode - getParent\(\)

Gets the parent node object of the accessed node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Parent node object of the accessed node.|

The following example uses the Findings API [incrementWithNode\(\)](../../Findings/concept/FindingsAPI.md#) method in a linter check. Use this method in the Script field of the [Linter Check form](https://www.servicenow.com/docs/access?context=hc-linter-check&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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

## LinterCheckAstNode - getTypeName\(\)

Gets the type of the accessed node.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Type name of the accessed node. For example, a function call in the source is tokenized as a node with the type name of `CALL`.|

The following example uses the Findings API [incrementWithNode\(\)](../../Findings/concept/FindingsAPI.md#) method in a linter check. Use this method in the Script field of the [Linter Check form](https://www.servicenow.com/docs/access?context=hc-linter-check&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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

## LinterCheckAstNode - visit\(Function callbackFunction\)

Accesses each node in the subtree starting from this node and executes a given callback function on each node.

|Name|Type|Description|
|----|----|-----------|
|callbackFunction|Function|Callback function to be executed on each node in the subtree of this node. This callback function takes a node as a parameter which is the node to be visited.|

|Type|Description|
|----|-----------|
|None| |

The following example uses the Findings API [incrementWithNode\(\)](../../Findings/concept/FindingsAPI.md#) method in a linter check. Use this method in the Script field of the [Linter Check form](https://www.servicenow.com/docs/access?context=hc-linter-check&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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

