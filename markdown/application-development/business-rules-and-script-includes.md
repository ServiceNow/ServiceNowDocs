---
title: Business rules and script includes
description: Business rules are server-side actions that can be run during CRUD \(Create, Read, Update, Delete\) operations on instance records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Build form and business logic, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Business rules and script includes

Business rules are server-side actions that can be run during CRUD \(Create, Read, Update, Delete\) operations on instance records.

**Note:** Consider creating applications with help from agentic AI. For more information, see [Vibe coding and AI app development on the ServiceNow AI Platform](../../ai-capabilities/concept/use-ai-capabilities-in-custom-apps.md).

Some good practices when using Business Rules are:

-   Keep Business Rules small and specific.
-   Avoid modifying base system Business Rules.
-   Use Script Includes instead of global Business Rules.
-   Use scripting only when necessary.
-   Store reusable script logic in a script include.
-   Use queries to limit records processed within a Business rule.
-   Avoid client-callable Business Rules to improve efficiency when running client scripts.
-   Always use a condition with Business Rules to control when the Business Rule runs. Running Business Rules with conditions can also aid in debugging. Business Rules rarely run with no conditions.

Business Rules can be configured to run before or after a database operation. They can also be configured to run asynchronously and also before displaying a form or executing a query.

|Value|Runs|When to Use|Example|
|-----|----|-----------|-------|
|Before|Synchronously before the database operation|Set or update values on the current object as part of the save operation. Validate and abort execution if required.|A developer wants to set the state of the current record based on another input in that record.|
|After|Synchronously after the database operation|Trigger events and notifications after the database update to access the previous object or to make something occur in sequence. Update related records other than the base table being updated to access the previous object or to make something occur in sequence.|A developer wants to cascade values from the current record down to child records.|
|Async|Asynchronously executed as a separate process after the database operation is completed|The process triggered by the rule may take a while to run. When the user who triggered the operation does not need the output right away. Trigger events, notifications, or related record updates when access to the previous values of the record or a specific sequence of actions is not required.|A developer needs to trigger an external process that may take a while or update a large number of records.|
|Display|Executed every time the corresponding form is displayed|Used to make server-side objects available to client-side scripts.|A developer wants to write information about a user associated with the current record to the g\_scratchpad object to use in a client-side script.|

**Note:** current.update\(\)should not be used in any Business Rules. Using current.update\(\)triggers an additional database operation, which could cause duplicate notifications, recursive loops, etc.

Use Script Includes to store JavaScript functions and classes for use by server scripts. Each Script Include defines either an object class or a function that can be reused among any server-side scripts. For more information, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US).

Store any code that might need to be used elsewhere in a Script Include. Call the Script Include from a Business Rule, UI Action, workflow script, Scripted REST API, etc. Instead of calling a Business Rule from a UI Action or a UI Action from a Scripted REST API, put the code in a Script Include and call the Script Include from both places.

Keeping functions in a Script Include allows testing of the function before deploying the function in other scripted areas, thus reducing overall development and testing time.

For more information, see [Classic Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-api-reference&ft:locale=en-US).

**Parent Topic:**[Build form and business logic](build-form-and-business-logic.md)

