---
title: Advanced linter check scripts
description: Linter check scripts helps you in writing checks that look for issues in scripts. When a linter check is run on a record, it provides an abstract syntax tree for its code. You can use this abstract syntax tree to analyze issues with the code such as too many nested if statements or usages of slow API in a while loop.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create a linter check, Create a check, Use, Instance Scan, Maintain and monitor, Administer]
---

# Advanced linter check scripts

Linter check scripts helps you in writing checks that look for issues in scripts. When a linter check is run on a record, it provides an abstract syntax tree for its code. You can use this abstract syntax tree to analyze issues with the code such as too many nested if statements or usages of slow API in a while loop.

## Linter check usage

Linter checks have a unique object to use called `rootNode`. This is the root node of the parsed abstract syntax tree \(AST\) for the script of the current record. This object has many functions, but the `visit` function is the most important. The `visit` function takes a callback function as a parameter which gets called on every node of the tree. The callback function then takes a node as a parameter which represents the current node during its iteration. You can return false from the callback function to stop iterating the tree early, otherwise it keeps visiting every subnode in the tree of the node you called `visit` on.

For example, if you want to scan for a deprecated API called `badFunction()`. You can write a Linter Check with a script in the following example:

```
(function(engine) {
	engine.rootNode.visit(function(node) {
		if (node.getTypeName() === "NAME" &&
				node.getNameIdentifier() === "badFunction" &&
				node.getParent().getTypeName() === "CALL") {
			engine.finding.incrementWithNode(node);
		}
	});
})(engine);
```

When you run a scan with this Linter Check, it checks every record in the scan with a script field. For example, if a record in that scan has a script that looks like the following, the scan picks up a finding for this record.

```
/*
badFunction()
*/
// badFunction()
function badFunction() {
	return;
}
var GoodClass = Class.create();
GoodClass.prototype = Object.extendsObject(Object, {
	badFunction: function() {
		// actually good
	}
});
var badFunction = ["badFunction", "badFunction()"];
badFunctionButSometimesGood();

badFunction();
```

## Node functions

The following is a list of available functions to call on the node object.

-   `getRootNode()`: Get the root node of the tree for this node
-   `getParent()`: Get the parent of this node
-   `getLineNo()`: Get the line number location for this node
-   `getColumnNo()`: Get the column number location for this node
-   `toSource()`: Get the source for this node. The source is based on this node and its children
-   `getTypeName()`: Get the node type name of this node. For example, a function call in source is tokenized as a node with the type name of "CALL"

    **Note:** The values of `node.getTypeName()` are from different types of nodes in an Abstract Syntax Tree \(AST\). The possible values come from Rhino's AST parser itself.

-   `getNameIdentifier()`: If the node type of this node is "NAME", then return the identifier, which is the string value of the name itself. A "NAME" node represents a simple name that is not a keyword, like a function name or a variable name.

    **Note:** If this node is not a NAME node, then the result is null.

-   `getAbsolutePosition()`: Get the absolute position of this node. The absolute position is the number of characters from the start of the script to this node
-   `compareTo(other)`: Compare this node with another node. The node with a greater absolute position and length will be the larger in comparison. `other` is a node to compare with this node
-   `visit(callbackFunction)`: Visit each node in the subtree starting from this node and execute the given callback function on each node. `callbackFunction` is a function that will be executed on each node in the subtree of this node. This callback function takes a LinterCheckAstNode as a parameter which is will be the node being visited
-   `debugPrint()`: Returns a string representation of the abstract syntax tree, starting from this node. Each line contains information about a node, and the indentation represents the hierarchy relationship between the nodes. The information in each line is arranged as follows
    1.  Absolute position
    2.  Node type name
    3.  Position relative to parent
    4.  Length
    5.  Name identifier \(if a NAME node\)

For more information, see [LinterCheckAstNode API - Scoped, Global](https://www.servicenow.com/docs/access?context=LinterCheckAstNodeAPIBoth&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

**Parent Topic:**[Create a linter check](../task/hc-linter-check.md)

