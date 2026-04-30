---
title: Sanitize shell arguments transform functions
description: Use sanitize shell arguments transform functions to remove any potentially unsafe command injections in String data pills to be used for Bash shell scripting.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Transform functions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Sanitize shell arguments transform functions

Use sanitize shell arguments transform functions to remove any potentially unsafe command injections in String data pills to be used for Bash shell scripting.

Sanitize shell arguments transform functions require a String input data pill. Make sure to use the correct input [data pill type](action-inputs-outputs.md) when applying sanitize shell arguments transform functions. If a sanitize shell arguments transform function is applied to an improper data type, the data is not transformed at runtime and the input value is returned instead. For more information on confirming your flow runtime values, see [Test a flow](../task/flow-test.md).

**Note:** When a data pill is dropped into the **Command** input for an [SSH step](ssh-step-action-designer.md), the sanitize shell arguments transform function category automatically appears.

## Sanitize Bash shell arguments

Returns a String free of any unsafe command injections in your Bash shell script. Wraps the input String with single quotes and escapes any existing single quotes so that you can pass the String directly to a shell function as a safe argument.

|Input data pill|Output data pill|
|---------------|----------------|
|String|String - String with Bash shell arguments properly escaped|

**Parent Topic:**[Transform functions](../concept/transform-functions.md)

